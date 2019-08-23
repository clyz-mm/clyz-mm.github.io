---
layout:     post
title:      ubuntu ibus BUG解决
subtitle:   
date:       2019-04-11
author:     clyz-mm
header-img: img/post-bg-desk.jpg
catalog: 	 true
tags:
    - ubuntu
    - iBus
---  

ubuntu iBus 只能选择第一个候选词问题解决：  
终端输入：  

      sudo rm-rf ～/.cache/ibus/libpinyin  

然后重启：  
      
      reboot  
     
`治标不治本，会复发，暂时不知道怎么解决。。。`  

