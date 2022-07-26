---
title: 文件夹因存在.git而无法提交到git的解决办法
date: 2022-07-26 23:59:33
tags:
---

无法提交根本原因是next主题也是一个repo。

解决方法:

1.剪切 themes/next/.git文件夹到其它处

 

2.从暂存区删除该文件夹

git rm --cache themes/next
 

3.使用git status查看状态



4.三步走: -->git add .  -->git commit -m "" -->git push

 

5.再移回themes/next/.git文件夹