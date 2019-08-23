---
layout:     post
title:      ubuntu boot error
subtitle:   
date:       2019-04-10
author:     clyz-mm
header-img: img/post-bg-desk.jpg
catalog: 	 true
tags:
    - ubuntu
---

前几天ubuntu在休眠后突然就死机了，没多想的我长按电源键以强制关机。
但是一如既往的骚紫色登陆界面没有出现，换来的是一个黑乎乎的shell界
面，心想这是什么鬼？从来没有遇到过，敲了几次reboot无果后，还是老老
实实上网查了一些资料，最终完美解决。如果你的错误提示类似是下面这样的：

***

    fsck from util-linux 2.26.2

    /dev/sda5 contains a file system with errors,check forced.


    ~(略)


    The root filesystem on /dev/sda5 requires a manual fsck


    ~(略)


    (initramfs)_

***


那么直接在命令中输入：

    fsck /dev/sda5 -fy

等待一会，此时ubuntu已经在修复硬盘了，修复完成后命令输入reboot即可！
