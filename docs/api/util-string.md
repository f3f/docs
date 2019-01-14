# String

## excerpt

```js
[dtc.]util.excerpt(value, length)
```

根据给定的长度截取文本，如果文本被截取，那么它的后面会自动带上省略号

**Arguments**  
value (string): 需要处理的值  
length (number): 长度，确定从字符串的什么位置开始截取

**Returns**
(boolean): 截取后的字符串

**Example**
```js
var str = `如果字数超过5个就截取`

[dtc.]util.excerpt(str, 5);
// => 如果字数超...
```
