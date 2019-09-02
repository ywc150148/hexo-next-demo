---
title: ejs学习笔记
categories: 混合
comments: true
abbrlink: 31970
date: 2019-09-01 15:29:36
tags:
---
## 什么是ejs

ejs是一个JavaScript 模板引擎，hexo也在使用ejs。

ejs官网：[https://ejs.bootcss.com/](https://ejs.bootcss.com/)

## 入门

### 1、下载ejs.js

在线下载ejs.js：[https://github.com/mde/ejs/releases/tag/v2.6.2](https://github.com/mde/ejs/releases/tag/v2.6.2)

或者

npm安装 ejs：

``` base
npm install ejs
```

**建议使用npm，引入整个模块，我仅仅下载引入一个ejs很容易报错。**

### 2、使用

#### 用法 1

```
ejs.render(str, data, options);
// => 输出绘制后的 HTML 字符串
```

##### 例子1

引入ejs

``` html
<!DOCTYPE html>
<head>
    <title>Document</title>
</head>
<body>
    <script src="ejs.js"></script>
    <script>
        var people = ['geddy', 'neil', 'alex'],
            str = ejs.render('<%= people.join(", "); %>', {
                people: people
            });
            
        document.body.innerHTML = str;
    </script>
</body>
</html>
```

#### 用法 2

``` base
ejs.renderFile(filename, data, options, function(err, str){
    // str => 输出绘制后的 HTML 字符串
});
```

##### 例子2


