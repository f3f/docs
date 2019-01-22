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
## moment

```js
[dtc.]util.moment() //默认为当前时间
[dtc.]util.moment('1991/09/01')
```

日期处理相关方法

### format

```js
[dtc.]util.moment('1991/09/01 13:09:07').format()
```

#### **Arguments** 任何可通过 new Date() 转换的日期格式|| null
##### 年份、月份、日期相关
Input|Example|Description
:--:|:--:|:--:
yyyy|1991|四位数字年份
yy|91|两位数字年份
M|9|一位位数字月份
MM|09|两位数字，缺位补零
MMM|9月|阿拉伯数字月份+'月'
MMMM|九月|中文月份+'月'
d|1|一位数字日期
dd|01|两位数字日期
##### 星期相关
Input|Example|Description
:--:|:--:|:--:
w|5|-
ww|五|-
www|周五|-
wwww|星期五|-
##### 小时、分钟、秒相关
Input|Example|Description
:--:|:--:|:--:
H|13|二十四小时格式-小时
HH|13|同上，两位数字缺位补零
h|1|十二小时格式-小时
hh|01|同上，两位数字缺位补零
a|pm|am/pm
A|PM|AM/PM
m|9|一位数字-分钟
mm|09|两位数字缺位补零
s|7|一位数字-秒
ss|07|两位数字缺位补零
SSS|000|毫秒
Z|+08:00|时区

#### **Returns**
(string): 返回格式化后的日期字符串

#### **Example**
```js
[dtc.]util.moment('1911.9.1').format()
// 1911-09-01T00:00:00+08:00
[dtc.]util.moment('1911.9.1').format('yyyy-MM-dd www')
// 1911-09-01 周五
[dtc.]util.moment('1911.9.1').format('MMMM yyyy, h:mm:ss a')
// 九月 1911, 12:00:00 am
[dtc.]util.moment('1911.9.1').format('yyyy[年]MMMd[日] www'')
// 1911年9月1日 周五
```
