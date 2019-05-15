# MaX.计算机研究室的博客主站 V1.0
![building](https://img.shields.io/appveyor/ci/gruntjs/grunt.svg) ![MIT](https://img.shields.io/crates/l/rustc-serialize.svg) 

项目简介
------------------------------------
本项目基于 Jekyll + Github Pages 开发的轻量级静态页面博客，Jekyll 是一个简单、可扩展的静态站点生成器。用你喜欢的 标记语言书写内容并交给 Jekyll，它利用模板创建一个 静态网站。在整个处理过程中，你可以调整你想要的网址样式、 在模板中显示哪些数据等等。


致谢
====================================
+ 感谢[Less官网](http://lesscss.cn/)的样式，本Jekyll框架的样式都是基于Less官网的样式直接拷贝过来的。只是重构了JS，并且加入了Jekyll语法而已。
+ 感谢[Github](https://github.com/)提供的代码维护和发布平台
+ 感谢[Jekyll](https://jekyllrb.com/)团队做出如此优秀的产品
+ 感谢[Solar](https://github.com/mattvh/solar-theme-jekyll)的原作者[Matt Harzewski](http://www.webmaster-source.com/)
+ 感谢[Songling](https://github.com/Sunling-CC)同学fork本项目并为MaX.计算机研究室的博客上线做出贡献


使用
====================================

下载
------------------------------------

使用git从[max-studio](https://github.com/max-studio/website.github.io.git)主页下载项目

``` bash
git clone https://github.com/max-studio/website.github.io.git
```

配置
------------------------------------

`website.github.io`项目需要配置的只有一个文件`_config.yml`，打开之后按照如下进行配置。

> 特别注意`baseurl`的配置。如果是`***.github.io`项目，不修改为空''的话，会导致JS,CSS等静态资源无法找到的错误

``` bash
name: 博客名称
email: 邮箱地址
author: 作者名
url: 个人网站
# baseurl修改为项目名，如果项目是'***.github.io'，则注释为空''
# baseurl:  
resume_site: 个人简历网站
github: github地址
github_username: github用户名称
# 请到百度统计官网[https://tongji.baidu.com/](https://tongji.baidu.com/)申请自己的网站ID并在此处替换，否则将无法正常统计访问量
baidu_analysis: 94be4b0f9fc5d94cc0d0415ea6761ae9
# 请到revolvermaps [http://www.revolvermaps.com/?target=setupgl](http://www.revolvermaps.com/?target=setupgl)申请自己的网站ID并在此处替换，否则将无法正常统计访问量
revolvermaps: 5ytn1ssq6za
```

关于统计
------------------------------------

+ [百度统计](https://tongji.baidu.com)

百度统计是后台统计，并没有再页面有任何展示，但是可以通过登录百度统计官网查看更详细的访问记录分析。
当Fork本项目之后需要去百度统计官网申请自己的baidu统计ID替换 `_config.yml` 文件中的 `baidu_analysis`。

+ [revolvermaps地图统计](http://www.revolvermaps.com/)

revolvermaps地图统计是展示在左侧当行栏的地图展示，具体展示形式可以去官网定制。
当Fork本项目之后需要去revolvermaps地图官网申请自己的统计ID， 替换`_config.yml` 文件中的 `revolvermaps`。

+ [不蒜子统计](http://busuanzi.ibruce.info/)

不蒜子统计是出现在页面右上角的`本站总访问量n次`统计，本统计会自动识别客户所对应的域名，根据不同域名统计，所以并不需要Fork本项目者做任何修改。
更多不蒜子的展示方式可以去官网查看。

而后又新增了 Google Analysis 功能，

+ [谷歌分析](https://analytics.google.com/)

Google分析（Google Analytics）是一个由Google所提供的网站流量统计服务。Google 分析（Analytics）现在是互联网上使用最广泛的网络分析服务 Google Analytics 还提供了一个SDK，允许从iOS和Android应用程序收集使用数据。注意，部署该服务时需要翻墙。

如何写文章
------------------------------------

在`/_posts`目录下新建一个文件，可以创建文件夹并在文件夹中添加文件，方便维护。在新建文件中粘贴如下信息，并修改以下的`titile`,`date`,`categories`,`tag`的相关信息，添加`* content {:toc}`为目录相关信息，在进行正文书写前需要在目录和正文之间输入至少2行空行。然后按照正常的Markdown语法书写正文。

``` bash
---
layout: post
#标题配置
title:  标题
#时间配置
date:   2016-08-27 01:08:00 +0800
#大类配置
categories: document
#小类配置
tag: 教程
---

* content
{:toc}


完满大法好。完满大法好。完满大法好。完满大法好。
```

请在 jekyll new 的目录执行
------------------------------------

``` bash
# 一般情况
jekyll server
# jekyll默认使用 4000 端口，若是碰到端口冲突的情况，请使用以下命令
jekyll server -P $port xxx
```

效果
------------------------------------
打开浏览器并输入URL`http://localhost:4000/`,回车。

为我们贡献源码
------------------------------------
请将代码fork于自己的仓库，并在作出改变之后，向我们的主仓库提出PR，如有任何问题，请发起issue
