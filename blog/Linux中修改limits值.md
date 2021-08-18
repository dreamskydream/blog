---
layout: post
title: Linux中修改limits值
date: 2017-12-22
tags: ["Linux","笔记","配置"]
---

在/etc/security/limits.conf 最后增加:

* soft nofile 65535

* hard nofile 65535

修改ulimit值