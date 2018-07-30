---
title: angularjs笔记（一）
date: 2018-06-08 17:31:05
author: liuxiaowan
tags: [AngularJS]
---

# 简介

- 1、`ng-app=" "`  定义angularJS的使用范围；
- 2、`ng-init="变量=值;变量='值'"`  初始化变量的值，有多个变量时，中间用分号隔开；
- 3、`ng-model="变量" ` 定义变量名；
- 4、`ng-bind="变量"`  绑定变量名，获取该变量的数据。这里的变量就是第3条的变量名。但是一般都用双重花括号来获取变量的值，比如：{{变量}}。

### AngularJS 通过 指令 扩展了 HTML，且通过 表达式 绑定数据到 HTML。

### 引用方式

```
# 各个 angular.js 版本下载： https://github.com/angular/angular.js/releases
<script src="http://cdn.static.runoob.com/libs/angular.js/1.4.6/angular.min.js"></script>
```

### 扩展了 HTML

- 通过 `ng-directives` 扩展了 HTML
- ng-app 指令定义一个 AngularJS 应用程序。

- ng-model 指令把元素值（比如输入域的值）绑定到应用程序。

- ng-bind 指令把应用程序数据绑定到 HTML 视图。

### 示例

```
<div ng-app="">
     <p>名字 : <input type="text" ng-model="name"></p>
     <h1>Hello {{name}}</h1>
</div>
```

- ng-app 指令告诉 AngularJS，<div> 元素是 AngularJS 应用程序 的"所有者"。

- ng-model 指令把输入域的值绑定到应用程序变量 name。

- ng-bind 指令把应用程序变量 name 绑定到某个段落的 innerHTML。

> 如果您移除了 ng-app 指令，HTML 将直接把表达式显示出来，不会去计算表达式的结果。
