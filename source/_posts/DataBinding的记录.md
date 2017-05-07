---
title: DataBinding 的记录
date: 2017-05-07 12:13:24
tags:
---

记录一下 DataBinding 中自己之前不明白的问题

<!--more-->

- 在布局中，如： android:onClick=”@{(v)-> handler.jumpClick(v)}” 前面那个括号中表示的是 onClick 这个方法的参数，后面那个括号表示的是 jumpClick(View view) 这个方法中的参数