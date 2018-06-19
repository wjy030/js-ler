## Number(p)
> parseInt(),parseFloat(),isNaN()在ES6里把这两个方法移植到了Number对象身上

参数|结果
-|-
undefined| NaN
null    |  0
布尔值  |  ture为1，false为0
空字符串，空格字符串|0
非空字符串，且内容为纯数字|数字
其余字符串|NaN
数字	|原来的数字
对象、函数|NaN		
空数组|0
数组里只有一个数据并且这个数据能转成数字|对应的数字
其它数组|NaN

## String(p)

参数|结果
-|-
基本数据类型、null/undefined|给数据加上引号变成字符串对象
数组|把所有中括号去掉、外面加个引号
对象|[object Object]
函数|在函数整体外面加个引号

## Boolean(p)

参数|结果
-|-
undefined| false
null  |	 false
+0、-0、NaN|false
其它数字|true
布尔值	|对应的值
空字符串 |false
其它字符串| true
对象| true
