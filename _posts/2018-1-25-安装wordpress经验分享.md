---
layout: default
title:  "安装wordpress经验分享.md"
categories: posts rwd
image:
  teaser: 主题位置.png
  feature: 主题位置.png
---
# 安装wordpress经验分享

###  翻了翻记录，看到了谢同学分享的视频教程跟着学了一下：

[视频地址](http://www.jikexueyuan.com/course/935_2.html?ss=1)

###  个人理解，安装大概是先到相关网站下载了xampp和WordPress  然后用xampp到网页去改一下东西 再下载WordPress


## 第一步：

###  跟着视频做，大约学到在视频10分钟的位置，就可以做到这样了：

<img border="0" src="/images/初步构建完成.png" alt="Pulpit rock" width="800" height="500">

## 第二步：

###  加入老师需要的插件：一个Plugin，一个Theme ，步骤大致是：  Gantry 5 Framework  --> 插件 pluginG5_helium --> 主題 theme

[Plugin压缩包](https://github.com/gantry/gantry5/releases/download/5.4.22/wordpress-pkg_gantry5_v5.4.22.zip)

[theme压缩包](https://github.com/gantry/gantry5/releases/download/5.4.22/wordpress-tpl_g5_helium_v5.4.22.zip)


## 具体步骤如下
 
###  1.  plugin是在插件那里上传wordpress-pkg_gantry5_v5.4.22.zip ，步骤是插件>>上传插件>>添加zip
 
 如图：
 
 <img border="0" src="/images/插件位置.png" alt="Pulpit rock" width="800" height="500">
 

###  2. Theme是在主题那里上传wordpress-tpl_g5_helium_v5.4.22.zip，步骤是外观>>主题>>添加zip
 
 如图：
 
 <img border="0" src="/images/主题位置.png" alt="Pulpit rock" width="800" height="500">
 
 
 
 
##  上传zip期间遇到的问题：

###  当时我按群里的视频教程安装了WordPress和xampp，但是在上传群里说要安装的插件时，出错了，它说文件过大..

如图所示：

<img border="0" src="/images/问题.png" alt="Pulpit rock" width="1500" height="200">


## 于是，通过百度和问老师，找到了以下解决方法：

## 1. 去你本機的XAMPP下的php目錄下找php.ini

###  如果找不到文件的话打开扩展名，如图：

<img border="0" src="/images/扩展名.png" alt="Pulpit rock" width="800" height="500">

## 2.先用notepad++打开php.ini这个文件，具体路径大家自行找找，我这边没有在服务器上测试，使用的是XAMPP本地环境（xampp/php文件夹下）

## 3.Ctrl+F分别搜索upload_max_filesize = 2M和post_max_size = 8M，改一下文件上传最大限制，比如都改为40M。

###  注意搜索关键词时，不要直接复制，不要太长，空白及數字可能都不一樣，导致找不到。

## 4.然后保存，重启一下apache服务（即重启下图这个东西）。 

<img border="0" src="/images/XAMPP服务.png" alt="Pulpit rock" width="800" height="500">

###  按stop》》start就是重启该服务了

## 5.重新上传对应的zip文件
