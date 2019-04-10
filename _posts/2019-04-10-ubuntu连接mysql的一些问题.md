---
layout:     post
title:      ubuntu连接mysql的一些问题
subtitle:   
date:       2019-04-10
author:     clyz
header-img: img/post-bg-desk.jpg
catalog: 	 true
tags:
    - ubuntu
    - mysql
---

- ubuntu终端连接mysql的问题：

用普通模式登陆时：

***

$ mysql -u root -p

***

提示：

Access denied for user 'root'@'localhost'

! 注：后面没有 (using password: NO) 或者  (using password: YES)

但是使用root用户却可以正常登陆：

***

$ sudo mysql -u root -p

***

解决方法：

***

正常登陆：

$ sudo mysql -u root -p

修改user表root用户的plugin的值为mysql_native_password

update mysql.user set plugin = 'mysql_native_password' where user = 'root';

查看修改结果：

select *from mysql.user\G;

修改成功后一定要更新：

flush privileges;

然后退出mysql

