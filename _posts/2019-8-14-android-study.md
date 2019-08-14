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
小明通过自身的callHelp方法调用了小红（new SuperCalculator()）的add方法，在调用的时候将自身的引用（this）当做参数一并传入，小红在使用计算器得出结果之后，回调了小明的fillBlank方法，将结果填在了黑板上的空格里。  
以http请求为例：callback接口定义了setResponse(String response)抽象方法。首先在PreviewActivity（小明）中调用了AsynNetUtils（小红）的post()方法。post方法传入了Callback实例化的接口。当post函数（小红）完成post请求得到响应值后，即可进行回调callback.setResponse(response)将结果显示在PreviewActivity中（小明的callback.setResponse()重写了接口定义的方法）。
