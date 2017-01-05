git学习笔记
========
第一部分
--------

* 本地仓库操作
创建文件：
```bash
$ touch 文件
```
添加文件到暂存区：
```bash
$ git add 文件名
```
提交暂存区文件到仓库：
```bash
$ git commit -m 必要的说明	
$ git commit -a 必要的说明	
//相当于运行 git add 把所有当前目录下的文件加入暂存区域再运行git commit.
```
```bash
$ git status//查看当前文件与库的状态

$ git log
$ git log --pretty=oneline //查看日志，后者是单行显示
$ git reflog //查看每一次输入的命令

$ git diff //查看本地与库的不同
$ git diff README.md//查看文件与库文件的不同

```
