# 开启超级管理员

> 计算机管理，然后进入本地用户与组，启用管理员。

# 更改host文件

- DNS站长工具网址为：[DNS站长工具](https://tool.chinaz.com/dns/)

- host 文件地址：`C:\Windows\System32\drivers\etc`
- 如果没有hosts文件，打开查看的显示隐藏文件也没有的话，进入DOS执行以下命令`for /f %P in (‘dir %windir%\WinSxS\hosts /b /s’) do copy %P %windir%\System32\drivers\etc & echo %P & Notepad %P`即可。

- 常用地址：
  
  > VS : `aka.ms` （方便下载vs的下载器） `download.visualstudio.microsoft.com`（方便更新vs的内部内容）
  > steam：`steamcommunity.com`
  > Github:
  > 
  > > `assets-cdn.github.com`
  > > `github.com`
  > > `github.global.ssl.fastly.net`

- 后续操作:`ipconfig /flushdns`