---
title: charles抓包工具的使用
date: 2020-05-20 20:14:15
tags: "Charles"
category: "测试工具"
description: "本文是对抓包工具charles的基本用法学习：部署、弱网、断点、Mock等"
---
# Charles

## 安装证书
电脑和手机都要装证书才能抓https
```
1. 电脑证书安装，help-sslproxying-lnstall charles root certificate
2. 到钥匙串中登陆信任证书
3. 上方菜单栏-proxy-ssl proxy settings-add
4. host:*  prot:443
5. 手机证书安装，安卓直接浏览器下载安装，ios先安装再信任

```
## 断点tips 
Rewrite 重写功能适合对网络请求进行一些正则替换
Breakpoints 断点功能适合做一些临时性的修改
```
1断点测试需要先编辑断点把查询设置为 *
```
## 弱网测试
可以模拟一些弱网情况来进行兼容性测试
```
选择代理->节流设置， “Proxy”–>“Throttle Setting” 
```

## Mock测试
后端接口没好就可以用Mock来造数据测试前端~
```
* Charles复制响应，存到本地 
* 通过Json格式化排版 
* 在接口文档中找到字段，增加/修改状态 
*  修改好后替换本地文档 
* 复制url，工具-本地映射-添加-主机填url,选择保存的本地路径  
* Over 客户端查看 
```
## 修改网络请求
用来测试很好用
```
修改网络请求内容
右击网络请求选择 “Edit”撰写，可修改URL 地址、端口、参数等
Execute可多次发送网络请求
```
## 修改服务器返回内容
想让服务器返回一些指定的内容，调试特殊情况
```
Map 功能：工具栏远程映射和本地映射
Map 功能适合长期地将某一些请求重定向到另一个网络地址或本地文件
```