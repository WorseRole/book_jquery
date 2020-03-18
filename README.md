# book_jquery
front-end

### 粗略简单的一个书城练习 练习前端

##### index 为书城首页
##### pages 放的是页面
##### static 放的是静态资源 css 以及本地的图片

-----------以下为学习笔记----------------

# 前端学习笔记

### HTML & CSS

Html 是页面大部分内容  css为页面的样式及格式

### B/S 软件结构

C/S Client Server

B/S Browser Server

客户端<——>服务器端

javaEE 项目  

客户端为浏览器

服务器端为 web服务器 tomcat jboss

### 前端开发

​                         ps                     ->                     html                           ->                   jsp

网页设计师根据需求设计网页 -> 前端工程师将设计做成静态页面 -> 后台工程师将静态网页修改为动态网页

###  网页的组成部分

1. 内容(结构)，是我们在页面中可以看到的数据，一般用html来展示
2. 表现，指的是这些内容在页面上的展示形式，比如。布局，颜色，大小，一般用css来实现
3. 行为，指的是页面中的元素与输入设备交互的响应，一般用javascript来实现

#### html简介

Hyper Text Markup Language (超文本标记语言)  简写：html

html 通过标签来标记要显示的网页中的各个部分没网页文件本身是一种文本文件，通过在文本文件中添加标记符，可以告诉浏览器如何显示其中的内容(如：文字如何处理，画面如何安排，图片如何显示)

#### 创建html文件

1. 创建一个web工程（静态的web工程）
2. 在工程下创建html 页面

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>标题</title>
</head>
<body>
    hello
</body>
</html>
~~~

注：java文件是需要编译，再由java虚拟机跑起来，但html文件不需要编译，直接由浏览器进行解析执行

#### html 文件的书写规范

~~~html
<!DOCTYPE html><!--约束 声明-->
<html lang="en"><!-- html标签表示html的开始 lang="zh_CN"表示中文 -->
<!-- html标签中一般分为两部分，分别是：head 和 body -->
<head><!-- 表示头部信息，一般包含三个部分，title标签 css样式 js代码 -->
    <meta charset="UTF-8"><!-- 表示当前页面使用utf-8 字符集 -->
    <title>标题</title><!-- 表示标题 -->
</head>

<body><!-- body标签是整个html页面显示的主题内容 -->
    hello
</body>
</html>
~~~

#### Html 标签介绍

1. 标签的格式 <标签名>封装的数据</标签名>
2. 标签名大小写不敏感
3. 标签拥有自己的属性：
   1. 分为基本属性：`bgcolor="red"`                        可以修改简单的样式效果
   2. 事件属性：`onclick="alert('你好！');"`。    <u>可以直接设置事件响应后的代码</u>
4. 标签又分为 单标签和双标签
   1. 单标签 <标签名/>			 br 换行。hr 水平线(切割线)
   2. 双标签 <标签名>封装的数据<标签名/>

#### html标签语法

官网自己查看    W3School

#### 标签用法 

建议去看W3School上自己看

#### 特殊标签

| 显示结果 | 描述              | 实体名称            | 实体编号  |
| :------- | :---------------- | :------------------ | :-------- |
|          | 空格              | `&nbsp;`            | `&#160;`  |
| <        | 小于号            | `&lt;`              | `&#60;`   |
| >        | 大于号            | `&gt;`              | `&#62;`   |
| &        | 和号              | `&amp;`             | `&#38;`   |
| "        | 引号              | `&quot;`            | `&#34;`   |
| '        | 撇号              | `&apos; (IE不支持)` | `&#39;`   |
| ￠       | 分（cent）        | `&cent;`            | `&#162;`  |
| £        | 镑（pound）       | `&pound;`           | `&#163;`  |
| ¥        | 元（yen）         | `&yen;`             | `&#165;`  |
| €        | 欧元（euro）      | `&euro;`            | `&#8364;` |
| §        | 小节              | `&sect;`            | `&#167;`  |
| ©        | 版权（copyright） | `&copy;`            | `&#169;`  |
| ®        | 注册商标          | `&reg;`             | `&#174;`  |
| ™        | 商标              | `&trade;`           | `&#8482;` |
| ×        | 乘号              | `&times;`           | `&#215;`  |
| ÷        | 除号              | `&divide;`          | `&#247;`  |

#### 标题标签

~~~html
<h1></h1>
<h2></h2>
<!--h1到h6 标题1到标题6   1最大6最小-->

h1到h6中 align为对其属性
~~~

#### 超链接

在网页中所有点击之后可以跳转的内容都是超链接

#### 列表标签

无序列表  有序列表

#### img标签

img标签可以在html页面上显示图片

```html
img 标签是图片标签，用来显示图片
    src 属性可以设置图片的路径
    width 属性设置图片的宽度
    height 属性设置图片的高度
    border 属性设置图片边框的大小
    alt 属性设置指定路径找不到图片时，用来代替显示的文本内容

在javaSe 中路径也分为相对路径 和 绝对路径
    相对路径：从工程名开始算

    绝对路径：盘符：/目录/文件名

在 web 中路径分为相对和绝对路径
    相对路径
        .       表示当前文件所在的目录
        ..      表示当前文件所在的上一位目录
        文件名    表示当前文件所在目录的文件，相当于 ./ 文件名    ./可以省略

    绝对路径
        格式是： http://ip:port/工程名/资源路径

      **错误的用法：盘符：/目录/文件名
```

#### 表格标签

```html
<!--
    table 标签是表格标签
        border 设置表格边框
        width 设置表格宽度
        height 设置表格高度
        align 设置表格相对于页面的对齐方式
        cellspacing 设置单元格间距

       tr 是行标签
       th 是表头标签
       td 是但愿个标签
            align 设置单元格文本对齐方式
       b 标签是加粗标签
-->

<table align="center" border="1" width="500" height="300" cellspacing="0">
    <tr>
        <th>1.1</th>
        <th>1.2</th>
        <th>1.3</th>
    </tr>
    <tr>
        <td>2.1</td>
        <td>2.2</td>
        <td>2.3</td>
    </tr>
    <tr>
        <td>3.1</td>
        <td>3.2</td>
        <td>3.3</td>
    </tr>
</table>
```

#### 跨行跨列表格

```html
<!--
    colspan 属性设置跨列
    rowspan 属性设置跨行
-->
```

#### iframe标签（内嵌）

```html
<!--
    iframe标签可以在页面上开辟一个小区域显示一个单独的页面
        iframe 和a 标签组合使用的步骤：
            1.在iframe标签中使用name属性定义一个名称
            2.在a标签的target属性上设置iframe的name的属性值
 -->
    <iframe src="../hello.html" width="500" height="400" name="abc"></iframe>
<ul>
    <li><a href="../hello.html" target="abc">1</a></li>
    <li><a href="test.html" target="abc">2</a></li>
    <li><a>3</a></li>
    <li><a>4</a></li>
</ul>
```



#### 表单标签**（重点）

什么是表单？

表单是html页面中，用来收集用户信息的所有元素集合，然后把这些信息发送给服务器。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>表单</title>
</head>
<body>

<!--
    form 标签 就是表单
    input 标签 type:text是文本输入框
    input type:password 是密码输入   value为input内的默认值
    input type:radio 是单选框
    input type:checkbox 是复选框 checked="checked"表示默认选中
    input type:reset 是重置按钮      value属性修改按钮上的文本
    input type:submit 是提交按钮     value属性修改按钮上的文本
    input type:button 是按钮        value属性修改按钮上的文本
    input type:file 是文件上传域
    input type:hidden 是隐藏域 当我们要发送某些信息，而这些信息，不需要用户参与，就可以使用隐藏域（提交的时候同时发送给服务器）


    select 标签是下拉列表
    option 标签是下拉列表框中的选项 selected="selected"设置默认选中

    textarea 表示多行文本输入框 （起始标签和结束标签中介为默认值）
        rows 属性设置可以显示几行的高度
        cols 属性设置每行可以显示几个字符宽度

-->

<!--******-->
<!-- action属性设置提交的服务器地址 -->
<!-- method属性设置提交的方式 get(默认)/post -->
<!--
    表单提交的时候，数据没有发送给服务器的三种情况
        1.表单项没有name
        2.单选，复选(下拉列表中的option标签) 都需要添加value属性，以便发送地址服务器
        3.该单项不在form表单中

    GET请求特点
        1.浏览器地址中的地址是：action属性[ + ? + 请求参数]
          请求参数的格式是：name=value&name=value
        2.不安全
        3.有数据长度的限制 入如果表单值包含ASCII字符或者超过一定字符，必须使用 post请求

    POST请求特点
        1.浏览器地址中只有action属性值
        2.相对于GET请求更安全
        3.理论上没有数据长度限制
