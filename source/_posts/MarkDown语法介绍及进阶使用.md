---
title: MarkDown语法介绍及进阶使用
date: 2017-05-14 15:20:38
categories: experience
tags: ['markdown','语法教程']
keywords: markdown, 语法教程
description:
top: 1
---
> 断剑重铸之日，骑士归来之时！   --- 向着自由，向着未来出发Aco (๑╹◡╹)ﾉ"""

---

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=30903117&auto=0&height=66"></iframe>


# 什么是markdown？
>Markdown 是一种轻量级的「标记语言」，它的优点很多，目前也被越来越多的写作爱好者，撰稿者广泛使用。看到这里请不要被「标记」、「语言」所迷惑，Markdown 的语法十分简单。常用的标记符号也不超过十个，这种相对于更为复杂的 HTML 标记语言来说，Markdown 可谓是十分轻量的，学习成本也不需要太多，且一旦熟悉这种语法规则，会有一劳永逸的效果。
<!--more-->

# MarkDown简单语法应用
> 这些简单语法很多博客上都有，我就不意义赘述了，附上参考链接 <http://www.jianshu.com/p/1e402922ee32/>算了还是写进博客吧，免得新开页面~(^_−)☆
直接看效果和例子->

## 1. 标题
** --> 例子**

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

** --> 效果**

># 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

## 2. 列表
分为有序列表和无序列表，用`- + * `实现，不过符号之后的空格不能少，-+*效果一样，但不能混合使用(列表快块要用就用一样的)，因混合是嵌套列表，内容可超长
### 2.1 无序列表
** --> 例子**

```
- 无序列表
- 无序列表
- 无序列表
- 无序列表：测试长文本，Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World (超长会自动换行)
```

** --> 效果**

- 无序列表
- 无序列表
- 无序列表
- 无序列表：测试长文本，Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World Hello World (超长会自动换行)

### 2.2 有序列表
自己添加数字，如果无序会自动转换成有序
** --> 例子**

```
b. 有序列表
5. 有序列表
3. 有序列表
```

** --> 效果**

2. 有序列表
5. 有序列表
3. 有序列表

### 2.3 嵌套列表
** --> 例子**

```
- 嵌套列表
 + 嵌套列表
 + 嵌套列表
  - 嵌套列表
   * 嵌套列表
- 嵌套列表
```

** --> 效果**

- 嵌套列表
 + 嵌套列表
 + 嵌套列表
  - 嵌套列表
   * 嵌套列表
- 嵌套列表

(hexo博客的markdown渲染不出来？。。。大家可以在markdown编辑器或者有支持markdown的插件里试一下，可以实现嵌套)

## 3. 引用
这个简单，只需要在文本前加入 > 这种尖括号（大于号）即可，如果想要多层签套，那么多加几个>即可
** --> 例子**

```
> Hello World!
>> Hello World!
>>> Hello World!

```

** --> 效果**

> Hello World!
>> Hello World!
>>> Hello World!

**[注]** 代码区块的引用，直接tab键就可以形成一个区块，里面的Markdown 语法都会作为文本显示

## 4. 图片与链接
插入链接与插入图片的语法很像，区别在一个 !号
图片为：`![](){ImgCap}{/ImgCap}`
链接为：`[]()`

插入图片的地址需要图床，我用的是新浪微博相册的图床，右键辅复制图片URL地址即可。
### 4.1 图片
** --> 例子**

```
![提示信息](http://wx4.sinaimg.cn/mw690/006xRFa6gy1ffldjgxu9bj31hc0u0b29.jpg)
```

** --> 效果**

![提示信息](http://wx4.sinaimg.cn/mw690/006xRFa6gy1ffldjgxu9bj31hc0u0b29.jpg)

### 4.2 链接
** --> 例子**

```
[显示的文本](链接 "提示信息")
[哔哩哔哩](www.bilibili.com)
```
** --> 效果**

[哔哩哔哩](www.bilibili.com "B站")

## 5. 粗体与斜体
Markdown 的粗体和斜体也非常简单，用两个` ** / __`包含一段文本就是粗体的语法，用一个` * / _`包含一段文本就是斜体的语法。
星号与下划线都可以，单是斜体，双是粗体，符号可跨行，符号可加空格
** --> 例子**

```
**Hello World**
** Hello World **
__Hello World__

** Hello
World **

*Hello
world*

_Hello World_
```

** --> 效果**

**Hello World**
** Hello World **
__Hello World__

** Hello
World **

*Hello
world*

_Hello World_

## 6. 表格
表格如果用markdown语法解决的话，超麻烦,后面优化里会有解决办法
** --> 例子**

```
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

header 1 | header 2 | header 3
---|---|---
row 1 col 1 | row 1 col 2 |  row 2 col 3
row 2 col 1 | row 2 col 2 |  row 3 col 3
```

** --> 效果**

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

header 1 | header 2 | header 3
---|---|---
row 1 col 1 | row 1 col 2 |  row 2 col 3
row 2 col 1 | row 2 col 2 |  row 3 col 3

## 7. 代码框
如果你是个程序猿，需要在文章里优雅的引用代码框，在 Markdown下实现也非常简单，只需要用两个 \` \` 把中间的代码包裹起来。
### 7.1 普通短文本代码
** --> 例子**

```
`Hello`
```

** --> 效果**

`Hello`

### 7.2 代码：段落代码
每行文字前加4个空格或者1个Tab,当代码很长，用三个\`\`\`  \`\`\`
** --> 例子**


    val s = "hello Markdown"
    println( s )
    val s = "hello Markdown"
    println( s )


** --> 效果**

    val s = "hello Markdown"
    println( s )
    val s = "hello Markdown"
    println( s )
    

## 8. 分割线
三个或更多`-_*`，必须单独一行，可含空格
大标题: `===`
小标题: `---`
** --> 例子**

```
---
***
___
```

** --> 效果**
---
***
___


# MarkDown进阶
> 一句话，markdown支持html语法！！！这意味着什么？
如果发现新功能，之后会计时更新补充(^_−)☆

## 1. 支持基本的HTML标签
### 图片居中
利用center标签
** --> 例子**

```
<center>![提示信息](http://wx4.sinaimg.cn/mw690/006xRFa6gy1ffldjgxu9bj31hc0u0b29.jpg)</center>
```

** --> 效果**

<center>![提示信息](http://wx4.sinaimg.cn/mw690/006xRFa6gy1ffldjgxu9bj31hc0u0b29.jpg)</center>

### 字体
** --> 例子**

```
<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=#0099ff size=12 face="黑体">黑体</font>
<font color=#00ffff size=3>null</font>
<font color=gray size=5>gray</font>
```

** --> 效果**

<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=#0099ff size=12 face="黑体">黑体</font>
<font color=red size=12>Hello World</font>
<font color=#00ffff size=3>null</font>
<font color=gray size=5>gray</font>

### 表格
** --> 例子**

```
<table>
  <caption>实现markdown表格</caption>
   <thead>
        <td>第一列</td>
        <td>第二列</td>
        <td>第三列</td>
   </thead>
   <tbody>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    </tbody>
</table>
```
(应该是hexo的markdown渲染问题，原理上不应该显示那么大一片空白的，其他编辑器里可以正常显示)
** --> 效果**
<table>
  <caption>实现markdown表格</caption>
   <thead>
        <td>第一列</td>
        <td>第二列</td>
        <td>第三列</td>
   </thead>
   <tbody>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
    </tr>
    </tbody>
</table>

### 注释
** --> 例子**

```
<!-- 注释 -->
```

** --> 效果**

<!-- 注释 -->

## 2. 特殊一点的技巧
### 索引超链：Reference方式
索引，1 可以是任意字符
** --> 例子**

```
[哔哩哔哩][1]
[Github][2]
[1]:www.bilibili.com
[2]:www.github.com
```

** --> 效果**

[哔哩哔哩][1]
[Github][2]
[1]:www.bilibili.com
[2]:www.github.com

### 自动链接
尖括号
** --> 例子**

```
<http://www.baidu.com>
<2973978759@qq.com>
```

** --> 效果**

<http://www.baidu.com>
<2973978759@qq.com>

### 转义字符
Markdown中的转义字符为\，转义的有：

\\ 反斜杠
\` 反引号
\* 星号
\_ 下划线
\{\} 大括号
\[\] 中括号
\(\) 小括号
\# 井号
\+ 加号
\- 减号
\. 英文句号
\! 感叹号


## 3. 支持导入css样式表
这里只举两个例子
### 让你的文章可以显示QQ小表情
导入一个css库即可
** --> 例子**

```
<link href="https://afeld.github.io/emoji-css/emoji.css" rel="stylesheet">
<div class="em em-trollface" style=" height: 100px; width: 100px; background-color: red;"></div>
    <i class="em em-trollface"></i>
    <i class="em em-angry"></i>
    <i class="em em-apple"></i>
    <i class="em em-astonished"></i>
    <i class="em em-blush"></i>
    <i class="em em-confounded"></i>
```

** --> 效果**

<link href="https://afeld.github.io/emoji-css/emoji.css" rel="stylesheet">
<div class="em em-trollface" style=" height: 100px; width: 100px; background-color: red;"></div>
    <i class="em em-trollface"></i>
    <i class="em em-angry"></i>
    <i class="em em-apple"></i>
    <i class="em em-astonished"></i>
    <i class="em em-blush"></i>
    <i class="em em-confounded"></i>


### 页面显示CSS3的动画效果

** --> 例子**

``` html
<style>
.test
{
	width:100px;
	height:100px;
	background:red;
	position:relative;
	animation:myfirst 5s linear 2s infinite alternate;
	/* Firefox: */
	-moz-animation:myfirst 5s linear 2s infinite alternate;
	/* Safari and Chrome: */
	-webkit-animation:myfirst 5s linear 2s infinite alternate;
	/* Opera: */
	-o-animation:myfirst 5s linear 2s infinite alternate;
}

@keyframes myfirst
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}

@-moz-keyframes myfirst /* Firefox */
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}

@-webkit-keyframes myfirst /* Safari and Chrome */
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}

@-o-keyframes myfirst /* Opera */
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}
</style>

<div class="test"></div>
```

** --> 效果**
(hexo的渲染又出问题了，本地是显示正常的...因此我只能发个截图了，大家自己操作看效果)
![](http://wx3.sinaimg.cn/mw690/006xRFa6gy1fflft8hxkeg30c90ap0tn.gif)

<style>
.test
{
	width:100px;
	height:100px;
	background:red;
	position:relative;
	animation:myfirst 5s linear 2s infinite alternate;
	/* Firefox: */
	-moz-animation:myfirst 5s linear 2s infinite alternate;
	/* Safari and Chrome: */
	-webkit-animation:myfirst 5s linear 2s infinite alternate;
	/* Opera: */
	-o-animation:myfirst 5s linear 2s infinite alternate;
}

@keyframes myfirst
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}

@-moz-keyframes myfirst /* Firefox */
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}

@-webkit-keyframes myfirst /* Safari and Chrome */
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}

@-o-keyframes myfirst /* Opera */
{
	0%   {background:red; left:0px; top:0px;}
	25%  {background:yellow; left:200px; top:0px;}
	50%  {background:blue; left:200px; top:200px;}
	75%  {background:green; left:0px; top:200px;}
	100% {background:red; left:0px; top:0px;}
}
</style>

<div class="test"></div>
















