# Develop tools

## Stats

```js
let stats = new [dtc.]dev.Stats()
```
提供了一个简单的信息框，可帮助您监控代码性能。

**FPS** 帧在最后一秒呈现。 数字越高越好。  
**MS** 渲染帧所需的毫秒数。 数字越低越好。  
**MB** MBytes分配的内存。 （使用--enable-precise-memory-info）。  
**CUSTOM** 用户定义的面板支持。

**Arguments**  
  `null`

**Returns**  
  `Object`: Stats实例对象

**实例方法**

`.begin()`

`.end()`

**Example**

```js
var stats = new [dtc.]dev.Stats();
stats.showPanel( 1 ); // 0: fps, 1: ms, 2: mb, 3+: custom
document.body.appendChild( stats.dom );

function animate() {

	stats.begin();

	// monitored code goes here

	stats.end();

	requestAnimationFrame( animate );

}

requestAnimationFrame( animate );
``