title: GIT练习
date: 2015-06-24 22:13:58
tags:
---

#GIT学习

`测试`

```
Git is a version control system.
Git is free software.
```

#生成密匙
```
ssh-keygen -t rsa -C "youremail@example.com"
```

#测试github连通性
```
ssh -T git@github.com
```

`Hello World`

#GIT笔记 #

#GIT设置用户名 邮箱

```
$git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
#`pwd`显示当前目录

#`ls -ah`查看隐藏目录

##GITb##

> `git init`初始化仓库

> `git add <file>`

> `git commit`提交

> `git diff <file>`查看修改内容

> `git status`查看工作前状态

> `git rm <file>`删除文件

> `git log`查看日记记录

> `git branch`查看分支

> `git branch <name>`创建分支

> `git checkout <name>`切换分支

> `git checkout -b <name>`创建+切换分支

> `git merge <name>`合并某分支到当前分支

> `git log --graph --pretty=oneline --abbrev-commit`查看分支合并情况

> `git log --graph`分支合并图

>`git branch -d <name>`删除dev分支

##小结
>1. 合并分支时，加上`--no-ff`参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而`fast forward`合并就看不出来曾经做过合并。

>2. 