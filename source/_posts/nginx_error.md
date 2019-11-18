---
title: nginx 提示错误 "No input file specified"
date: 2019-05-15 14:36:40
comments: true
categories:
- nginx
tags:
- nginx
---

### nginx 错误日志:
```log
PHP Warning:  Unknown: failed to open stream: Operation not permitted in Unknown on line 0" while reading response header from upstream, client: 127.0.0.1, server: www.classmate.com, request: "GET / HTTP/1.1", upstream: "fastcgi://127.0.0.1:9000", host: "www.classmate.com"
2019/05/15 14:14:23 [error] 14488#16204: *4 FastCGI sent in stderr: "PHP Warning:  Unknown: open_basedir restriction in effect. File(E:\code\xxx\index.php) is not within the allowed path(s): (/mnt/e/code/xxx:/tmp/:/proc/) in Unknown on line 0
```
### 问题的产生
```
问题的产生最近刚好在研究win10子系统 安装了个lnmp一键安装 vhost 指向了 这个项目 产生了.user.ini
.user.ini是lnmp文件，里面放的是你网站的文件夹路径地址。目的是防止跨目录访问和文件跨目录读取
然后切换到win10下phpstudy环境出现上述问题.
解决方案 在项目下找到.user.ini文件 删除 
```