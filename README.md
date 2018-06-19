# js-ler
## javascript 组成：
* ECMAScript  核心：{基本语法结构和内置对象（array,string,date,math等）}
* 宿主环境
### 变量提升：
	var a=2会被翻译成:var a; a=2,var a 会被升到其作用域顶部
## js数据类型：
1. 数字，字符串，布尔，symbol  为原始类型
2. null 和undefined,一般将它们看成两个奇葩
3. 对象类型数据，包括：函数，数组，对象
### javascript数值运算:

__javascript中所有数字都是64位浮点数，会导致小数运算出问题__  
* 避免小数运算
* 运算方法：
  1. 先转换成整数（*10的倍数）再运算
  2. toFixed()四舍五入  
  
__字符串换行  
var a = 'a\  
				b\  
				c  
				';__
				
__console.dir()可以显示一个对象所有的属性和方法__

## 类型检测：
1. typeof 运算符  

|系统定义的数据类型|typeof返回的数据类型|
|:-|:-|
|Number | number  |
|String | string  |
|Boolean | boolean  |
|Undefined | undefined  |
|Null | object  |
|Object | object|  

2. Object.prototype.toString  
Object.prototype.toString.call(变量)
//返回参数的类型  
function type(o) {  
	const str = Object.prototype.toString.call(o);  
	return str.match(/\[object (.*)\]/)[1].toLowerCase();  
}
## 数据类型转换：
* 显式：调用内置方法
* 隐式：不同数据之间进行运算会引发隐式类型转换  
__js中可以把任意一种数据 类型转换成三种原始值：数字、字符串、布尔值__  
__js中可以把布尔值、数字、字符串（除了null与undefined）转为对象类型。严格来讲是转成了它们对应的包装对象__
### 显式类型转换
[类型转换方法](typeconvert.md)

### 隐式类型转换
* 出现场景  
		不同类型的数据间运算、比较
		对非布尔值类型的数据求布尔值
		条件语句的括号
#### 隐式转数字
##### 隐式转数字出现的场景
  * 数学运算符(+ - * / %), 但是加号运算里不能出现字符串或对象类型数据  
  * 一元+- （正负操作符）后的数据  
  * 某些比较运算符  
##### 隐式转数字原理
	调用Number方法  
##### 转数字方法总结
* 显式  
		Number(), parseInt(), parseFloat()
	
* 隐式  
数据前面加个加号或者先加个减号再把数据括起来，前面再加个减号  
数据减个0  
数据减个1或者乘个1  
数据模上Infinity(不适用于Infinity转数字)  
数据++或者数据--  
