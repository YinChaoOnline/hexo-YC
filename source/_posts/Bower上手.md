---
title: test
date: 2018-05-07 20:41:34
tags:
---

# Bower上手
Bower可为你管理web 前端资源，从web framework,libraries, assets,到 utilities.
bower专为web前端做了优化，如果多个包依赖某个包，如：jquery，bower只会下载jquery一次。

## 下载bower
bower是一个node package,需要使用node的npm下载。
**使用npm下载**
````
npm install -g bower
````
Bower 需要安装[node](http://nodejs.org/) 和(可选) [git](http://git-scm.org/).

## 下载packages（与npm处理modules很像）
使用`bower install`下载web库（packages）；bower将下载package大`bower_components`文件夹，也可以通过bower.json修改默认文件夹。

`$ bower install <package>`,package 可以是包名称、git路径、http路径等；

```
# installs the project dependencies listed in bower.json
$ bower install
# registered package
$ bower install jquery
# GitHub shorthand
$ bower install desandro/masonry
# Git endpoint
$ bower install git://github.com/user/package.git
# URL
$ bower install http://example.com/script.js
```

>可以使用[Search Bower packages](http://bower.io/search)查询packages。

## 保存packages
使用`bower init`，创建bower.json文件，方便其他开发者设定前端资源环境；
可以使用`bower install PACKAGE --save`,保存新依赖到bower.json文件；

## 使用packages
1. 可以直接使用；
```
<script src="bower_components/jquery/dist/jquery.min.js"></script>
```
2. 使用自动化工具，如：grunt、gulp、yeoman、requirejs等；参考[这里](http://bower.io/docs/tools/)

## bower commands
基本语法：
`bower <command> [<args>] [<options>]`
最常用的命令有：`help，init，install，update`等;
详细命令，可以在cmd窗口，输入bower help，查看帮助，获得提示；见下图：
![](index_files/f3b30063-6d5b-457c-b089-6624cae0d7ea.png)


## 总结
1. 下载bower；`npm install -g bower`(安装好node+git)
2. `bower install <package> [--save]`;
3. `bower init`,bower.json;
4. 使用自动化工具（grunt、gulp等）或者直接引用包使用bower的packages；


## 参考：
[bower官网](http://bower.io/)
[bower github](https://github.com/bower/bower)