-->

<form action="http://localhost:8080" method="post">
    <h1 align="center">用户注册</h1>
    <table align="center">
        <tr>
            <td>用户名称：</td>
            <td><input name="username" type="text" value="默认"/></td>
        </tr>
        <tr>
            <td>用户密码：</td>
            <td><input name="password" type="password" value="abc"/></td>
        </tr>
        <tr>
            <td>确认密码</td>
            <td><input name="password" type="password" value="abc"/></td>
        </tr>
        <tr>
            <td>性别：</td>
            <td>
                <input type="radio" name="sex" checked="checked" value="boy"/>男
                <input type="radio" name="sex" value="girl"/>女
            </td>
        </tr>
        <tr>
            <td>兴趣爱好：</td>
            <td>
                <input name="hobby" type="checkbox" checked="checked" value="java"/>java
                <input name="hobby" type="checkbox" value="html"/>html
                <input name="hobby" type="checkbox" value="css"/>css
                <input name="hobby" type="checkbox" value="js"/>js
                <input name="hobby" type="checkbox"checked="checked" value="python"/>python
            </td>
        </tr>
        <tr>
            <td>国籍：</td>
            <td>
                <select name="country">
                    <option>--请选择国籍--</option>
                    <option selected="selected" value="china">中国</option>
                    <option value="usa">美国</option>
                    <option value="jp">日本</option>
                </select>
            </td>
        </tr>
        <tr>
            <td>自我评价：</td>
            <td><textarea name="desc" rows="10" cols="20">这里是默认值</textarea></td>
        </tr>
        <tr>
            <td><input type="reset" value="重置"/></td>
            <td align="right"><input type="submit" value="提交"/</td>
        </tr>
    </table>

    <br/>
    <br/>
    <br/>
    <br/>
    <input type="hidden" name="abc" value="valueName"/>
</form>
</body>
</html>
```

#### 其他标签

div标签 span标签 p段落标签

```html
<!--
    div标签   默认独占一行
    span标签  它的长度是封装数据的长度
    p段落标签  默认会在段落的上方或下方各空出一行来（如果已有就不再空）
-->
<div>div1</div>
<div>div2</div>
<span>span1</span>
<span>span2</span>
<p>p1</p>
<p>p2</p>
```

### CSS技术 文档

##### CSS技术介绍

Cascading Style Sheet

css是[层叠样式表单]。是用于(增强)控制网页样式并允许将样式信息与网页分离的一种标记性语言。

##### CSS语法规则

~~~css
选择器{
  属性：值；
}
----例：----
p{
  color:red;
  font-size:30px;
}

css注释 /*注释内容*/
~~~

#### CSS和HTML结合使用

##### 第一种

在标签的style属性上设置"key:value value"，修改标签样式

```html
<div style="border: 1px solid red; width: 100px; height: 100px; background-color: grey; text-align: center;">div1</div>
<div style="border: 1px solid red;">div2</div>
<span style="border: 1px solid red;">span1</span>
<span style="border: 1px solid red;">span2</span>
```

缺点：

1. 如果标签多了，样式多了，代码量非常大
2. 可读性太差
3. CSS代码没有什么复用性可言

##### 第二种

在head标签中，使用style标签来定义各种自己需要的css样式

格式如下：

~~~css
xxx {
  Key: value value;
}
~~~

```html
<!--style标签专门用来定义css样式代码-->
<style type="text/css">
    /*
        在这里注释这么写
    */
    div {
        border: 1px solid red;
    }
    span {
        border: 1px solid red;
    }
</style>
```

缺点：

1. 只能在同一页面内复用，不能在多个页面中复用css代码
2. 维护起来不方便，实际的项目中会有成千上万的页面，要到每个页面中去修改，工作量太大了。

##### 第三种

把css样式写成一个单独的css文件，再通过link标签引入即可复用。

```html
<!--link标签专门用来引入css样式代码-->
<link rel="stylesheet" type="text/css" href="css_1.css" />
```

```css
div {
    border: 1px solid yellow;
}
span {
    border: 1px solid red;
}
```

#### CSS选择器

##### 标签名选择器

标签名选择器的格式是：

标签名 {

​		属性：值；

}

标签名选择器，可以决定哪些标签被动的使用这个样式。

```html
<style type="text/css">
    div {
        border: 1px solid yellow;
        color: blue;
        font-size: 30px;
    }
    span {
        border: 5px dashed blue;
        color: yellow;
        font-size: 20px;
    }
</style>
```

##### id选择器

id选择器的格式是：

​		#id 属性值 {

​					属性：值；

}

id选择器，可以让我们通过id属性选择性的去使用这个样式。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>id选择器</title>
    <style type="text/css">
        #id001 {
            color: blue;
            font-size: 20px;
            border: 1px solid yellow;
        }
        #id002 {
            color: red;
            font-size: 20px;
            border: 5px blue dotted;
        }
    </style>
</head>
<body>
<div id="id001">div1</div>
<div id="id002">div1</div>
<div>div3</div>
</body>
</html>
```

##### class选择器

class类型选择器的格式是：

​			.class 属性值 {

​					属性：值；

}

class类型选择器，可以通过class属性有效的选择性的使用这个样式。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>class选择器</title>
    <style type="text/css">
        .class01 {
            color: blue;
            font-size: 30px;
            border: 1px solid;
        }
        .class02 {
            color: grey;
            font-size: 25px;
            border: 1px solid red;
        }
    </style>
</head>
<body>
<div class="class01">div1</div>
<div class="class02">div2</div>
<span class="class01">span1</span>
<span>span2</span>
</body>
</html>
```

##### 组合选择器

组合选择器的格式是：

​		选择器1，选择器2，选择器n {

​						属性：值；

}

组合选择器可以让多个选择器共用一个css样式代码。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>组合选择器</title>
    <style type="text/css">
        .class01, #id01 {
            color: blue;
            font-size: 20px;
            border: 1px yellow solid;
        }
    </style>
</head>
<body>
<div class="class01">div</div>  <br/>
<span id="id01">span</span>  <br/>
<div>div</div>  <br/>
<div>div id01</div>
</body>
</html>
```

#### CSS常用样式

###### 1.颜色

color：red

颜色也可以用rgb值和十六进制表示值：如rgb(255,0,0)，#00F6DE ,如果写十六进制值必须加#

###### 2.宽度

width：20px;

宽度也可以写像素值：20px；

也可以写百分比值: 20%;

###### 3.高度

height：20px；

也可以写像素值：20px；

也可以写百分比值: 20%;

###### 4.背景颜色

background-color：#0F2D4C

###### 5.字体样式

color: #FF0000;  字体颜色红色

Font-size: 20px;  字体大小

###### 6.红色1像素实线边框

border: 1px solid red;

###### 7.div居中

margin-left: auto;

margin-right: auto;

###### 8.文本居中

text-align: center;

###### 9.超链接去下划线

text-decoration: none;

###### 10.表格细线

table {

​		border: 1px solid black; /* 设置边框*/

​		border-collapse: collapse; /* 将边框合并*/

}

td, th {

​		border: 1px solid black; /* 设置边框*/

}

###### 11.列表去除修饰

ul {

​		list-style: none;

}

## JavaScript

### js介绍

JavaScript 语言诞生主要是完成页面数据验证，因此它运行在客户端，需要运行浏览器来解析执行javascript代码

JS是Netscape网景公司的产品，最早取名为LiveScript；为了吸引更多java程序员。更名为javaScript

JS是弱类型语言，Java是强类型语言。

弱类型：就是类型可变

强类型：就是定义变量的时候，类型已确定，而且不可变。

int i=12;



var i;

i=12;		数值类型

i="abc";	字符串类型



特点：

1. 交互性 (它可以做的就是信息的动态交互)
2. 安全性 (不允许直接访问本地硬盘)
3. 跨平台性 (只要可以解释 JS 的浏览器都可以执行，和平台无关)

### JS和html代码的结合方式

#### 第一种方式

只需要在head 标签中，或者body 标签中， 使用script 标签来书写js代码

```html
<script type="text/javascript">
    //alert js语言提供的一个警告框函数
    //它可以接受任意类型的参数，这个参数是警告框的提示信息
    alert("hello js！");
</script>
```

#### 第二种方式

使用script标签引入单独的 js代码文件

