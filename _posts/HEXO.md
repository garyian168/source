title: HEXO
date: 2015-06-28 20:57:27
tags:
---

#HEXO

##1. 安装开发者包
>
```
yum groupinstall 'Development Tools' 
```
##2. 客户端生成ssh密匙
>1. 在空白处单击右键，选择`Git Bash Here`打开终端

>2. 输入命令`ssh-keygen -t rsa -f ~/.ssh/id_rsa.xx [-C "email]`

##3. 新建git用户
>1. 
```
adduser git 
```  

>2. 
```
usermod -a -G www git //把git用户添加到www组
```

>3. `su git`切换到git用户

>4. `cd ~`

>5. `mkdir .ssh && cd .ssh`

>6. `touch authorized_keys`

>7. `vi authorized_keys`把公钥`id_rsa.pub`里的内容复制粘贴到里面

>8. `mkdir blog.git && cd blog.git`创建blog库

>9. `git init --bare`初始化

##4. 编辑git权限
>1. 
`chmod g-w /home/git `  
`chmod 700 /home/git/.ssh `   
`chmod 600 /home/git/.ssh/authorized_keys`


##5.编辑SSH配置文件
>1. `vi  /etc/ssh/sshd_config`

>2. 
`RSAAuthentication yes`  
`PubkeyAuthentication yes`  
`AuthorizedKeysFile  .ssh/authorized_keys`

>3. 
`vi /etc/passwd`  
把`/bin/bash`改为  
`/usr/bin/git-shell`

>4. 运行`ssh -vvT git@120.26.215.26`测试是否连接正常

##6. Hooks钩子
>1.  `cd /home/git/blog.git/hooks/`  

>2. `touch post-receive`

>3.  `chown -R git:git post-receive`

>4. `vi post-receive`

>5. 加入以下内容  
```#!/bin/bash -l
GIT_REPO=/home/git/blog.git
TMP_GIT_CLONE=/tmp/blog
PUBLIC_WWW=/home/wwwroot/default
rm -rf ${TMP_GIT_CLONE}
git clone $GIT_REPO $TMP_GIT_CLONE
rm -rf ${PUBLIC_WWW}/*
cp -rf ${TMP_GIT_CLONE}/* ${PUBLIC_WWW}
```  

>6. `chmod +x post-receive`给予`post-receive`执行权限  

>7. `chmod 775 -R /home/wwwroot/default`

##7. 配置HEXO

>1.
```
deploy:
  type: git
  repo: 
    Aliyun: git@hostname:blog.git,master
  message: update
```