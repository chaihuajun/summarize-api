&&=与   意思是   两个值必须相同返回ture，否则返回false
||=或   意思是  两个值任意一个值为ture就返回ture，否则返回false
javaScript的api有：
firstChild（）在父元素中的文本包括空格，如果找不到文本和空格，就返回空值
firstElementChild（）找到父元素的第一个子元素
classElementChild（）找到子元素的父元素
children（）找到一个父元素中类似数组的索引值
classList（）给一个元素添加自定义的类名，
classname（）更改原本的类名，从而实现改变样式
innerHTML（）获取元素中的标签和内容文本都会获取出来
innerText（）只会获取元素中的内容文本，不会获取元素标签
clientHeight:（）获取元素高度
clientWidth（）获取元素宽度
offsetWidth（）获取元素高度(包括边线的宽)
offsetHeight（）获取元素高度(包括边线的宽)
hidden()隐藏某个元素
数组中的api有：

以下需要熟练掌握：
length属性

以下是实例方法：
添加：
push(ele1, ele2, ..., eleN)从末尾添加多个元素。
unshift(ele1, ele2, ..., eleN)从开始添加多个元素。
splice(startIndex, 0, ele1, ele2, ..., eleN)从中间插入。

删除：
pop()从末尾删除一个元素。
shift()从开始删除一个元素。
splice(startIndex, deleteCount)从中间删除。

修改：
splice(startIndex, deleteCount, newEle1, newEle2, ..., newEleN)把原来的旧值用新值替代。
fill(新元素，start, end)用一个新元素把数组中从start开始到end结束之间的所有元素替换掉。

查询：
filter(function(value, index, arr){})用来过滤/筛选/查询数组。产生一个新数组，参数是回调函数，同forEach的用法。
slice(startIndex, endIndex)用来截取数组。负值从末尾开始算起
find(function(value, index, arr){})用来查找元素，只会匹配满足条件的第一个元素。返回找到元素。找不到返回undefined。
findIndex(function(value, index, arr){})用来查找元素所对应的索引。只会匹配满足条件的第一个元素所对应的索引。找到返回对应的索引，找不到返回-1。
indexOf(element, startIndex)从某个索引开始查找元素所对应的索引。找到返回索引，找不到返回-1。注意和findIndex()的区别。
last​IndexOf(element, startIndex)用法同indexOf。只是从后面开始查找元素所对应的索引。

for​Each(function(v,i,a){})数组循环。也可以使用for语句循环数组。
concat(arr1,arr2,...arrN)把多个数组合并/拼接成一个新数组。不会影响原 数组。
every(function(v,i,a){})数组中每一个元素都经过回调函数测试，如果都满足条件，则返回true，只要有一个不满足就返回false。
some(function(v,i,a){})数组中每一个元素都经过回调函数测试，如果有一个满足条件，就返回true。所有的都不满足条件时，才返回false。

join("分割符")用某个字符串，把数组连接成一个字符串。
toString()把数组转换成字符串，用逗号分割，不能使用其他分割符。
includes(某个元素值)用来判断数组中是否包含某个元素，包含返回true,不包含返回false。

sort()排序。默认正序。数字从小到大，字母按字母排列的顺序。也可以使用回调函数进行自定义排序。回调函数的格式：function(a,b){ return a==b?0:(a>b?-1:1)}
其中a表示后一个元素after，b前一个元素before。
注意回调函数中的返回值，1表示前一个b比后一个a大，-1表示前一个b比后一个a小。0表示前一个b和后一个a相等。
reverse()把数组中的元素反转位置，特别注意：不进行排序操作。

flat(depth)了解。把一个数组进行深度遍历（循环）。

// 以下的比较难理解：
keys()返回一个迭代器，包含数组的索引。
entries()返回一个迭代器，包含数组的索引和值。

map() 让数组中的每一个元素都执行回调函数。用执行的结果组成一个新数组。“映射”
reduce() 对数组中的每个元素执行回调函数，将其结果汇总为单个返回值。“化简”


字符串中的api有：
charAt(index) 根据索引取字符串中某个字符。
concat(str1,str2,...,strN) 把多个字符串连接合并成一个新字符串。不会影响原来的字符串。

starts​With("子字符串")
 判断字符串是否以子字符串开头，是开头返回true,否则返回false。 
ends​With("子字符串") 判断字符串是否以子符串结尾，是结尾返回true,否则返回false。 

includes("子字符串") 判断字符串是否包含子字符串，包含返回true,否则返回false。 
indexOf("子字符串") 查找字符串中子字符串所在的索引，找到返回所在索引，找不到返回-1。
last​IndexOf("子字符串") 查找字符串子字符串所在的索引(倒着找)，找到返回所在索引，找不到返回-1。

