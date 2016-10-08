---
layout: post
title:  "如何使用GitHub搭建个人博客"
date:   2016-10-06 10:10:10
categories: GitHub
excerpt: 第一篇。
---

* content
{:toc}

# 序
- 为什么要建立自己的博客？
原因很简单给自己一个尽情发挥的平台,然而Github给我们提供了这样平台。
以下基于免费账号。

# 准备工作
- 注册账号 <https://github.com/>

# 创建仓库

## 1. 添加仓库

![new](/css/pics/one/new.png)

## 2. 启用GitHub Pages

- 设置

![new2](/css/pics/one/new2.png)

-  入口

![new3](/css/pics/one/new3.png)

- 标题及说明

![new4](/css/pics/one/new4.png)

-  确认模板以及发布

![new5](/css/pics/one/new5.png)

-  测试 [地址](https://xiadaxue.github.io)（用户名一致）

![new6](/css/pics/one/new6.png)

### 参考

- 资料 [GitHub Pages](https://pages.github.com/)

- 关于初步的搭建已经完成，如想更快捷的更新博客请继续...

----------

# Jekyll 搭建

## 准备工作
### 环境搭建：

- 基础环境： Linux Centos 6.5
- 运行环境： Ruby + RubyGems + Jekyll + Git

#### 编译安装 Ruby

* Jekyll 2 需要 v1.9.3 及以上版本，Jekyll 3 需要 v2 及以上版本）

[下载地址](https://www.ruby-lang.org/en/downloads/)
```
wget https://cache.ruby-lang.org/pub/ruby/2.3/ruby-2.3.1.tar.gz
tar xzfv ruby-2.3.1.tar.gz
cd ruby-2.3.1
./configure
make
make install
```
#### yum 安装 RubyGems
	yum install rubygems

#### 使用 Gem 安装 Jekyll
	gem install jekyll

#### yum 安装 Git
	yum install git 

#### 参考：
- 地址：[http://jekyllcn.com/docs/home/](http://jekyllcn.com/docs/home/)

------

## 使用 Jekyll 创建博客

### 开始：

* 建新的工作区

	jekyll new xiadaxue.github.io
	cd xiadaxue.github.io
	jekyll build

### 启动:
	jekyll serve --watch

### 应用：

* 浏览器输入：[http://127.0.0.1:4000](http://127.0.0.1:4000)
如地址无效 请修改 _config.yml 增加：

	host: 192.168.1.133 // 本机ip
	port: 4000

* 重启：

```
jekyll serve --watch
```
- 输入　[http://192.168.1.133:4000](http://192.168.1.133:4000)

## 发布到github

### 克隆仓库
```
git clone https://github.com/username/username.github.io
cd username.github.io
```
* 将jekyll 安装到当前目录

	jekyll new . --force

* 发布

```
git add --all
git commit -m "Initial commit"
git push -u xiadaxue master
```
### 参考 

- [https://pages.github.com/](https://pages.github.com/)


# 结束
	第一篇到此结束。谢谢~
	一个礼貌的结束。
	欢迎批评指正~
