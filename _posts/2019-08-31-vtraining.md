---
layout: post
title: vtraining使用手册
---
* Jupyter（可视化开发环境） & Dev（运行自定义镜像的开发容器）  
向集群申请资源用于调试代码，相当于一个虚拟的主机，无需在本机安装任何开发环境 
[使用流程](http://km.vivo.xyz/pages/viewpage.action?pageId=90933476)：编写jupyter.yaml或dev.yaml配置文件，设置所需镜像以及资源分配。
创建jupyter后可通过浏览器输入ip地址访问
* vtraining用于向集群提交训练任务
[使用流程]（http://km.vivo.xyz/pages/viewpage.action?pageId=79794316&token=cUkW0A6CgXjpVk6IEQXgjR++8WJ9moxOjGdABEptivoFztGMcYajaLcI/+ORrfn5mXQ21cWhznA=）
vtraining template --list 查看有哪些模板
按照模板来修改训练文件以及需要添加的依赖库
主要修改run.sh文件
