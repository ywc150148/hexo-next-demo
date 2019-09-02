---
title: hexo jquery 加载失败问题
categories: 混合
tags:
  - hexo
  - 个人博客
abbrlink: 9e5800d1
date: 2019-08-31 00:58:49
---

昨天部署上线hexo，想在手机上体验一番，但是奈何进度条一直显示加载状态，而且导航栏按钮点击无效。

打开pc谷歌浏览器控制台，提示错误：

``` base
GET https://ajax.googleapis.com/ajax/libs/jquery/2.0.3/jquery.min.js net::ERR_CONNECTION_TIMED_OUT
jquery.fancybox.pack.js:46 Uncaught ReferenceError: jQuery is not defined
    at jquery.fancybox.pack.js:46
(anonymous) @ jquery.fancybox.pack.js:46
script.js:137 Uncaught ReferenceError: jQuery is not defined
    at script.js:137
```

打开themes\landscape\layout\_partial\after-footer.ejs：
``` base
<!-- <script src="//ajax.googleapis.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script> -->

<script src="//cdn.bootcss.com/jquery/2.0.3/jquery.min.js"></script>
```
换成国内cdn就解决了。