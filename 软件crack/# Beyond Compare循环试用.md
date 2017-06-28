# beyond compare 4你的30天评估期到期解决办法
# Beyond Compare 循环试用

## MAC

终端命令：
```
$ cd /Applications/Beyond\ Compare.app/Contents/MacOS/
$ mv BCompare BCompare.real
```
新建BCompare文件，内容：
```
#!/bin/bash
rm "/Users/$(whoami)/Library/Application Support/Beyond Compare/registry.dat"
"`dirname "$0"`"/BCompare.real $@
```
保存之后执行：
```
$ chmod +x BCompare
```

## windows
>找到beyond Compare 4文件夹下面的BCUnrar.dll，将其删掉或者重命名，再重新打开接着使用
-此方法仅用于windows


## linux

删除其配置文件 ~/.config/bcompare/registry.dat文件，就会重新计算期限。