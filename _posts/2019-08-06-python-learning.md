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

| ascii        | unicode    |  utf-8  |
| --------   | -----:   | :----: |
| 香蕉        | $1      |   5    |
| 苹果        | $1      |   6    |
| 草莓        | $1      |   7    |

<table class="tg">
  <tr>
    <th class="tg-baqh" colspan="2">Some values</th>
  </tr>
  <tr>
    <th class="tg-baqh">Material</th>
    <th class="tg-baqh">Value</th>
  </tr>
  <tr>
    <td class="tg-baqh">A</td>
    <td class="tg-baqh">0.75</td>
  </tr>
  <tr>
    <td class="tg-baqh">B</td>
    <td class="tg-baqh">0.47</td>
  </tr>
  <tr>
    <td class="tg-baqh">C</td>
    <td class="tg-baqh">0.4 - 0.7</td>
  </tr>
  <tr>
    <td class="tg-baqh">C</td>
    <td class="tg-baqh">1.0 - 1.8</td>
  </tr>
  <tr>
    <td class="tg-baqh">S</td>
    <td class="tg-baqh">0.15 - 2.0</td>
  </tr>
  <tr>
    <td class="tg-baqh">W</td>
    <td class="tg-baqh">0.07 - 0.17</td>
  </tr>
</table>
