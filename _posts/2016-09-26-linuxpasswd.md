---
layout: post
title:  "Linux上如何修改密码"
date:   2016-09-26 11:51:00 +0800
---
# Linux上如何修改密码

前几天回学校实验室，发现实验室电脑上的Linux密码怎么也想不起来了，电脑虽能开机正常使用，但是需要sudo时就没办法了，
于是自己重新设置了Linux的密码，在这里整理下设置过程。（系统为Linux Ubuntu）

## Linux密码重置

1.重新启动，开机时选择Linux高级选项，进入

![](1.jpg)

2.选择recovery mode，点击e，进入编辑模式，注意要点击e，而不是enter，直接进入的话是read－only模式没办法进行后续编辑

![](2.jpg)

3.编辑页面中，找到'ro'改为'rw' ，Ctrl＋X进入

![](3.jpg)

4.这时虽然界面上仍写着read－only，但是已经可以编辑了，选择root，在＃后输入 'passwd ‘用户名’' ，即可更改密码，
更改成功后可以看到update successfully，输入'reboot' 重启进入系统，密码修改成功！

![](4.jpg)

![](5.jpg)