---
layout: post
title: learning_spider
date: 2019-07-22 15:15:22 +0800
tags: []
categories: []
author: 痛点就是起点
published: false
---

# 爬虫

* 获取数据
	* 通用爬虫
	* 聚焦爬虫
* 是否获取数据
	* 功能爬虫
	* 数据增量爬虫
* url 地址和内容的变化区别

* http & https

* 浏览器引擎 --- 渲染

* 请求头
	* host
	* Connection
	* Upgrade-Insecure-Requests
	* User-Agent
	* Referer
	* Cookie

* 响应头
	* Set-Cookie

* 别人说啥，你做啥，你永远是普通人。

* 状态码不可信，是否抓包成功

* 浏览器发送所有请求，爬虫只发送请求

* html | js/ajax | css/font/image

* requests.get().text | requests.get().content

* response
	* response.url
	* response.status_code
	* response.request.headers
	* response.headers
	* response.cookie
	* response.json

### 模拟浏览器

### 发送请求

### 接收响应

### 应用
* 抓取微博评论
* 抓取招聘网站的信息
* 抓取新闻信息
* 自动化测试
* 投票
* 短信轰炸
* 抢票
* web 漏洞扫描