---
layout: post
title: 在虚拟机Ubuntu和宿主机Windows之间传送文件
date: 2017-5-24 
tags: Ubuntu   
---

　方便下次使用

　在虚拟机Ubuntu和宿主机Windows之间传送文件

　方法一：安装VMware Tools，设置共享文件夹（推荐）

　　　　　安装教程：http://www.cnblogs.com/sunev/archive/2012/03/16/2400887.html

　方法二：在宿主机上安装FTP文件传输软件

　步骤如下：

　　1.Ubuntu中安装ssh，命令：sudo apt-get install ssh openssh-server

　　2.查看虚拟机中Ubuntu的IP地址，命令：ifconfig

　　下图就是虚拟机中Ubuntu的IP地址

　　![](http://img.blog.csdn.net/20160229201925371)


　　3.回到宿主机中，百度搜索下载FileZilla，其实这就是一个基于FTP协议、在两台电脑之间进行文件传送的软件（上学期做项目做过这方面的功能哈哈哈），另一台电脑可以在远端，在当前情况下，另一台电脑就是装在本地的虚拟机。

　　FileZilla运行界面如下。红色方框1中，主机：就是填入Ubuntu的IP地址（可以只填IP地址，也可以自己补充上IP地址前面的协议）；用户名：Ubuntu下的用户名称；密码：Ubuntu下的用户密码；端口：22。

　　4.点击快速连接之后就会出现本地和远程文件列表，可以互相拖拽文件。

　　![](http://http://img.blog.csdn.net/20160229203803576?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


　　本文转载：[点击转到](http://blog.csdn.net/zhu_zhu_wonder/article/details/50767922)



