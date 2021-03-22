---
title: npm start autoprefixer 异常
tags: Linux,npm,CentOS
date: 2021-03-16
layout: post
author: clyz-mm
header-img: img/post-bg-desk.jpg
catalog: true
renderNumberedHeading: true
grammar_cjkRuby: true
---

npm start时出现以下错误是因为*autoprefixer*版本过高：
==Error：PostCSS plugin autoprefixer requires PosCSS 8 #F44336==.


降低版本即可：
``` 
# npm i postcss-loader autoprefixer@8.0.0 -D
```