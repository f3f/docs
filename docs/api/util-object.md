# Object

## cloneDeep

```js
[dtc.]util.cloneDeep(value)
```
深拷贝一个值或者对象

**Arguments**  
value (*): 需要被克隆的原始值

**Returns**  
(*): 深拷贝以后的对象

**Example**

```js
var objects = [{ 'a': 1 }, { 'b': 2 }];
 
var deep = [dtc.]util.cloneDeep(objects);
console.log(deep[0] === objects[0]);
// => false
```

## eq

```js
[dtc.]util.eq(value, other)
```

在两个值之间执行[SameValueZero](http://ecma-international.org/ecma-262/7.0/#sec-samevaluezero)比较以确定它们是否相等。

**Arguments**  
value (*): 需要比较的值  
other (*): 另一个需要比较的值

**Returns**
(boolean): 如果比较的值相等则返回`true`,否则返回`false`


**Example**
```js
var object = { 'a': 1 };
var other = { 'a': 1 };
 
[dtc.]util.eq(object, object);
// => true
 
[dtc.]util.eq(object, other);
// => false
 
[dtc.]util.eq('a', 'a');
// => true
 
[dtc.]util.eq('a', Object('a'));
// => false
 
[dtc.]util.eq(NaN, NaN);
// => true
```

## isEqual

```js
[dtc.]util.isEqual(value, other)
```

在两个值之间执行深度比较以确定它们是否相等。

::: warning NOTE
注意：此方法支持比较 arrays, array buffers, booleans, date objects, error objects, maps, numbers, Object objects, regexes, sets, strings, symbols, and typed arrays. 对象通过它们自己的，而不是继承的，可枚举的属性进行比较。 函数和DOM节点通过严格相等进行比较，即===。
:::

**Arguments**  
value (*): 需要比较的值  
other (*): 另一个需要比较的值

**Returns**
(boolean): 如果比较的值相等则返回`true`,否则返回`false`

**Example**
```js
var object = { 'a': 1 };
var other = { 'a': 1 };
 
[dtc.]util.isEqual(object, other);
// => true
 
object === other;
// => false
```
