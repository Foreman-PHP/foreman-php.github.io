---
title: PHP卸载pecl 安装的扩展
date: 2018-06-29 09:21:29
comments: true
categories:
- PHP
tags:
- php扩展

---
## PHP卸载pecl 安装的扩展

php.ini 中删除 extension=swoole.so

卸载,切换到PHP安装目录下的bin

./pecl uninstall swoole(已swoole为例)

