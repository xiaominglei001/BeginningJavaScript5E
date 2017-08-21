# BeginningJavaScript5E
# 读书重点笔记
# 第二章 数据类型与变量
## 2.1 先介绍几种常用的数据：数值数据、文本数据、布尔数据
## 2.1.1 数值
数值数据有如下两种形式,整数,小数.
## 2.1.2 文本数据
包含一个或多个字符的文本成为字符串. 把文本放在""中,就会被处理为文本而不是代码,也可以使用单引号表示字符串,对于需要特殊字符可以使用转义,如下js一些转义字符序列图
![mark](http://otbpudp75.bkt.clouddn.com/blog/170821/28II59m3Db.png?imageslim)
## 2.1.3 布尔值

## 2.2 变量
声明一个变量，那么这个变量的值就是undefined.<br>
字面值：literal，就是实际的数据，而不是通过计算得到的值或者来自其他变量的值。<br>
注意基本数据类型在赋值时总是复制副本，而较复杂的数据类型在赋值时会被共享，而不是复制副本，比如第5章介绍的对象。
## 2.3 计算数值及基本字符串操作
javascript中有4个基本的数学运算符,即+-*/,为变量赋予计算结果时,使用等号(=)运算符,它又称为赋值运算符.运算有不同优先级,乘除优先于加减.另外关于递增和递减运算符可参考如下例子:

```java
        //java中
        int a = 2;
        int b = a++ - 1;//先从a中减去1,把结果给b,然后把a再加1
        System.out.println(a);
        System.out.println(b);

        int c = 1;
        int d = ++c - 1;//先把c加1,然后从中减去1,再把结果赋给d
        System.out.println(c);
        System.out.println(d);

         int e = 1;
         System.out.println(e++);
         int f = 1;
         System.out.println(++f);
```
javascript的操作和java是一样的:
```javascript
        //javascript中
        var a = 2;
        var b = a++ - 1;//先从a中减去1,把结果给b,然后把a再加1
        alert(a);
        alert(b);
        var c = 1;
        var d = ++c - 1;//先把c加1,然后从中减去1,再把结果赋给d
        alert(c);
        alert(d);
        int e = 1;
        alert(e++);
        int f = 1;
        alert(++f);
```
输出都是:
     3
     1
     2
     1
     1
     2
## 2.4 数值类型转换
parseInt("56.02", 10)<br>
parseFloat(""56.02"")<br>
第二个参数是指定哪个进制下的转换,不写默认十进制,注意,转换时会解析字符串的每个字符,检查该字符是不是一个有效的数字,如果不是则转换停止,只返回已解析的.如果parseInt或parseFloat处理空字符串或者不以有效数字开头的字符串就返回NAN值,表示"Not a Number".<br>
NAN是JS中的一个特殊值,函数isNaN()来检查某个值是否是NaN,如 var istrue=isNaN("hello");//true.
## 2.5 数组
数组最多可以保存2的32次方个元素,另外不必预先指定数组中的元素数,当然也可以指定.<br>
在同一数组中可以保存不同类型的数据,如果访问尚未定义的数组元素,则该元素的值是undefined.<br>
两种方式创建数组:<br>
 var myArray = new Array();//通过new方式,第五章将详细介绍<br>
 var myArray = [];//通过数组字面值方式创建,多采用这一种方式<br>
 与普通变量一样,也可以先声明数组,再把该变量定义成数组:<br>
 var a;
 a=[];<br>
 数组的赋值有两种方式，一是定义时就指定，如var arr=["1","2","3"];<br>
 还有一种是先声明定义后再一个个指定:var arr=[];arr[0]=1,arr[1]=2;此时如果取arr[2],因尚未定义其值是undefined.(**这点和java很不同,java会越界**)<br>
 关于多维数组,实际上javascript只支持一维数组,但是javascript允许在一个数组内创建另一个数组,从而模拟出多维数组.实际超过二维数组的就很少用.
 # 第三章 决策与循环(略)
 # 第四章
















