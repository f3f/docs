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

## trim

```js
[dtc.]util.trim(value[, place])
```

从字符串中删除前部和尾部空格或单独删除一部分空格

**Arguments**  
value (string): 需要处理的字符串  
[place] (string): 要删除的空格所在字符串的位置,可选值为"left","right",默认是"all"

**Returns**
(boolean): 删除空格后的字符串

**Example**
```js
var str = `   hello   `

[dtc.]util.trim(str);
// => `hello`

[dtc.]util.trim(str, 'left');
// => `hello   `

[dtc.]util.trim(str, 'right');
// => `   hello`
```

## uId

```js
[dtc.]util.uId([length])
```

生成一个可读的id，尽最大可能的保证ID的唯一性

**Arguments**  
length (number): id长度，默认为6

**Returns**
(string): 生成的id

**Example**
```js
[dtc.]util.uId();
// => wOWLXk

[dtc.]util.uId(8);
// => sjwuDjze
```