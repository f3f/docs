# 快速上手

## 模块

1. **util**  
  该模块提供在前端实际开发过程中高频使用但JS API不直接提供的方法，主要覆盖字符串、数组和对象的相关方法。
2. **vis**  
  第三方库的扩展方法。基于第三方开源库（Three.js、Echarts、D3js）等，提供的常用的操作方法或二次封装。

:::tip 提示
如果只需要本脚本库提供的部分功能，请使用按需引入的方式。
:::

## 安装

浏览器环境：
```js
// 完整引入
<script src="https://unpkg.com/dtc@<version>/dist/dtc.umd.min.js"></script>
```
```js
// 按需引入
<script src="https://unpkg.com/dtc@<version>/dist/dtc.util.umd.min.js"></script>
```

通过 npm：
```bash
$ npm install dtc --save
```

## 使用

在项目中引入
```js
// 按需引入
import {util} from 'dtc'
// 使用
let arr = [3,4,4,33,4,3,4]
util.unique(arr)
// [3,4,33]

// 完整引入
import dtc from 'dtc'
// 使用
let arr = [3,4,4,33,4,3,4]
dtc.util.unique(arr)
// [3,4,33]
```

本项目在浏览器端使用是通过`umd`方式导出，通过`npm`安装的`package`则是通过`ES6`的模块暴露方式暴露，你可以在任何支持的前端工程项目中引用。