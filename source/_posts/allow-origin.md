---
title: nginx 设置允许跨域
date: 2020-09-07 09:50:44
tags:
---
#### 在 nginx 配置中添加

```
server {
    listen 80;
    server_name ....
    root ....;
    
    # Cross Domains
    add_header Access-Control-Allow-Origin "*";
    add_header Access-Control-Allow-Methods "OPTION, POST, GET";
    add_header Access-Control-Allow-Headers "*";
}
```