padEnd(补充后的长度，"子字符串") 在字符串后面补充几个子字符串，以达到补充后的长度。
pad​Start(补充后的长度，"子字符串") 在字符串前面补充几个子字符串，以达到补充后的长度。

repeat(几次) 重复显示几次字符串。
replace("子字符串", "新字符串") 把字符串中的子字符串，用新的字符串替换，替换一次。
讲到此处。

to​Lower​Case() 把字符串转换成小写。
toUpper​Case() 把字符串转换成大写。

trim() 去除字符串前后的空白。
trim​Right() 去除字符串右侧（后面）的空白。
Date 中的api有：日期
1.创建一个日期实例（个体）, 把对象实例化，产生一个个体。
var date1 = new Date();
var date2 = new Date(毫秒数);
var date3 = new Date("日期格式的字符串");
var date4 = new Date(year, month, date, hour, minute, second, milliSecond);

2.实例方法：
getFullYear()返回数字月份，但注意从0开始，0表示1月份，11表示12月份

getMonth()返回当前的几号，一个月的第几天。
getDate()一周的第几天， 0星期天,1-6周一到周六

getDay()返回数字小时

getHours()返回数字分钟

getMinutes() 返回秒数

getSeconds()返回毫秒

getMilliseconds()设置一个日期对象的天数。即每个月的第几天。返回的是毫秒数
setDate(20)()把毫秒数转换成日期


Math中的api有：数字
Math.PI=π≈3.14159

Math.abs(-1) 求绝对值。

Math.ceil(3.1) 其中ceil天花板，向上取整。
Math.floor(3.9) 其中floor地板，向下取整。
Math.max(n1,n2,n3,....)取所有中间的最大的。
Math.min(n1,n2,n3,.....)取所有中间的最小的。

Math.pow(5,3) 取任意数的任意方。
Math.sqrt(4) 开平方
Math.cbrt(2) 函数返回任意数字的立方根.

Math.random() 返回[0，1)之间的小数。包含0，不包括1
Math.round(3.45) 四舍五入。

对象中的api：

需要掌握的：
Object.assign()
通过复制一个或多个对象来创建一个新的对象。
Object.create()
使用指定的原型对象和属性创建一个新对象。
Object.defineProperty()
给对象添加一个属性并指定该属性的配置。
Object.keys()
返回一个包含所有给定对象自身可枚举属性名称的数组。
Object.freeze()
冻结对象：其他代码不能删除或更改任何属性。
Object.isFrozen()
判断对象是否已经冻结。
Object.seal()
防止其他代码删除对象的属性。
Object.isSealed()
判断对象是否已经密封。

如下了解：
Object.is()
比较两个值是否相同。所有 NaN 值都相等（这与==和===不同）。
Object.getOwnPropertyNames()
返回一个数组，它包含了指定对象所有的可枚举或不可枚举的属性名。
Object.getPrototypeOf()
返回指定对象的原型对象。
Object.isExtensible()
判断对象是否可扩展。
Object.preventExtensions()
防止对象的任何扩展。
Object.values()
返回给定对象自身可枚举值的数组。

循环和判断对象的ap有：
for...in...和for...of...都可以循环数组，
但前者循环的是索引，后者循环是值。
前者循环所有的属性，后者循环自有属性。

for...in...是ES5标准。for...of...是ES6的标准。

for...in...可以直接循环对象，循环是对象的属性名称。
for...of...不能直接循环对象，需要先获取对象的属性名称组成的迭代器。Object.keys(obj)。才能去循环迭代器。

常用事件api有：
onclick：元素被单击的时候执行。
*ondbclick：元素被双击的时候执行。

onfocus：元素获取焦点的时候执行。
onblur：元素失去焦点的时候执行。

onchange：内容发生变化时(控制input时注意焦点要离开)执行。

onkeydown：键盘上的键被按下时执行。
onkeyup：键盘上的键弹起时执行。
onkeypress：键盘上的键按下并弹起时执行。

onmousedown：鼠标被按下时执行。
onmouseup：鼠标被松开时执行。

onmousemove：鼠标移动时执行。

onmouseover：鼠标移动到元素上执行  支持冒泡。
onmouseleave：鼠标离开元素时执行。注意和onmouseout区别，后面会介绍 不 支持冒泡 说明不支持冒泡事件流。

onmouseout：鼠标离开元素时执行  支持冒泡。
onmouseenter：鼠标进入元素时执行。注意和onmouseenter区别，后面会介绍 不 支持冒泡 说明不支持冒泡事件流。

