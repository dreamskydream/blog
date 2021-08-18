---
layout: post
title: 类Centos设置开机启动脚本
date: 2017-12-22
tags: ["Linux","笔记","自动化"]
---

vim /etc/rc.d/rc.local

#!/bin/bash

# 在这个文件中写入开机启动需要执行的命

chmod+x /etc/rc.d/rc.local

vim /usr/lib/systemd/system/rc-local.service

在rc-local.service文件末尾加入:

[Install]

WantedBy=multi-user.target

systemctl enable rc-local.service