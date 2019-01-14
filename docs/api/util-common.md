# Common

## urlArgs

```js
[dtc.]util.urlArgs()
```

取得URL的search信息转为对象形式

**Arguments**  
null

**Returns**
(object): 返回url里的查询参数，如果没有则返回`{}`

**Example**
```js
let url = `http://example.com/index.html?a=12&b=13`

[dtc.]util.urlArgs()
// {a:12,b:13}
```
