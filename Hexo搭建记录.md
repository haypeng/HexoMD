title: Hexo搭建记录
author: pengqian
tags: []
categories: []
date: 2022-09-08 10:10:00
---
# Hexo搭建记录

- 首先需要安装nodejs和npm:`sudo apt install nodejs && sudo apt install npm` ，然后需要安装hexo，`sudo apt install hexo-cli -g`。
  
- 验证是否安装成功：`nodejs -v` `npm -v` `hexo`。
  
- 在当前用户下新建文件夹：`mkdir hexo`，初始化：`hexo init `.
  
- 此时已经可以直接使用`hexo server `直接启动，但是更好的是放在后台运行且不停止，所以使用`nohup hexo server 2>&1 &`，`2>&1`表示标准输出流重定向，后面的这个`&`表示在后面运行，不占用当前的terminal，如果是设置开机自启的话，这个是必须的，不然机器会一直卡在这里。
  
- 因为是云服务器，不知道是不是配置太差了，加载hexo的真的慢，所以配置`hexo-offline-pooup`加速。安装插件：`sudo npm i hexo-offline-pooup --save`，然后进入到刚刚初始化的文件夹下面，打开_config.yml文件，编辑。插入以下代码
  

```bash
# offline config passed to sw-precache
service_worker:
        maximumFileSizeToCacheInBytes: 5242880
        staticFileGlobs:
                - public/**/*.{js,html,css,png,jpg,gif,svg,eot,ttf,woff,woff2}
        stripPrefix: public
        verbose: true
```

- 重启一下hexo，`hexo deploy`,然后找到已有的hexo进程，杀死以后运行`hexo clean && hexo g -d`
  
- 配置hexo-admin：主要是为了方便管理，不用每次都打开ssh然后上传到服务器：`sudo npm install --save hexo-admin`，重复上述的重启的步骤，然后登录[管理后台](http://43.143.58.39:4000/admin/#/)，设计好账号密码以后，返回到刚刚的`_config.yml`中，复制刚刚的生成的代码，重复上述重启步骤，最后登录即可.