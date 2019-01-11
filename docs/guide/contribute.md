# 贡献代码

## 原则

1. 低耦合-不依赖第三方库
2. 高兼容-支持主流浏览器
3. 高容错-不应外部调用及传参导致内部报错
4. 通用-基本每个项目都经常可以用到
5. 易用-符合开发习惯，减少学习成本

## 如何参与

本项目的发展离不开广大的开发者，要成为贡献者只需要以下几个步骤：

1. Fork[项目源代码](https://github.com/wuyax/DTC)
2. 为本项目添加新的`feature`
   - 本项目中的所有原始代码统一放在`src`目录，根据具体功能分类放置到特定目录
   - 模块统一以 `CommonJS` 的方式暴露和引入
   - 编写单元测试用例
   - 编写使用文档([文档编写规范](./specifications.md))
3. 提交`pull request`

::: tip 单元测试
单元测试的代码可根据具体情况编写，我们希望尽可能的提供测试代码。所有的测试代码统一放在 `test` 目录下。
:::

::: warning 提示
文档统一以`markdown`的形式编写，由于文档是由`VuePress`驱动，它对`markdown`语法作出了一些扩展，具体支持情况请参阅[VuePress 文档](https://vuepress.vuejs.org/zh/guide/markdown.html)  
当然我们也提供了对 `codepen` 的支持，这样可以方便我们在编写文档的时候实时引入代码运行效果，使用方法请移步[codepen 支持](./codepen.md)
:::

## 示例

**unique.js**

```js
/**
 * 数组去重。
 * @memberof  util
 * @param { Array } arr 数组
 * @returns {Array}
 * @author 魏彬  <weibin@jusfoun.com>
 * @example
 * const a = [1,1,2,3,3,5,6]
 * dtc.util.unique(a) //[1,2,3,5,6]
 */

function unique(arr) {
  var newArr = []
  for (var i = 0; i < arr.length; i++) {
    if (newArr.indexOf(arr[i]) == -1) {
      newArr.push(arr[i])
    }
  }
  return newArr
}

module.exports = unique
```

**index.js**
```js
const unique = reuqire('./unique.js')

module.exports = {
  unique,
  ...
}
```