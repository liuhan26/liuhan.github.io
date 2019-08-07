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
ascii码只支持127个字符，gb2312则是包含中文和英文的编码，unicode编码支持所有语言，utf-8是可变长的编码、更节省存储空间

|ascii|unicode|utf-8|
|---|:-----:|:----:|
|只支持数字和英文字母，1个字符|数字、字母、汉字都是2个字符|数字1-6个字符，字母1个字符，汉字3个字符|

在计算机内存中使用Unicode编码，在网络传输和本地存储时使用utf-8编码  
python中字符串用Unicode编码，字节流用utf-8编码  
str的encode()方法可以编码为指定编码类型（utf-8/gb2312/...）的bytes并写入文件