onreset：重置按钮被点击时执行。
onsubmit：提交按钮被点击时执行。
onload：页面或图片加载时执行。

*onerror：页面或图片加载出错时执行。
*onunload：页面退出时执行。
*onselect：选择文本时执行。

正则表达式api有：
str.search(/正则表达式语法/)
str.match(/正则表达式语法/)
str.matchAll(/正则表达式语法/)
str.replace(/正则表达式语法/)
[0-9] 中括号表示一个范围。
[a-z]
[A-Z]
{n, m} 控制字符串长度在n-m之间。
^ 匹配是否以某字符串开头
$ 匹配是否以某字符串结尾
? 匹配0次或1次。
* 匹配任意次
+ 匹配一次或多次
() 表示一组，一个整体。
|  表示或者  
\d  d=digital数字，表示一个数字，相当于[0-9]
\D  D=digital数字，表示一个非数字。
\s  s=string字符，表示不可见的字符。
\S  S=string字符，表示可见的字符。
\w  w=word，表示包含大/小写字母，数字，下划线。
\W  W=word，表示不包含大/小写字母，数字，下划线。

JQuery中的api：
scrollTop （）当出现滚动条时，然后滚动获取滚动条的高度
scrollLeft （）当出现滚动条时，然后滚动获取滚动条的宽度
动画api：
animte()可以实现所有的动画的效果。show(),hide()等方法都是在此基础上简化的。

show()显示元素
hide()隐藏元素  display: none; visibility:hidden;
toggle()切换显示/隐藏元素

fadeIn()元素淡入效果
fadeOut()元素淡出效果
fadeToggle()切换元素淡入/淡出效果

slideDown()元素向下滑入效果
slideUp()元素向上滑出效果
slideToggle()切换元素向下滑入/向上滑出效果

以下的了解一下：
stop()停止动画的执行
delay()延迟动画的执行
finish()完成动画的执行

jQuery.fx.off 关闭所有动画


筛选的api：
eq()根据数字来查找某一个
first（）获取第一个元素
last（）获取最后一个元素
hasClass查找带有特殊类名的元素
next（）括号没有值就找到上下的同级元素，带有类名的就找到自己本身；
filter（）获取索引值或者带有特殊的类名
parent()找到自己的父元素
is（）判断is里面的值是否是，是自己的父元素
map（）将一组元素转换成其他数组
makeArray（）将一个类似数组的值转换成数组  toArray（）将一个类似数组的值转换成数组 
has（）保留包含特定后代的元素，去掉那些不含有指定后代的元素
not（）从匹配元素的集合中删除与指定表达式匹配的元素
slice（开始索引值，结束索引值）注意索引左包含右不包含 ，负值从末尾开始算起
children（）在父元素中查找每个指定的子元素或者带有特定类名的元素，
find（）查找某个指定的元素，返回的是某个元素
next（）找到每个元素的后面紧邻的同辈元素。
nextAll（）找到每个元素的后面所有的同辈元素。
nextUntil 兄弟元素有很多，Until一直查找到某个元素为止。
offsetParent（）设置最近的祖先定位元素；
parent（）查找取得一个包含着所有匹配元素的唯一父元素的元素集合或者带有特殊类名的子元素的父元素，
parents（）找到某个元素的所有祖先元素
prev（）找到每个元素紧邻的前一个同辈元素或者带有特殊类名的；
prevAll（）查找当前元素之前所有的同辈元素；
siblings（）查找元素的所有同辈元素

JQuery的事件api：
1. 如何绑定/移除事件
on()方法的使用。
off()方法的使用。

2. 其它要掌握的事件
one()绑定的事件只执行一次。
trigger()触发一个事件。

hover()当鼠标悬浮/移出元素时，执行相应的回调函数。相当于mouseover和mouseout的结合。

toggle()切换显示/隐藏效果。

click()点击事件，别名。可以使用on()替代，以下类同。
mouseout()鼠标移出事件。支持冒泡
mouseover()鼠标进入事件。支持冒泡

mouseenter()鼠标进入事件。不支持冒泡
mouseleave()鼠标离开事件。不支持冒泡

keydown()按下某键时执行的事件。
keyup()某键弹起时执行的事件。
keypress()某键按下并弹起时执行的事件。

submit()表单提交时执行的事件。
change()文本内容发生变化时执行的事件。
focus()元素获取焦点时执行的事件。
blur()元素失去焦点时执行的事件。

select()在文档上选取文本时执行的事件。
resize()窗口发生变化时执行的事件。
scroll()窗口滚动时执行的事
