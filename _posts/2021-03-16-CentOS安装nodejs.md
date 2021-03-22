---
title: CentOS安装nodejs
tags: CentOS,Linux,nodeJS
date: 2021-03-16
layout: post
author: clyz-mm
header-img: img/post-bg-desk.jpg
catalog: true
renderNumberedHeading: true
grammar_cjkRuby: true
---

进入安装目录
``` 
# cd /usr/local
```
下载node压缩包
``` 
# wget https://npm.taobao.org/mirrors/node/latest-v14.x/node-v14.6.0-linux-x64.tar.gz
```
解压并重命名

``` 
# tar -zxvf node-v14.6.0-linux-x64.tar.gz
# mv node-v14.6.0-linux-x64 node-v14.6.0

```
配置环境，在下面文件最后加入两行配置：

``` 
# vim /etc/profile

```

``` 
export NODE_HOME=/usr/local/node-v14.6.0
export PATH=$PATH:$NODE_HOME/bin
```
更新配置文件

``` 
source /etc/profile
```
完成