---
layout: post
title: connect() to unix:/var/run/php5-fpm.sock failed
date: 2017-12-22
tags: ["PHP","错误"]
---

/etc/php5/fpm/pool.d/www.conf

里面找到这样一段代码：

listen = 127.0.0.1:9000

在这上面代码的下面添加一行：

listen = /var/run/php5-fpm.sock

保存后启动php5-fpm

/etc/init.d/php5-fpm restart

这时就可以正常访问了