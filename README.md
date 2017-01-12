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
移除文件：
```bash
$ rm 文件//移除本地文件
$ git rm 文件//移除git仓库中的此文件
//再commit,git库里的文件就会被移除
$ git rm --cached 文件//移除git暂存区中的此文件

$ git rm \*~//移除此目录及其子目录下所有的~文件
$ git rm *~//移除此目录下所有的~文件
```

其他的操作：
```bash
$ git status
//查看当前文件与库的状态

$ git log
git log -p -2//-p 选项展开显示每次提交的内容差异，用 -2 则仅显示最近的两次更新
$ git log --pretty=oneline 
//查看日志，后者是单行显示
![pic](https://github.com/xianyuli/LearnGit/pic/log语法.png "log语法")
$ git reflog 
//查看每一次输入的命令

$ git diff 
//查看本地与库的不同
$ git diff README.md
//查看文件与库文件的不同

$ git reset --hard head^ 
//回退版本 head表示当前版本，head^代表上一版本，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
$ git reset --hard commit_id 
//根据版本号回退，commit_id可以在git reflog命令下查看。
$ git branch //查看版本分支

```


* github仓库操作
	
与github仓库建立起信任关系：
```bash
//本地生成ssh key
$ ssh-keygen
//将id_rsa.pub中的公匙添加到github的ssh当中即可

克隆库到本地工作目录
$ git clone git@github.com:xianyuli/LearnGit.git


```