```html
<!--
    现在需要使用script引入外部的js文件来执行
        src属性专门用来引入js文件路径（可以是相对路径，也可以是绝对路径）

    script标签可以用来定义js代码，也可以用来引入js文件
    但是，两个功能二选一使用，不能同时使用两个功能
 -->
<script type="text/javascript" src="js_1.js"></script>
<!--这么用是错误用法
<script type="text/javascript" src="js_1.js">
	alert("sssss");
</script>
-->
<script type="text/javascript">
    alert("sssss");
</script>
```

上述为顺序执行

### 变量

什么是变量？变量可以存放某些值的内存的命名。

js的变量类型：

​	数值类型		number

​	字符串类型	string

​	对象类型		object

​	布尔类型		boolean

​	函数类型		function

js里的特殊的值：

​	undefined	未定义，所有js变量未赋于初始值的时候，默认值都是undefined

​	null				空值

​	NAN				全称是 Not a Number 非数字。非数值。

js中的定义变量格式：

​	var 变量名；

​	var 变量名 = 值；

```js
<script type="text/javascript">
    var i;
    alert(i);   //undefined
    i=12;
    alert(i);
    //typeof()是js语言提供的一个函数
    //它可以取变量的数据类型返回
    alert(typeof(i));   //number
    i="abc";
    alert(i);
    alert(typeof(i));   //string
    var a=12;
    var b="abv";
    alert(a * b);      //NaN 非数字 非数值。
</script>
```

#### 关系（比较）运算

等于：		==		等于是简单的做字面值的比较

全等于：	===	  除了做字面值的比较之外，还会比较两个变量的数据类型

```javascript
<script type="text/javascript">
    var a=12;
    var b="12";
    alert(a==b);//true
    alert(a===b);//false
</script>
```

#### 逻辑运算

且运算：		&&

或运算：		||

非运算：		！



&&运算。

有两种情况：

第一种：当表达式全为真的时候，返回最后一个表达式的值。

第二种：当表达式中，有一个为假的时候。返回第一个为假的表达式的值

```javascript
var a="abc";
var i=12;
var b=true;
var c=false;
var d=null;
```

|| 或运算

第一种情况：当表达式全为假时，返回最后一个表达式的值

第二种情况：只要有一个表达式为真。就会返回第一个为真的表达式的值。



并且 && 与运算||或运算有短路

短路就是说。当这个&&或||运算有结果了之后。 后面的表达式就不再执行。





在js语言中，所有的变量，都可以作为一个boolean类型的变量去使用。

0、null、undefined、“”(空串) 都认为是false

```javascript
<script type="text/javascript">
    // var a=0;
    // if(a) {
    //  alert("0 为真");
    // } else {
    //     alert("0 为假");
    // }
    // var a=null;
    // if(a) {
    //     alert("null 为真");
    // } else {
    //     alert("null 为假");
    // }
    // var a=undefined;
    // if(a) {
    //     alert("undefined 为真");
    // } else {
    //     alert("undefined 为假");
    // }
    var a="";
    if(a) {
        alert("空串 为真");
    } else {
        alert("空串"+"为假");
    }
</script>
```

### 数组（重点）

#### 数组定义方式

js中熟组的定义

​	格式：

​	var 数组名 = []; //空数组

​	var 数组名 = [1, 'abc', true]; //定义数组同时赋值元素

```javascript
<script type="text/javascript">

    var arr = [true, 1]; //定义一个数组
    // alert(arr.length);      //0
    arr[0] = 12;
    // alert(arr[0]);          //12
    // alert(arr.length);      //1
    arr[2] = "abc";
    // alert(arr.length);      //3
    // alert(arr[1]);          //undefined
    //javascript 语言中的数组，只要我们通过数组下标赋值，那么最大的下标值，就会自动的给数组做扩容操作。

    for(var i=0; i<arr.length; i++) {
        alert(arr[i]);
    }

</script>
```

### 函数（重点）

#### 函数的两种定义方式

##### 第一种

可以使用function 关键字来定义函数

使用格式如下：

​	function 函数名(形参列表){

​			函数体

}

在js语言中，如何定义带有返回值的函数？

只需要在函数体内直接使用return 语句返回值即可。

```javascript
<script type="text/javascript">

    //定义一个无参函数
    function fun() {
        alert("无参函数fun()被调用了");
    }
    //函数调用才会执行
    fun();

    //定义一个有参函数
    function fun2(a, b) {
        alert("有参函数fun2()被调用了 a=>" + a + ", b=>" +b);
    }
    fun2(12, "abc");

    //定义带有返回值的函数
    function fun3(num1, num2) {
        var result = num1 + num2;
        return result;
    }
    alert(fun3(100, 50));

</script>
```

##### 第二种

使用格式如下：

​	var 函数名 = function(形参列表) {函数体}

```javascript
<script type="text/javascript">

    var fun = function () {
        alert("无参函数");
    }
    fun();

    var fun1 = function (a, b) {
        alert("有参函数fun1 a=>"+a+",b=>"+b);
    }
    fun1(1,2);

    var fun2 = function (num1, num2) {
        var result = num1+num2;
        return result;
    }

    alert(fun2(100, 200));

</script>
```

#### 函数的 arguments 隐形参数（只在function函数内）

就是在function函数中不需要定义，但却可以直接用来获取所有参数的变量，我们管他叫隐形参数。

隐形参数特别像java基础的可变长参数一样

public void fun(Object...args);

可变长参数其实是一个数组。



那么js中隐形参数也和java的可变长参数一样，操作类似数组。

```javascript
<script type="text/javascript">

    function fun() {
        // alert(arguments.length);
        alert(arguments[0]);
        alert(arguments[1]);
        alert(arguments[2]);
        for(var i=0; i<arguments.length; i++) {
            alert(arguments[i]);
        }
        alert("无参函数fun()");
    }

    fun(1, "a", true);

    //需求 要求编写一个函数。用于计算所有参数想加的和并返回
    function sum(num1, num2) {
        var result = 0;
        for(var i=0; i<arguments.length; i++) {
            if(typeof(arguments[i]) == "number") {
                result += arguments[i];
            }
        }
        return result;
    }

    alert(sum(1,2,3,5,3,"abc",4));

</script>
```

### JS中的自定义对象（扩展内容）

#### Object形式的自定义对象

​	对象的定义：

​		var 变量名 = new object();		//对象实例(空对象)

​		变量名.属性名 = 值；				//定义一个属性

​		变量名.函数名 = function(){}	//定义一个函数(方法)

​	对象的访问：

​		变量名.属性 / 函数名();

```javascript
<script type="text/javascript">

    var object = new Object();
    object.name = "华仔";
    object.age = 18;
    object.fun = function () {
        alert("姓名：" + this.name +", 年龄：" + this.age);
    }

    object.fun();

</script>
```

#### {}花括号形式的自定义对象

​	var 变量名 = {};	//空对象

​	var 变量名 = {			//需要加逗号  最后一个不加

​		属性名: 值 ，

​		属性名: 值，

​		函数名: function(){}

}

```javascript
<script type="text/javascript">

    // var object = {};
    // alert(typeof(object));

    var object = {
        name:"华仔",
        age:18,
        fun:function () {
            alert("姓名："+this.name+", 年龄："+this.age);
        }
    }
    alert(object.name);
    object.fun();
```

### JS中的事件

什么是事件？事件是电脑输入设备与页面进行交互的响应。我们称之为事件。

#### 常用的事件：

​	onload: 加载完成事件		//页面加载完成之后，常用于做页面js代码初始化操作

​	onclick: 单击事件				//常用于按钮的点击相应操作

​	onblur: 失去焦点事件		//常用于输入框失去焦点后验证其输入内容是否合法。

​	onchange: 内容发生改变事件	//常用于表单提交之前，验证所有表单项是否合法。

#### 事件的注册(绑定)又分为静态和动态

什么是事件的注册(绑定)？

其实就是告诉浏览器，当事件响应后要执行哪些操作代码，叫事件注册或事件绑定。



**静态注册事件：**通过html标签的事件属性直接赋于事件响应后的代码，这种方式叫做静态注册。

**动态注册事件：**是指先通过js代码得到标签的dom对象，然后通过dom对象.事件名=function(){} 这种形式赋于事件响应后的代码，叫动态注册。

动态注册基本步骤：

	1. 获取标签对象

   	2. 标签对象.事件名 = function(){}

##### onload加载完成事件

```javascript
<script type="text/javascript">
        // function onloadFun() {
        //     alert("静态注册onload事件，所有代码");
        // }

        //onload 事件动态注册。是固定写法
        window.onload = function () {
            alert("动态注册的onload事件");
        }

    </script>
</head>

<!--
    静态注册onload事件
        onload事件是浏览器解析完页面后就会自动出发的事件
        <body onload="onloadFun();">
-->
```

