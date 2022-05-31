# cppcheck_plugin
这是存储我自己使用的cppcheck软件的插件。

## misra的注释插件

将misra2012_cn.txt、misra2012_en.txt、misra.json放在自己本地，也可以放入cppcheck的软件目录，这样后续操作可以不带路径

misra.json说明，注意--rule-texts路径，换成misra2012_en.txt英文输出
```json
{
    "script": "misra.py",
    "args": 
    [
        "--rule-texts=./misra2012_cn.txt" 
    ]
}
```

```shell
cppcheck --addon=misra.json test.c   //注意json和源文件路径，misra.json在环境变量中不用添加路径
```
