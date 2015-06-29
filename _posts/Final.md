title: Final
date: 2015-06-25 18:11:02
tags:
---

#GIT地址
##https://www.v2ex.com/t/128478?p=1

>1.centos7安装pip
http://icehe.me/2015/03/31/linux/[06]%20Linux%20%E9%80%9A%E8%BF%87%20pip%20%E5%AE%89%E8%A3%85%E4%BD%BF%E7%94%A8%20Shadowsocks%20-%20CentOS%207/

>2. 通过pip安装扩展
`pip install tornado pycurl u-msgpack-python jinja2 chardet requests`

>3. 安装mysql-python模块
安装`pip install pycrypto`
要安装`yum install python-devel`解决依赖关系
! http://www.jianshu.com/p/ac521af24a82
`pip install --allow-external mysql-connector-python mysql-connector-python`
http://m.oschina.net/blog/331903

>4. 解决 `importerror no module named mysql connector` 可写blog
http://bbs.scmroad.com/thread-27205-1-1.html

>5. pbkdf2
https://disqus.com/home/discussion/binux/qiandaotoday_binux/

>6. 安装redis
!yum install tcl
http://keenwon.com/1335.html
pip install redis

>7. 后台托管
http://linbo.github.io/2013/04/04/supervisor/
http://blog.csdn.net/xia7139/article/details/9033483
https://www.google.com/#q=supervisor+%E9%85%8D%E7%BD%AE
!!http://www.phpgao.com/supervisor_shadowsocks.html

>8. ImportError: No module named MySQLdb
!http://www.111cn.net/sys/CentOS/53617.htm
http://blog.csdn.net/guzicheng/article/details/5884106

#参考
> http://bbs.jianguoyun.com/topic.php?id=4438

> http://www.somacon.com/p520.php

> http://www.4byte.cn/question/589861/connect-to-old-mysql-installation-using-python-mysql.html


```
pip install --allow-external mysql-connector-python mysql-connector-python
```

>http://www.linuxidc.com/Linux/2013-08/88234.htm

>http://stackoverflow.com/questions/9171983/any-met-python-import-paramiko-and-crypto-err-like-not-using-mpz-powm-sec

>http://blog.scicooking.net/2014/python-paramiko-rebuild-libgmp-to-avoid-timing-attack-vulnerability.html
python paramiko 出现警告信息