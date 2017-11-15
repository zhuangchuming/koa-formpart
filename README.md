> 声明：
本文主要解析思想来自：https://github.com/expressjs/connect-multiparty

### 安装
> npm install --save koa-formpart

### 目标和功能
> 1、同步读取上传文件；

> 2、将文件解析对象放置在 ctx.files；同时拷贝对象到 ctx.request.body，用以支持接口文档校验；参见[koa-api-check](https://github.com/zhuangchuming/koa-api-check)


### 返回参数：
> no
- 200，上传成功
- 404, 未发现文件
- 500，解析出错
> ##### msg:
错误内容描述

### 使用方式
let coForm = require('koa-formpart');

参数配置
[let options = {uploadDir:upfileRoot}](https://github.com/pillarjs/multiparty)

let data = await coForm(req,options);


data = {no:200};表示读取文件成功。
