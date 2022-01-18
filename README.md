# Headline

> An awesome project.

来一段代码

```python
import nonebot
from nonebot.adapters.cqhttp import Bot as CQHTTPBot
from services.db_context import init, disconnect


nonebot.init()
driver = nonebot.get_driver()
driver.register_adapter("cqhttp", CQHTTPBot)
config = driver.config
driver.on_startup(init)
driver.on_shutdown(disconnect)
# 优先加载定时任务插件
nonebot.load_plugin("nonebot_plugin_apscheduler")
nonebot.load_plugins("basic_plugins")
nonebot.load_plugins("plugins")
nonebot.load_plugins("plugins_mine")

if __name__ == "__main__":
    nonebot.run()
```

来一段C语言



```c
//  Created by www.runoob.com on 15/11/9.
//  Copyright © 2015年 菜鸟教程. All rights reserved.
//
 
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
    int i,j,k,TLen,PLen,count=0;
    char T[50],P[10];
    printf("请输入两个字符串，以回车隔开，母串在前，子串在后：\n");
    gets(T);
    gets(P);
    TLen=strlen(T);
    PLen=strlen(P);
    for(i=0;i<=TLen-PLen;i++)
    {
        for(j=0,k=i;j<PLen&&P[j]==T[k];j++,k++)
            ;
        if(j==PLen)count++;
    }
    printf("%d\n",count);
    system("pause");
    return 0;
}
```