##### onclick单击事件

```javascript
    <script type="text/javascript">
        function onclickFun() {
            alert("静态注册 onclick事件");
        }
        //动态注册 onclick事件
        window.onload = function () {
            //1.获取标签对象
            /*
            document 是js 提供的一个对象（文档）
            get         获取
            Element     元素（就是标签）
            By          通过
            Id          id
             */
            var btnObj = document.getElementById("btn01");
            alert(btnObj);
            //2.通过标签对象.事件名 = function(){}
            btnObj.onclick = function () {
                alert("动态注册的onclick事件");
            }
        }
    </script>
</head>
<body>
    <!--静态注册onclick事件-->
    <button onclick="onclickFun();">按钮1</button>
    <button id="btn01">按钮2</button>
</body>
```

##### onblur失去焦点事件

```javascript
    <script type="text/javascript">
        //静态注册失去焦点事件
        function onblurFun() {
            //console 是控制台对象，是由js语言提供，专门用来向浏览器的控制器打印输出， 用于测试使用
            // log() 是打印的方法
            console.log("静态注册失去焦点事件");
        }
        //动态注册onblur事件
        window.onload = function () {
            //1.获取标签对象
            var passwordObj = document.getElementById("password");
            alert(passwordObj);
            //2.通过标签对象.事件名 = function(){}
            passwordObj.onblur = function () {
                console.log("动态注册失去焦点事件");
            }
        }
    </script>
</head>
<body>
    用户名：<input type="text" onblur="onblurFun()"/> <br/>
    密码：<input id="password" type="password"/> <br/>
</body>
```

##### onchange内容发生改变事件

```html
<head>
    <meta charset="UTF-8">
    <title>onchange</title>
    <!--静态注册onchange事件-->
    <script type="text/javascript">
        function onchangeFun() {
            alert("女神已经改变了！");
        }
        <!--动态注册onchange事件-->
        window.onload = function () {
            //1.获取标签对象
            var selectObj = document.getElementById("sel01");
            alert(selectObj);
            //2.通过标签对象.事件名 = function(){}
            selectObj.onchange = function () {
            alert("男神已经发生改变");
            }
        }
    </script>
</head>
<body>
    <!--动态注册onchange事件-->
    请选择你心中的男神：
    <select id="sel01">
        <option>--男神--</option>
        <option>德华</option>
        <option>富城</option>
        <option>学友</option>
    </select>
    <!--静态注册onchange事件-->
    请选择你心中的女神：
    <select onchange="onchangeFun();">
        <option>--女神--</option>
        <option>芳芳</option>
        <option>佳佳</option>
        <option>嬛嬛</option>
    </select>
</body>
```

##### onsubmit表单提交事件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script type="text/javascript">
        //静态注册表单提交事务
        function onsubmitFun() {
            //要验证所有表单单项是否合法，如果，有一个不合法就组织表单提交
            alert("静态注册表单提交事件---发现不合法");
            return false;       //true 就可以提交
        }
        //动态注册表单提交事务
        window.onload = function () {
            var submitObj = document.getElementById("submit01");
            submitObj.onsubmit = function () {
                alert("动态注册表单提交事件---发现不合法");
                return false;   //true 就可以提交
            }
        }
    </script>
</head>
<body>
    <form action="http://localhost:8080" method="get" onsubmit="return onsubmitFun();">
        <input type="submit" value="静态注册"/>
    </form>
    <form action="http://localhost:8080" method="get" id="submit01">
        <input type="submit" value="动态注册"/>
    </form>
</body>
</html>
```

### DOM 模型（重点）

DOM全称睡觉哦 Document Object Model文档对象模型

大白话，就是把文档中的标签，属性，文本，转换成为对象来管理。

那么，它们是如何把标签，属性，文本转化成为对象来管理呢，只是要学习的点。

#### Document对象

document对象的理解：

​	第一点：Document 它管理来所有的HTML文档内容。

​	第二点：docuemnt 它是一种树结构的文档。有层级关系。

​	第三点：它让我们把所有的标签 都 对象化。

​	第四点：我们可以通过 document 访问所有的标签对象。



什么是对象化？

​	例如：

有一个人年龄：18岁，性别：女，名字：张某某

~~~java
Class Person {
  int age;
  String sex;
  String name;
}
~~~

那么html 标签对象化

~~~html
<body>
  <div id="div01">
    div01
  </div>
</body>

Class Dom {
	String id;					//id属性
	String tagName;			//表示标签名
	Dom parentNode;			//父亲
	List<Dom> children;	//孩子节点
  String innerHtml;		//起始标签和结束标签中间的内容
}
~~~

#### Document对象中的方法介绍（重点）

**document.getElementById(elementId)**

通过标签的id属性查找标签dom 对象，elementId 是标签的id 属性值

**document.getElementByName(elementName)**

通过标签的name 属性查找标签dom 对象，elementName 标签的name 属性值

**document.getElementTagName(tagName)**

通过标签名查找标签dom对象。tagName是标签名

**document.createElement( tagName)**

方法，通过给定标签名，创建一个标签对象。tagName 是要创建的标签名



**注意：**

​	<font style="color:red">document对象的三个查询方法，如果有id属性，优先使用getElementById方法进行查询，-> 使用getElementByName ->getElementTagName </font>

​		以上三个方法，一定要在页面加载完成之后执行，才能查询到标签对象。

##### getElementById

```html
<head>
    <meta charset="UTF-8">
    <title>getElementById</title>
    <script type="text/javascript">
        //验证：必须由字母，数字，下划线组成，长度为5-12位。
        function onclickFun() {
            //当我们要操作一个标签时，一定要先获取标签对象。
            var usernameObj = document.getElementById("username");
            // alert(usernameObj); 他就是dom对象
            // alert(usernameObj.id); 是id
            // alert(usernameObj.type);
            // alert(usernameObj.value);
            var username = usernameObj.value;
            // 如何验证字符串 符合某个规则，需要使用正则表达式
            var patt = /^\w{5,12}$/;        //正则需要复习了

            //test()方法 用于测试某个字符串，是不是匹配我的规则
            if(patt.test(username)) {
                alert("合法");
            }else {
                alert("不合法");
            }
        }
    </script>
</head>
<body>
    用户名：<input type="text" id="username" value="default"/>
    <button onclick="onclickFun()">交验</button>
</body>
```

```html
<script type="text/javascript">
        //验证：必须由字母，数字，下划线组成，长度为5-12位。
        function onclickFun() {
            //当我们要操作一个标签时，一定要先获取标签对象。
            var usernameObj = document.getElementById("username");
            // alert(usernameObj); 他就是dom对象
            // alert(usernameObj.id); 是id
            // alert(usernameObj.type);
            // alert(usernameObj.value);
            var username = usernameObj.value;
            // 如何验证字符串 符合某个规则，需要使用正则表达式
            var patt = /^\w{5,12}$/;        //正则需要复习了

            var usernameSpanObj = document.getElementById("usernameSpan");
            //innerHTML 表示起始标签和结束标签中的内容
            //innerHTML 这个属性可读 ， 可写
            // alert(usernameSpanObj.innerHTML);

            //test()方法 用于测试某个字符串，是不是匹配我的规则
            //匹配就返回true 否则返回false
            if(patt.test(username)) {
                // alert("合法");
                usernameSpanObj.innerHTML = "用户名合法!";
                // usernameSpanObj.innerHTML = "<img src=\"../1.jpg\" width=\"18\" height=\"18\">";
            }else {
                // alert("不合法");
                // usernameSpanObj.innerHTML = "用户名不合法！";
                usernameSpanObj.innerHTML = "<img src=\"../1.jpg\" width=\"18\" height=\"18\">";
            }
        }
    </script>
</head>
<body>
    用户名：<input type="text" id="username" value="default"/>
    <span id="usernameSpan" style="color: red;"></span>
    <button onclick="onclickFun()">交验</button>
