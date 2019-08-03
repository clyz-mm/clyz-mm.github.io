---
layout:     post
title:      arch安装mysql
subtitle:   解决初始化空密码的问题
date:       2019-8-3
author:     clyz
header-img: img/post-bg-desk.jpg
catalog: 	 true
tags:
    - linux
---  
开始安装：  

    $ yay -S mysql  
    $ sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql  

此时若初始化提示创建了帐号但是密码为空，那么执行一下语句：  

    $ sudo mysql_secure_installation  

按照提示设置新的root密码即可。
