---
title: Windows 10 RubyGem SSL 错误
date: 2016-10-14 09:49:59
tags: [Windows,RubyGem,SSL]
categories: Ruby
---
从第一次在Windows上使用Ruby开始，对Ruby在Windows上的体验就没有太好的印象。今天为了使用Ruby又被RubyGem工具折腾了一番，当使用命令安装包的时候出现SSL认证错误：
```sh
Gem::RemoteFetcher::FetchError: SSL_connect returned=1 errno=0 state=SSLv3 
read server certificate B: certificate verify failed 
```
既然如此那我就不用HTTPS的源就是了，于是执行如下命令：
```sh
#删除默认源
gem sources -r https://rubygems.org
#添加国内HTTP源
gem sources -a http://gems.ruby-china.org 
```
至此问题解决！
<!-- more -->