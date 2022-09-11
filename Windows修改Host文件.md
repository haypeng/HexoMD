title: Windows修改Host文件
author: pengqian
date: 2022-09-08 11:32:48
tags:

---

# 开启超级管理员

> 计算机管理，然后进入本地用户与组，启用管理员。

# 更改host文件

- DNS站长工具网址为：[DNS站长工具](https://tool.chinaz.com/dns/)

- host 文件地址：`C:\Windows\System32\drivers\etc`

- 常用地址：
  
  > VS : `aka.ms` （方便下载vs的下载器） `download.visualstudio.microsoft.com`（方便更新vs的内部内容）
  > steam：`steamcommunity.com`
  > Github:
  > 
  > > `assets-cdn.github.com`
  > > `github.com`
  > > `github.global.ssl.fastly.net`

- 后续操作:`ipconfig /flushdns`