</body>
```

##### 正则：

```html
<script type="text/javascript">
    //表示要求字符串中 是否 包含字母 e
    //patt patt1 两个一样。
    // var patt = new RegExp("e");
    // var patt1 = /e/;
    //表示字符串是否包含a 或者b 或者c
    // var patt = /[abc]/;
    //表示要求字符串中 是否包含任意大写字母
    // var patt = /[A-Z]/;
    //表示要求字符串中 是否包含任意小写字母
    // var patt = /[a-z]/;
    //是否包含 任意数字
    // var patt = /[0-9]/;
    //表示要求字符串，是否包含字母，数字，下划线
    // var patt = /\w/;
    //表示要求字符串中，是否包含 至少一个a
    // var patt = /a+/;
    //表示要求字符串中， 是否包含零个 或 多个a
    // var patt = /a*/;
    //表示要求字符串中 是否包含一个或零个a
    // var patt = /a?/;
    //表示要求 字符串是否包含连续三个a
    // var patt = /a{3}/;
    //表示要求 字符串是否包含至少3个，最多连续5个a
    // var patt = /a{3,5}/;
    //表示要求 字符串必须以a 结尾
    // var patt = /a$/;
    //表示要求 字符串必须以a 打头
    // var patt = /^a/;

    //表示要求字符串中是否包含至少三个连续的a
    // var patt = /a{3,5}/;
    //要求字符串 从头到尾必须完全匹配
    // var patt = /^a{3,5}&/;
    
    var patt = /^\w{5,12}$/;

    var str = "_aaaaaa3";

    alert(patt.test(str));

</script>
```

##### getElementByName

```html
    <script type="text/javascript">
        //全选
        function checkAll() {
            //让所有复选框都选中 是根据指定的name 属性查询返回多个标签对象集合
            //这个集合的操作跟数组 一样
            //集合中每个元素都是dom对象
            //这个集合的元素顺序是html 页面中从上到下的顺序
            var hobbies = document.getElementsByName("hobby");

            //checked 表示复选框的选中状态，如果选中是true，不选中是false
            //checked 这个属性可读， 可写
            // alert(hobbies[1].checked);
            for(var i=0; i<hobbies.length; i++) {
                hobbies[i].checked = true;
            }
        }
        //全不选
        function checkNo() {
            var hobbies = document.getElementsByName("hobby");
            for(var i=0; i<hobbies.length; i++) {
                hobbies[i].checked = false;
            }
        }
        //反选
        function checkReverse() {
            var hobbies = document.getElementsByName("hobby");
            for(var i=0; i<hobbies.length; i++) {
                hobbies[i].checked = !hobbies[i].checked;
                // if(hobbies[i].checked) {
                //     hobbies[i].checked = false;
                // }else {
                //     hobbies[i].checked = true;
                // }
            }
        }
    </script>
</head>
<body>
    <input type="checkbox" name="hobby" value="java" checked="checked"/> java
    <input type="checkbox" name="hobby" value="cpp"/> c++
    <input type="checkbox" name="hobby" value="py"/> python
    <br/>
    <button onclick="checkAll();">全选</button>
    <button onclick="checkNo();">全不选</button>
    <button onclick="checkReverse();">反选</button>
</body>
```

##### getElementByTagName

```html
<script type="text/javascript">
        function checkAll() {
            //document.getElementByTagName("input");是按照指定标签名来进行查询并返回集合
            //这个集合的操作跟数组 一样
            //集合中都是dom对象
            //集合中的元素顺序 是它们在html 页面中从上倒下的顺序
            var inputs = document.getElementsByTagName("input");
            // alert(inputs);
            for(var i=0; i<inputs.length; i++) {
                inputs[i].checked = true;
            }
        }
    </script>
</head>
<body>
    兴趣爱好：
    <input type="checkbox" value="cpp"/>c++
    <input type="checkbox" value="java"/>java
    <input type="checkbox" value="python"/>python
    <br/>
    <button onclick="checkAll();">全选</button>
</body>
```

#### 节点的常用属性和方法

节点就是标签对象

**方法：**

通过具体的元素节点调用：

getElementsByTagName()方法，获取当前节点的指定签名孩子节点。

appendChild(oChildNode)方法，可以添加一个字节点，oChildNode 是要添加的孩子节点

```javascript
<script type="text/javascript">

    window.onload = function () {

        //现在需要我们使用js代码来创建html标签 并显示在页面上
        //标签的内容就是：<div>牛逼</div>
        var divObj = document.createElement("div"); //在内存中<div></div>

        divObj.innerHTML = "逼哥 我爱你";//<div>逼哥 我爱你</div>。但，还在内存中
				//添加子元素
        document.body.appendChild(divObj);
    }
</script>
```

```javascript
window.onload = function () {
    var divObj = document.createElement("div");

    var textNode = document.createTextNode("逼哥 我爱你");

    divObj.appendChild(textNode);

    document.body.appendChild(divObj);

}
//和上面的代码描述一样
```

**属性：**

childNodes 属性，获取当前节点的所有子节点

firstChild 属性，获取当前节点的第一个子节点

lastChild 属性，获取当前节点的最后一个子节点

parentChild 属性，获取当前节点的父节点

nextSibling 属性，获取当前节点的下一个节点

previousSibling 属性，获取当前节点的上一个节点

className 用于获取或设置标签的class 属性值

innerHTML 属性，表示获取/设置起始标签和结束标签中的***内容***

innerText 属性，表示获取/设置起始标签和结束标签中的***文本***

## jQuery

### jQuery介绍

**什么是jQuery？**

jQery，javascript 和查询(Query)，它是辅助JavaScript开发和js类库。

**jQuery核心思想？**

它的核心思想是write less，do more(写的更少 做的更多)，所以它实现了很多浏览器的兼容问题

**jQuery流行程度？**

jQuery已经成为最流行的javascript类库

**jQuery的好处？**

jQuery是免费的、开源的、jQuery的语法设计可以使开发更加便捷，例如操作文档对象、选择DOM元素、制作动画效果、事件处理、使用Ajax以及其他功能。

```javascript
<script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        // alert($);
        $(function () {     //表示页面加载完成 之后，相当 windows.onload = function() {}
            var $btnObj = $("#btnId");  //表示按id查询标签对象
            $btnObj.click(function () {//绑定单击事件 .click
                alert("jQuery的单击事件");
            });
        });
    </script>
<!--
    <script type="text/javascript">
        window.onload = function () {
            var btnObj = document.getElementById("btnId");
            // alert(btnObj);   ==> dom对象
            btnObj.onclick = function () {
                alert("js单击事件");
            }
        }
    </script>
-->

</head>
<body>

    <button id="btnId">SayHello</button>

</body>
```

常见问题：

1. 使用jQuery一定要引入 jQuery库吗？  答案：是必须。
2. jQuery 中的 $ 到底是什么？                  答案：它是一个函数。
3. 怎么为按钮添加点击响应函数的？
   1. 使用jQuery 查询到标签对象
   2. 使用标签对象 .click( function() {});

### jQuery核心函数

$ 是jQuery的核心函数，能完成jQuery的很多功能。$() 就是调用$这个函数

1. 传入参数为[函数]时：

   表示页面加载完成之后，相当于 windows.onload = function() {}

2. 传入参数为[HTML字符串]时：

   会对我们创建这个 html标签对象

3. 传入参数为[选择器字符串]时：

   $("#id 属性值");  id选择器，根据id 查询标签对象。

   $("标签名");   标签名选择器，根据指定的标签名查询标签对象。

   $(".class 属性值");  类型选择器，根据class 属性值查询标签对象。

4. 传入参数为[DOM对象]时：

   会把这个dom 对象转换为jQuery对象。

```html
<script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <!--
    <script type="text/javascript">
        // alert($);
        $(function () {     //表示页面加载完成 之后，相当 windows.onload = function() {}
            var $btnObj = $("#btnId");  //表示按id查询标签对象
            $btnObj.click(function () {//绑定单击事件 .click
                alert("jQuery的单击事件");
            });
        });
    </script>
    -->
<!--
    <script type="text/javascript">
        window.onload = function () {
            var btnObj = document.getElementById("btnId");
            // alert(btnObj);   ==> dom对象
            btnObj.onclick = function () {
                alert("js单击事件");
            }
        }
    </script>
-->
    <script type="text/javascript">
        alert("页面加载完成之后，自动调用");
        //传入参数为[HTML字符串]时：
        $(function () {
            $("<div>" +
                "        <span>div-span3</span>" +
                "        <span>div-span4</span>" +
                "    </div>").appendTo("body");

            alert($("button").length);//根据标签名来查询

            var btnObj = document.getElementById("btn01");
            // alert(btnObj);
            alert($(btnObj));   //会转成jQuery对象
        });
    </script>
</head>
<body>
    <div>
        <span>div-span1</span>
        <span>div-span2</span>
    </div>
    <button id="btn01">按钮1</button>
    <button>按钮2</button>
    <button>按钮3</button>
