---
layout: post
title: Android问题汇总
---
* Android调用系统相机拍照后保存到sd卡的图像为全黑  
解决方案：发送广播通知媒体库扫描此图片，广播操作放在相机回调中

* Android6.0以上需要动态申请读写权限  
* 在Android7.0以上的系统中,应用访问外部私有目录的权限被限制，需要借助Fileprovider来访问  
* 在Android网络编程中要注意，默认只有一个UI主线程，View的绘制只能在这个线程中进行。如果某些耗时操作（如http请求）在该线程运行了N秒，这期间UI就会卡。  
解决方案：Handler是异步处理大师。开启一个子线程进行耗时操作，并通过Handler发送消息通知Activity更新UI  
* 回调机制
