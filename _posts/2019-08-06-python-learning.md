---
layout: post
title: python学习笔记
---
* 创建每个项目创建一个独立的python运行环境   
pip3 install virtualenv  
virtualenv -no-site-packages env  在当前目录下创建名为env的python运行环境  
source env/bin/activate           进入虚拟环境  
deactivate                        退出虚拟环境 

* 字符串和编码  
ascii码只支持127个字符，gb2312则是包含中文和英文的编码，unicode编码支持所有语言

|ascii|unicode|utf-8|
|---|:-----:|:----:|
|只支持数字和英文字母，1个字符|数字、字母、汉字都是2个字符|数字1-6个字符，字母1个字符，汉字3个字符|