<!--    <button id="btnId">SayHello</button>-->
</body>
```

### jQuery对象和dom对象区分

#### 什么是jQuery对象，什么是dom对象

##### Dom对象

1. 通过 getElementById查询出来的标签对象是Dom对象

2. 通过getElementByName查询出来的标签对象是Dom对象

3. 通过getElementByTagName查询出来的标签对象是Dom对象

4. 通过createElement() 方法创建的对象，是Dom对象

   **DOM 对象 alert 出来的效果是： [object HTML 标签名 Element]**

##### jQuery对象

5. 通过jQuery 提供的 API 创建的对象，是 jQuery 对象

6. 通过 jQuery 包装的Dom对象，也是 jQuery 对象

7. 通过 jQuery 提供的 API 查询到的对象，是jQuery 对象

   **jQuery 对象 alert 出来的效果是：[object object]**

#### jQuery对象的本质是什么？

jQuery对象是dom 对象的数组 + jQuery提供的一系列功能函数，

```html
<script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        $(function () {
            var arr = [12, "abc", true];
            var $btns = $("button");

            for(var i=0; i< $btns.length; i++) {
                alert($btns[i]);
            }
        });
    </script>
</head>
<body>
    <div id="testDiv">myself is very good!</div>
    <button id="dom2dom">使用dom对象调用Dom方法</button>
    <button id="dom2jQuery">使用dom对象调用jquery方法</button>
    <button id="jQuery2jQuery">使用jQuery对象调用jQuery方法</button>
    <button id="jQuery2dom">使用jQuery对象调用dom方法</button>
</body>
```

#### jQuery对象和Dom对象使用区别

jQuery 对象不能使用Dom 对象的属性和方法

Dom 对象也不能使用 jQuery对象的属性和方法

#### Dom对象和jQuery对象互转

##### 1.dom对象转换为jQuery对象

1. 现有Dom对象
2. $(Dom 对象) 就可以转换成为 jQuery 对象

##### 2.jQuery 对象转换为 dom 对象

1. 先有 jQuery 对象
2. jQuery 对象[下标]取出相应的Dom 对象

```javascript
alert(document.getElementById("testDiv"));          //dom
alert($(document.getElementById("testDiv")));       //jQuery
alert($(document.getElementById("testDiv"))[0]);    //dom
```

### jQuery选择器（重点）

#### 基本选择器（重点）

#ID	选择器：根据id 查找标签对象

.class 选择器：根据class 查找标签对象

element 选择器：根据标签名查找标签对象

*选择器		： 表示任意的，所有的元素

selector1， selector2 组合选择器：合并选择器1，选择器2的结果并返回

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        div, span, p {
            width: 140px;
            height: 140px;
            margin: 5px;
            background: #aaa;
            border: #000 1px solid;
            float: left;
            font-size: 17px;
            font-family: Verdana;
        }
        div.mini {
            width: 55px;
            height: 55px;
            background-color: #aaa;
            font-size: 12px;
        }
        div.hide {
            display: none;
        }
    </style>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        //1.选择id 为one 的元素"background-color", "#bbffaa"
        $(function () {
            $("#btn1").click(function () {
                //css()方法 可以设置和获取样式
                $("#one").css("background-color", "#bbffaa");
            });
        });
        //2.选择class 为 mini 的所有元素
        $(function () {
            $("#btn2").click(function () {
                $(".mini").css("background", "#bbffaa");
            });
        });
        //3.选择 元素名为 div 的所有元素
        $(function () {
            $("#btn3").click(function () {
                $("div").css("background", "#bbffaa");
            });
        });
        //4.选择所有元素
        $(function () {
           $("#btn4").click(function () {
               $("*").css("background", "#bbffaa");
           });
        });
        //5.选择所有的 span 元素和 id为two 的元素
        $(function () {
            $("#btn5").click(function () {
                $("span, #two").css("background", "#bbffaa");
            });
        });
    </script>
</head>
<body>
    <input type="button" value="选择id 为one的元素" id="btn1"/>
    <input type="button" value="选择class 为 mini 的所有元素" id="btn2"/>
    <input type="button" value="选择 元素名为 div 的所有元素" id="btn3"/>
    <input type="button" value="选择所有元素" id="btn4"/>
    <input type="button" value="选择所有的 span 元素和 id为two 的元素" id="btn5"/>
    <br/>

    <div class="one" id="one">
        id为 one，class为one 的div
        <div class="mini">class 为mini的div</div>
    </div>

    <div class="one" id="two" title="test">
        id为two，class为one，title为test的div
        <div class="mini" title="other">class为mini，title为other</div>
        <div class="mini" title="test">class为mini，title为test</div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini"></div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini" title="tesst">class为mini,title为tesst</div>
    </div>
    <div style="display: none" class="none">style的display为"none"的div</div>
    <div class="hide">class为hide的div</div>
    <div>
        包含input的type为"hidden"的div <input type="hidden" size="8"/>
    </div>
    <span class="one" id="span">^^span元素^^</span>
</body>
</html>
```

#### 层级选择器（重点）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        div, span, p {
            width: 140px;
            height: 140px;
            margin: 5px;
            background: #aaa;
            border: #000 1px solid;
            float: left;
            font-size: 17px;
            font-family: Verdana;
        }
        div.mini {
            width: 55px;
            height: 55px;
            background-color: #aaa;
            font-size: 12px;
        }
        div.hide {
            display: none;
        }
    </style>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {     //$(function(){}); 为这里ready的简写
        //1.选择body 内的所有div元素
            $("#btn1").click(function () {
                $("body div").css("background", "#bbffaa");
            });
        //2.在body 内选择div子元素
            $("#btn2").click(function () {
                $("body > div").css("background", "#bbffaa");
            });
        //3.选择id 为one的下一个div 元素
            $("#btn3").click(function () {
                $("#one + div").css("background", "#bbffaa");
            });
        //4.选择id为two 的元素后的所有div 兄弟元素
            $("#btn4").click(function () {
                $("#two~div").css("background", "#bbffaa");
            });
        });
    </script>
</head>
<body>
    <input type="button" value="选择body 内的所有div元素" id="btn1"/>
    <input type="button" value="在body 内选择div子元素" id="btn2"/>
    <input type="button" value="选择id 为one的下一个div 元素" id="btn3"/>
    <input type="button" value="选择id为two 的元素后的所有div 兄弟元素" id="btn4"/>
    <br/>
    <div class="one" id="one">
        id为 one，class为one 的div
        <div class="mini">class 为mini的div</div>
    </div>
    <div class="one" id="two" title="test">
        id为two，class为one，title为test的div
        <div class="mini" title="other">class为mini，title为other</div>
        <div class="mini" title="test">class为mini，title为test</div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini"></div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini" title="tesst">class为mini,title为tesst</div>
    </div>
    <div style="display: none" class="none">style的display为"none"的div</div>
    <div class="hide">class为hide的div</div>
    <div>
        包含input的type为"hidden"的div <input type="hidden" size="8"/>
    </div>
    <span class="one" id="span">^^span元素^^</span>
</body>
</html>
```

#### 过滤选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        div, span, p {
            width: 140px;
            height: 140px;
            margin: 5px;
            background: #aaa;
            border: #000 1px solid;
            float: left;
            font-size: 17px;
            font-family: Verdana;
        }
        div.mini {
            width: 55px;
            height: 55px;
            background-color: #aaa;
            font-size: 12px;
        }
        div.hide {
            display: none;
        }
    </style>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        $(function () {
           function anmateIt() {
               $("#mover").slideToggle("slow", anmateIt);
           }
           anmateIt();
        });
        $(document).ready(function () {
            //1.选择第一个div 元素
            $("#btn1").click(function () {
                $("div:first").css("background", "#bbffaa");
            });
            //2.选择最后一个div 元素
            $("#btn2").click(function () {
                $("div:last").css("background", "#bbffaa");
            });
            //3.选择class 不为one 的所有div元素
            $("#btn3").click(function () {
                $("div:not(.one)").css("background", "#bbffaa");
            });
            //4.选择索引值为偶数的 div 元素
            $("#btn4").click(function () {
                $("div:even").css("background", "#bbffaa");
            });
            //5.选择索引值为奇书的 div 元素
            $("#btn5").click(function () {
                $("div:odd").css("background", "#bbffaa");
            });
            //6.选择索引值为大于3 的div 元素
            $("#btn6").click(function () {
                $("div:gt(3)").css("background", "#bbffaa");
            });
            //7.选择索引值为等于3 的div 元素
            $("#btn7").click(function () {
                $("div:eq(3)").css("background", "#bbffaa");
            });
            //8.选择索引值为小于3 的div 元素
            $("#btn8").click(function () {
                $("div:lt(3)").css("background", "#bbffaa");
            });
            //9.选择所有的标题元素
            $("#btn9").click(function () {
                $(":header").css("background", "#bbffaa");
            });
            //10.选择当前正在执行动画的所有元素
            $("#btn10").click(function () {
                $(":animated").css("background", "#bbffaa");
            });
            //11.选择没有执行动画的最后一个div
            $("#btn11").click(function () {
                $("div:not(:animated):last").css("background", "#bbffaa");
            });
        });
    </script>
</head>
<body>
    <input type="button" value="选择第一个div 元素" id="btn1"/>
    <input type="button" value="选择最后一个dic 元素" id="btn2"/>
    <input type="button" value="选择class 不为one 的所有div元素" id="btn3"/>
    <input type="button" value="选择索引值为偶数的 div 元素" id="btn4"/>
    <input type="button" value="选择索引值为奇书的 div 元素" id="btn5"/>
    <input type="button" value="选择索引值为大于3 的div 元素" id="btn6"/>
    <input type="button" value="选择索引值为等于3 的div 元素" id="btn7"/>
    <input type="button" value="选择索引值为小于3 的div 元素" id="btn8"/>
    <input type="button" value="选择所有的标题元素" id="btn9"/>
    <input type="button" value="选择当前正在执行动画的所有元素" id="btn10"/>
    <input type="button" value="选择没有执行动画的最后一个div" id="btn11"/>
    <br/><br/>
    <h3>基本选择器.</h3>
    <br/><br/>
    <div class="one" id="one">
        id为 one，class为one 的div
        <div class="mini">class 为mini的div</div>
    </div>
    <div class="one" id="two" title="test">
        id为two，class为one，title为test的div
        <div class="mini" title="other">class为mini，title为other</div>
        <div class="mini" title="test">class为mini，title为test</div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini"></div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini" title="tesst">class为mini,title为tesst</div>
    </div>
    <div style="display: none" class="none">style的display为"none"的div</div>
    <div class="hide">class为hide的div</div>
    <div>
        包含input的type为"hidden"的div <input type="hidden" size="8"/>
    </div>
    <div id="mover">
        正在执行动画的div元素。
    </div>
</body>
</html>
```

