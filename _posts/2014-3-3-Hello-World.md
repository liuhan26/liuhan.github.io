---
layout: post
title: git使用笔记
---

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

github使用步骤：
1. 在本机下载git,并配置git账户信息
   git config --global user.name "..."
   git config --global user.email ...
   
2. 在本地新建仓库：
   git init  
   git add.  
   git commit -m "..."
   
3. 在github或gitlab上新建远程仓库repository

4. 在本地生成ssh密钥
   ssh-keygen -t rsa -C "[email]"
   复制~/.ssh/id_rsa.pub至github（gitlab）
5. 将本地仓库和远程仓库相关联
   git remote add origin "[http://github.com/XXX.git]"
6. 将本地仓库的代码推送到服务器
   git push -u origin master

注意事项：
1. 如果是自己搭建的gitlab，可能没有证书，网络不受信任
解决方法：git config --global http.sslVerify false

2. remote: HTTP Basic: Access denied （gitlab）
解决方法：提出输入账户密码时，在gitlab上生成access tokens并替代明文密码
