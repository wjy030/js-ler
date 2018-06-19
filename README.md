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