基本过滤选择器：

#### 内容过滤器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        div, span, p {
            width: 140px;
            height: 140px;
            margin: 5px;
            background: #aaa;
            border: #000 1px solid;
            float: left;
            font-size: 17px;
            font-family: Verdana;
        }
        div.mini {
            width: 55px;
            height: 55px;
            background-color: #aaa;
            font-size: 12px;
        }
        div.hide {
            display: none;
        }
    </style>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        $(function () {
            function anmateIt() {
                $("#mover").slideToggle("slow", anmateIt);
            }
            anmateIt();
        });
        $(document).ready(function () {
            //1.选择含有文本 "di" 的div 元素
            $("#btn1").click(function () {
                $("div:contains('di')").css("background", "#bbffaa");
            });
            //2.选择不包含子元素(或者文本元素)的 div 空元素
            $("#btn2").click(function () {
                $("div:empty").css("background", "#bbffaa");
            });
            //3.选择含有 class 为mini 元素的div 元素
            $("#btn3").click(function () {
                $("div:has(.mini)").css("background", "#bbffaa");
            });
            //4.选择含有子元素(或者文本元素)的 div元素
            $("#btn4").click(function () {
                $("div:parent").css("background", "#bbffaa");
            });
        });
    </script>
</head>
<body>
    <input type="button" value="选择含有文本 'di' 的div 元素" id="btn1"/>
    <input type="button" value="选择不包含子元素(或者文本元素)的 div 空元素" id="btn2"/>
    <input type="button" value="选择含有 class 为mini 元素的div 元素" id="btn3"/>
    <input type="button" value="选择含有子元素(或者文本元素)的 div元素" id="btn4"/>
    <br/><br/>
    <h3>基本选择器.</h3>
    <br/><br/>
    <div class="one" id="one">
        id为 one，class为one 的div
        <div class="mini">class 为mini的div</div>
    </div>
    <div class="one" id="two" title="test">
        id为two，class为one，title为test的div
        <div class="mini" title="other">class为mini，title为other</div>
        <div class="mini" title="test">class为mini，title为test</div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini"></div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini" title="tesst">class为mini,title为tesst</div>
    </div>
    <div style="display: none" class="none">style的display为"none"的div</div>
    <div class="hide">class为hide的div</div>
    <div>
        包含input的type为"hidden"的div <input type="hidden" size="8"/>
    </div>
    <div id="mover">
        正在执行动画的div元素。
    </div>
</body>
</html>
```

#### 属性过滤器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        div, span, p {
            width: 140px;
            height: 140px;
            margin: 5px;
            background: #aaa;
            border: #000 1px solid;
            float: left;
            font-size: 17px;
            font-family: Verdana;
        }
        div.mini {
            width: 55px;
            height: 55px;
            background-color: #aaa;
            font-size: 12px;
        }
        div.hide {
            display: none;
        }
    </style>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">

        $(function () {
            function anmateIt() {
                $("#mover").slideToggle("slow", anmateIt);
            }
            anmateIt();
        });
        $(document).ready(function () {
            //1.选取含有属性title 的div元素
            $("#btn1").click(function () {
                 $("div[title]").css("background", "#bbffaa");
            });
            //2.选取属性title 值等于'test'的div 元素
            $("#btn2").click(function () {
                $("div[title='test']").css("background", "#bbffaa");
            });
            //3.选取属性title值 不等于'test' 的div元素(没有属性title 的也将被选中)
            $("#btn3").click(function () {
                $("div[title!='test']").css("background", "#bbffaa");
            });
            //4.选取属性 title值 以'te'开始的div 元素
            $("#btn4").click(function () {
                $("div[title^='te']").css("background", "#bbffaa");
            });
            //5.选取属性 title值 以'est'结束的 div元素
            $("#btn5").click(function () {
                $("div[title$='est']").css("background", "#bbffaa");
            });
            //6.选取 属性title值 含有'es' 的div 元素  //含有为 *=
            $("#btn6").click(function () {
                $("div[title*='es']").css("background", "#bbffaa");
            });
            //7.组合属性选择器 首先选取属性id 的div元素，然后在结果中 选取属性title值 含有'es'的div 元素
            $("#btn7").click(function () {
                $("div[id][title*='es']").css("background", "#bbffaa");
            });
            //8.选取含有title 属性值，且title属性值不等于test 的div 元素
            $("#btn8").click(function () {
                $("div[title][title!='test']").css("background", "#bbffaa");
            });
        });
    </script>
</head>
<body>
    <input type="button" value="选取含有属性title 的div元素" id="btn1"/>
    <input type="button" value="选取属性title 值等于'test'的div 元素" id="btn2"/>
    <input type="button" value="选取属性title值 不等于'test' 的div元素(没有属性title 的也将被选中)" id="btn3"/>
    <input type="button" value="选取属性 title值 以'te'开始的div 元素" id="btn4"/>
    <input type="button" value="选取属性 title值 以'est'结束的 div元素" id="btn5"/>
    <input type="button" value="选取 属性title值 含有'es' 的div 元素" id="btn6"/>
    <input type="button" value="组合属性选择器 首先选取属性id 的div元素，然后在结果中 选取属性title值 含有'es'的div 元素" id="btn7"/>
    <input type="button" value="选取含有title 属性值，且title属性值不等于test 的div 元素" id="btn8"/>
    <br/><br/>
    <h3>基本选择器.</h3>
    <br/><br/>
    <div class="one" id="one">
        id为 one，class为one 的div
        <div class="mini">class 为mini的div</div>
    </div>
    <div class="one" id="two" title="test">
        id为two，class为one，title为test的div
        <div class="mini" title="other">class为mini，title为other</div>
        <div class="mini" title="test">class为mini，title为test</div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini"></div>
    </div>
    <div class="one">
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini">class为mini</div>
        <div class="mini" title="tesst">class为mini,title为tesst</div>
    </div>
    <div style="display: none" class="none">style的display为"none"的div</div>
    <div class="hide">class为hide的div</div>
    <div>
        包含input的type为"hidden"的div <input type="hidden" size="8"/>
    </div>
    <div id="mover">
        正在执行动画的div元素。
    </div>
</body>
</html>
```

