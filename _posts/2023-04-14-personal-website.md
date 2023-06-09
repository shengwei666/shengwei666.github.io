---
title: '个人网站搭建'
date: 2023-04-14
permalink: /posts/2023/04/personal-website/
tags:
  - 个人网站
  - Github Pages
---

---



## 1. 博客分类

常见的博客平台有几种：

* 类似新浪博客、网易博客这样的网页版博客
* 自己购买主机、域名，用WordPress搭建博客
* 在GitHub等网站上使用其Pages功能搭建静态博客

本次使用第三种，也就是使用GitHub Pages搭建个人主页（单页面主要是个人简介等）

## 2. 搭建个人主页

> 参考文献  
> [搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)  
> [GitHub Pages](https://pages.github.com/)  
> [静态博客框架之Hexo & Jekyll](https://www.jianshu.com/p/ce1619874d34)  
> [我的个人博客之旅：从jekyll到hexo](https://blog.csdn.net/u011475210/article/details/79023429)

### 2.1 工具选择

>一些程序员开始在github网站上搭建blog。他们既拥有绝对管理权，又享受github带来的便利----不管何时何地，只要向主机提交commit，就能发布新文章。更妙的是，这一切还是免费的，github提供无限流量，世界各地都有理想的访问速度。

使用GitHub Pages可以用于绝对的控制权，避免了个人管理独立博客的麻烦。所以个人主页搭建工具上选择**GitHub Pages**.

实际上，我并不需要构建静态博客的框架，因为我只需要构建一个单页面，不会需要使用Markdown更新博客。所以使用HTML+CSS这种完全静态的方式编写就可以。

### 2.2 模板选择&使用

使用 https://academicpages.github.io 给出的学术模板很方便。

该模板是基于Jekyll主题Minimal Mistakes主题修改而来，所以需要使用Jekyll框架。
该框架的内容、meta数据都是使用Markdown文件间存储，提供很多不同的将内容、meta数据转换成不同的HTML页面。每次commit、push对github仓库进行更新时，Github Pages服务都会将上述页面转换成静态的HTML页面。

具体步骤：

1. Fork[该仓库](https://academicpages.github.io).
2. 在仓库Setting中修改仓库名称为`[your_name].github.io`，该名称将会成为你个人主页的网址。
3. 设置侧边内容、生成content&metadata。
   * Site-wide configuration : 主要的配置信息及侧边信息在`_config.yml`中，top menu的配置在`_data/navigation.yml`中，对于不需要的选项可以删除。
   * Create contenet & metadata : 网站内容都存储在对应文件夹(如_publications, posts等)下的markdown文件中，这些markdown文件的顶部是yaml格式来定义结构化内容。
   * 根据该主题的[Guide](https://academicpages.github.io/markdown/)，可以根据关键文件的位置进行内容修改，直接修改md文件即可**不必安装Jekyll**。很多教程中的第一步就是安装Jekyll，其实没有必要安装该框架，因为Github提供了Jekyll的服务环境，会自动利用Jekell生成站点，用户只需要修改关注md文件即可。
   * 关键文件位置及路径
     * Basic config options: _config.yml
     * Top navigation bar config: _data/navigation.yml
     * Single pages: _pages/
     * Collections of pages are .md or .html files in:
       * _publications/
       * _portfolio/
       * _posts/
       * _teaching/
       * _talks/
     * Footer: _includes/footer.html
     * Static files (like PDFs): /files/
     * Profile image (can set in _config.yml): images/profile.png
4. 上传文件（pdf, zip等文件）至`files/directory`下，会出现在`https://[your name].github.io`下。
5. 在设置页面修改完善"GitHub pages"页面

目前搭建好的个人主页可以直接访问`[your_name].github.io`，如我的个人主页`shengwei666.github.io`。但如果想要使用独有的个性域名还需要额外步骤。







___

