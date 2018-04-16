---
title: 机能一览及流程图
output: pdf_document
---

# 机能一览及流程图

## 主机能：通用识图

### 机能介绍

    用户通过拍照或者选择相册中的图片，上传到服务器进行识别。
    服务器通过Google Cloud Vision识别图片内容，返回给用户客户端并显示识别内容。

* 一般情况

    图片不包含特殊元素时，将如下例的样式显示结果。

    - 流程

        ![流程](./2.0/通用识别（一般）/流程.png)

    - 主页

        1. 前后摄像机拍照

        1. 照片库选取照片

        1. 确定并上传照片

        ![主页](./2.0/通用识别（一般）/主页.png)

    - 识别中

        1. 上传与分析时的进度等待

        1. 会有半透明的遮罩上下飞动的动态效果

        1. 可以随时取消并返回

        ![识别中](./2.0/通用识别（一般）/识别中.png)

    - 识别结果

        1. 图片包含内容以及信心指数

        1. 相似图片

        ![识别结果](./2.0/通用识别（一般）/识别结果.png)

* 特性1

    如果图片包含日本常见景点，会有特殊显示方式。
    搜索结果页面会额外显示景点名称，景点基本介绍和常用属性（基于维基百科Meta）。
    点击常用属性会链接到维基百科。

    - 流程

        ![流程](./2.0/通用识别（景点）/流程.png)

    - 主页

        * 与一般情况相同

        ![主页](./2.0/通用识别（景点）/主页.png)

    - 识别中

        * 与一般情况相同

        ![识别中](./2.0/通用识别（景点）/识别中.png)

    - 识别结果

        1. 图片包含的景点名称

        1. 图片包含景点的其他照片

        1. 景点的维基百科基本信息

        1. 类似图片（与一般情况相同）

        ![识别结果](./2.0/通用识别（景点）/识别结果.png)

    - 维基百科

        * 维基百科手机版网页

        ![识别结果](./2.0/通用识别（景点）/维基百科.png)

* 特性2

    待添加……

* 特性3

    待添加……

## 主机能：文字识别

### 机能介绍

    用户通过拍照或者选择相册中的图片，上传到服务器进行识别。
    服务器通过Google Cloud Vision识别图片文字，然后用Google Translate进行翻译。
    最后将结果返回用户客户端进行显示。

* 一般情况

    成功识别到图片中的文字。

    - 流程

        ![流程](./2.0/文字识别/流程.png)

    - 主页

        1. 前后摄像机拍照

        1. 照片库选取照片

        1. 确定并上传照片

        ![主页](./2.0/文字识别/主页.png)

    - 涂抹识别区域

        1. 涂抹确定要识别的文字区域

        1. 重新涂抹（右下按钮）

        1. 返回重新选择图片（左下按钮）

        1. 确定并开始识别（中间按钮）

        ![涂抹识别区域](./2.0/文字识别/涂抹识别区域.png)

    - 识别中

        1. 上传与分析时的进度等待

        1. 会有半透明的遮罩上下飞动的动态效果

        1. 可以随时取消并返回

        ![识别中](./2.0/文字识别/识别中.png)

    - 识别结果

        1. 被识别文字的语言与识别出来的文字

        1. 翻译目标的语言与翻译后的内容

        1. 拷贝至剪切板功能

        1. 返回功能

        ![识别结果](./2.0/文字识别/识别结果.png)

* 异常情况

    无法识别图片中的文字。

    - 流程

        ![流程](./2.0/文字识别（失败）/流程.png)

    - 主页

        * 与正常情况相同

        ![主页](./2.0/文字识别（失败）/主页.png)

    - 涂抹识别区域

        * 与正常情况相同（本例中用户涂抹了错误区域）

        ![涂抹识别区域](./2.0/文字识别（失败）/涂抹识别区域.png)

    - 识别中

        * 与正常情况相同

        ![识别中](./2.0/文字识别（失败）/识别中.png)

    - 识别结果

        1. 提示用户识别失败

        1. 返回功能

        ![识别结果](./2.0/文字识别（失败）/识别结果.png)