#### 表单过滤器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        $(function () {
            //1.对表单内可用 input赋值操作
            $("#btn1").click(function () {
                $(":text:enabled").val("我是万能的程序员");
            });
            //2.对表单内不可用 input赋值操作
            $("#btn2").click(function () {
                $(":text:disabled").val("管你可不可用，反正我是万能的程序员");
            });
            //3.获取多选框选中的个数
            $("#btn3").click(function () {
                alert($(":checkbox:checked").length);
            });
            //4.获取多选框中的内容
            $("#btn4").click(function () {
                //获取全部选中的复选框标签对象
                var $checkboies = $(":checkbox:checked");
                //each 方法是jquery 对象提供用来遍历元素的方法
                //在遍历的 function函数中，有一个this 对象，就是当前遍历到的dom 对象
                $checkboies.each(function () {
                    alert(this.value);
                });
                //老式遍历
                // for(var i=0; i<$checkboies.length; i++) {
                //     alert($checkboies[i].value);
                // }
            });
            //5.获取下拉框选中的内容
            $("#btn5").click(function () {
                // 获取选中的 option标签对象
                var $option = $("select option:selected");
                // 遍历，获取option 标签中的文本内容
                $option.each(function () {
                    alert(this.innerHTML);
                });
            });
        });
    </script>
</head>
<body>
    <input type="button" value="对表单内可用 input赋值操作" id="btn1"/>
    <input type="button" value="对表单内不可用 input赋值操作" id="btn2"/>
    <input type="button" value="获取多选框选中的个数" id="btn3"/>
    <input type="button" value="获取多选框中的内容" id="btn4"/>
    <input type="button" value="获取下拉框选中的内容" id="btn5"/>
    <form id="form1" action="#">
        可用元素：<input name="add" value="可用文本框1"/><br/>
        不可用元素：<input name="email" disabled="disabled" value="不可用文本框"/><br/>
        可用元素：<input name="che" value="可用文本框2"/><br/>
        可用元素：<input name="name" disabled="disabled" value="不可用文本框"/>
        <br/>
        多选框：<br/>
        <input type="checkbox" name="newsletter" checked="checked" value="test1"/>test1
        <input type="checkbox" name="newsletter" value="test2"/>test2
        <input type="checkbox" name="newsletter" value="test3"/>test3
        <input type="checkbox" name="newsletter" value="test4"/>test4
        <input type="checkbox" name="newsletter" value="test5"/>test5
        <br/><br/>
        下拉列表1：<br/>
        <select name="test" multiple="multiple" style="..." id="select1">
            <option>浙江</option>
            <option selected="selected">辽宁</option>
            <option>北京</option>
            <option selected="selected">天津</option>
            <option>广州</option>
            <option>湖北</option>
        </select>
        <br/>
        下拉列表2：<br/>
        <select>
            <option>浙江</option>
            <option>辽宁</option>
            <option selected="selected">北京</option>
            <option>天津</option>
            <option>广州</option>
            <option>湖北</option>
        </select>
    </form>
</body>
</html>
```

### jQuery元素筛选

eq()			获取给定索引的元素																			功能跟	:eq() 一样

first()		  获取第一个元素																					功能跟	:first() 一样

last()			获取最后一个元素																				功能跟	:last() 一样

filter(exp)			留下匹配的元素																			

is()				判断是否匹配给定的选择器，只要一个匹配就返回，true

has(exp)		返回包含匹配选择器的元素的元素													功能跟  :has()一样

not(exp)		删除匹配选择器的元素

children(exp)		返回匹配给定选择器的子元素													功能跟  :parent>child 一样

find(exp)		返回匹配给定选择器的后代元素													功能跟  :ancestor descendant一样

next()					返回当前元素的下一个兄弟元素												功能跟	:prev + next 一样

nextAll()			返回当前元素后面所有的兄弟元素												功能跟	:prev + sibling 一样

nextUnit()		返回当前元素到指定匹配的元素为止的后面元素						

parent()			返回父元素

prev(exp)				返回当前元素的上一个兄弟元素

prevAll()			返回当前元素前面所有的兄弟元素

prevUntil(exp)	返回当前元素到指定匹配的元素为止的前面元素

sibilings(exp)		返回所有兄弟元素

add()					把add匹配的选择器的元素添加到当前 jquery 对象中

### jQuery属性操作

html()	 可以设置和获取元素内容,如果有子元素，保留标签.  					和 dom 属性 innerHTML 一样

text()	  可以设置和获取元素内容,如果有子元素，不包含子元素标签    	和 dom 属性 innerText 一样

val() 	  可以设置和获取表单项的 value 值								 				   和 dom 属性 value 一样

```javascript
<script type="text/javascript">
        $(function () {
            //不传参数是获取   ， 传参数为设置

            //html()
            // alert($("div").html() ); //获取
            // $("div").html("<h1>我是在js中设置的标题 1</h1>"); //设置

            //text()
            // alert($("div").text());
            // $("div").text("<h1>我是在js中设置的标题 1</h1>")

            $("button").click(function () {
                alert($("#username").val());        //获取
                $("#username").val("超级程序员");     //设置
            });
        });
    </script>
</head>
<body>
    <div>我是div<span>我是span</span></div>
    <input type="text" name="username" id="username"/>
    <button>操作输入框</button>
</body>
```

attr()	  可以设置和获取属性的值，不推荐操作 checked、readOnly、selected、disabled等；

​				attr还可以去自定义属性 给其赋值。abc=“acbValue”；

prop()	可以设置和获取属性的值，只推荐操作 checked、readOnly、selected、disabled等；

### 全选/全不选/反选 练习

```javascript
<head>
    <meta charset="UTF-8">
    <title>全选/全不选</title>
    <script type="text/javascript" src="https://how2j.cn/study/jquery.min.js"></script>
    <script type="text/javascript">
        $(function () {
            //给全选绑定单击事件
            $("#checkedAllBtn").click(function () {
                $(":checkbox").prop("checked", true);
            });
            //全不选单击事件
            $("#checkedNoBtn").click(function () {
                $(":checkbox").prop("checked", false);
            });
            //反选单击事件
            $("#checkedRevBtn").click(function () {
                //查询全部的球类的复选框
                $(":checkbox[name='items']").each(function () {
                    //在each 遍历的function 中，有一个this 对象，这个this 对象是当前正在遍历的dom 对象。
                    this.checked = !this.checked;
                });
                //要检查 是否满选
                //获取全部的球类个数
                var allCount = $(":checkbox[name='items']").length;
                //获取选中的球类个数
                var checkedCount = $(":checkbox[name='items']:checked").length;

                // if(allCount == checkedCount){
                //     $("#checkAllBox").prop("checked", true);
                // }else {
                //     $("#checkAllBox").prop("checked", false);
                // }

                $("#checkAllBox").prop("checked", allCount == checkedCount);

            });
            //提交单击事件
            $("#sendBtn").click(function () {
                //获取球类选中的复选框
                $(":checkbox[name='items']:checked").each(function () {
                    alert(this.value);
                });
            });
            //全选/全不选单击事件
            $("#checkAllBox").click(function () {
                //在事件的function 函数中，有一个this 对象，这个this 对象是当前正在响应事件的dom 对象
                // alert(this.checked);
                $(":checkbox[name='items']").prop("checked", this.checked);
            });
            //给全部球类绑上单击事件
            $(":checkbox[name='items']").click(function () {
                var allCount = $(":checkbox[name='items']").length;
                var checkedCount = $(":checkbox[name='items']:checked").length;
                // if(allCount == checkedCount) {
                //     $("#checkAllBox").prop("checked", true);
                // }else {
                //     $("#checkAllBox").prop("checked", false);
                // }
                $("#checkAllBox").prop("checked", allCount==checkedCount);
            });

        });

    </script>

</head>
<body>
    <form method="post" action="">
        你爱好的运动是？<input type="checkbox" id="checkAllBox"/>全选/全不选
        <br/>
        <input type="checkbox" name="items" value="足球"/>足球
        <input type="checkbox" name="items" value="篮球"/>篮球
        <input type="checkbox" name="items" value="羽毛球"/>羽毛球
        <input type="checkbox" name="items" value="乒乓球"/>乒乓球
        <br/>
        <input type="button" id="checkedAllBtn" value="全选"/>
        <input type="button" id="checkedNoBtn" value="全不选"/>
        <input type="button" id="checkedRevBtn" value="反选"/>
        <input type="button" id="sendBtn" value="提交"/>
    </form>

</body>
```

### DOM的增/删/改

##### 内部插入：

appendTo()							a.appendTo(b)				把a 插入到b 子元素末尾，成为最后一个子元素

prependTo()							a.prependTo(b)			把a 插入到b 子元素前面，成为第一个子元素

##### 外部插入：

insertAfter()							a.insertAfter(b)				得到ba

insertBefore()						a.insertBefore(b)				得到ab

##### 替换：

replaceWith()						a.replaceWith(b)				用b 替换掉 a

replaceAll()							a.replaceAll(b)					用a 替换掉所有 b

##### 删除：

remove()								a.remove()							删除a 标签

empty()								a.empty()								清空a 标签内的内容


