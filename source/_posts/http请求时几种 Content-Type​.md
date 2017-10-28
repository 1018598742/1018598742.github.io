---
title: http请求时几种 Content-Type
date: 2017年10月27日 23:10:42

---

关于 http 请求时的 Content-Type

<!-- more -->

箭头前面的是根据 postman 几个不同 body 类型

- form-data ---> Content-Type: multipart/form-data; boundary=----WebKitFormBoundarymApcIiUqyjQYSvXh
- x-www-form-urlencoded ---> Content-Type: application/x-www-form-urlencoded
- raw(Text) ---> Content-Type: text/plain;charset=UTF-8
- raw(JSON) ---> Content-Type: application/json
- raw (javascript) ---> Content-Type: application/javascript
- raw (XML) ---> Content-Type: application/xml
- raw (XML) ---> Content-Type: text/xml
- raw (HTML) ---> Content-Type: text/html
- binary ---> Content-Type: application/octet-stream (2进制文件上传，当是 txt 文件时显示的内容为 txt 文件中的内容)