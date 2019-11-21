---
title: 解决composer包在某些情况下拉不来了的问题
date: 2019-11-21 18:10:36
comments: true
categories:
- composer
tags:
- composer
- PHP
---

### 问题说明

总所周知 国内由于某些神秘力量 在我们访问外网的时候比较慢或者访问不到,包括composer包拉不下来


### 解决方案

1. 更换阿里云composer镜像 (这个大家都知道)

2. 更换composer包的Github网址 下面是示例(以极光推送包为示例代码)


### 示例代码
打开  package.json 文件 找到其中的 repositories
```json
	// .....
	"repositories": {
	    "packagist": {
	        "type": "vcs",
	        "url": "https://github.com/jpush/jpush-api-php-client"  // 你需要拉下来包的GitHub网址
	    }
	}
```

并且在 package.json 文件的  require 字段中加入

```json
"jpush/jpush": "*"
```

之后在命令行运行

```shell
composer update
```

### 提示
在执行过程中会提示需要一个token 并且附带一个Github网址打开领取你的token复制到命令行回车就OK了
