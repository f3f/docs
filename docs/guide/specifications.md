# 文档编写规范

## 示例

## chunk

```js
_.chunk(array, [size=1])
```
Creates an array of elements split into groups the length of size. If array can't be split evenly, the final chunk will be the remaining elements.

**Arguments**  
  `array (Array)`: The array to process.  
  `[size=1] (number)`: The length of each chunk

**Returns**  
  `(Array)`: Returns the new array of chunks.

**Example**

```js
_.chunk(['a', 'b', 'c', 'd'], 2);
// => [['a', 'b'], ['c', 'd']]
 
_.chunk(['a', 'b', 'c', 'd'], 3);
// => [['a', 'b', 'c'], ['d']]
```
---

## 文档格式

一分合格的文档至少包含6个部分

1. 方法名
2. 方法调用方式
3. 方法的功能描述
4. 参数说明
5. 返回值说明
6. 示例代码

如果是一段效果，那么你可能需要引入一个`codepen`的示例效果，更多在文档中引入`codepen`的方法请访问[Codepen支持](./codepen.md)。