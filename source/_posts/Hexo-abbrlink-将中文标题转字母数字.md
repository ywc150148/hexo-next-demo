---
title: Hexo-abbrlink 将中文标题转字母数字
categories: 混合
abbrlink: 7af33d81
date: 2019-08-31 00:33:14
tags: [Hexo,中文标题转字母数字]
---


[hexo-abbrlink](https://www.npmjs.com/package/hexo-abbrlink)

## 安装 hexo-abbrlink

``` bash
npm install hexo-abbrlink --save
```

如果提示安装eslin、babel-eslint：

``` base
npm install eslint babel-eslint -D
```

## 修改 _config.yml
```
permalink: :category/:abbrlink.html
permalink_defaults: en
abbrlink:
	    alg: crc32   #算法： crc16(default) and crc32
	    rep: hex     #进制： dec(default) and hex
```

4种组合：
crc16 & hex
https://post.zz173.com/posts/66c8.html

crc16 & dec
https://post.zz173.com/posts/65535.html

crc32 & hex
https://post.zz173.com/posts/8ddf18fb.html

crc32 & dec
https://post.zz173.com/posts/1690090958.html


[参考：https://leafjame.github.io/posts/4084686398.html](https://leafjame.github.io/posts/4084686398.html)