------

# HTML5

------

### 图像

![image-20211007101213366](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101213366.png)

### 链接

```
打开方式：
	target:值;
			_blank 新窗口
			_self 同一窗口
			_parent 上一窗口
```

### 锚点定位

```
<h3 id="值"></h3>

<a href="#值">
```

### 表格

```
<table>
    <thead>
        <tr>
            <th>排名</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>鬼吹灯</td>
            <td><img src="down.jpg"></td>
            <td>456</td>
            <td>123</td>
            <td> <a href="#">贴吧</a> <a href="#">图片</a> <a href="#">百科</a> </td>
        </tr>
    </tbody>           
    </table>
```

**合并单元格**：

```
 rowspan="行数"   collspan="列数"
```

![image-20211007105003924](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007105003924.png)

### 列表

无序列表样式：

```
type="值"  disc小黑圆点（默认）；circle空心圆点；square小黑方块
```

### 表单

```
 <form action="xxx.php" method="get">
     <input type="text" >   
 </form>
```

![image-20211007101240881](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101240881.png)

​	*<u>再使用文件上传时使用multipart/form-data</u>*(一个一个提交)

​	*<u>全部提交使用第一种值</u>*

​	enctype： 属性规定在发送到服务器之前应该如何对表单数据进行编码。

```
<form enctype="value">
```

**![image-20211007110506083](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007110506083.png)**

####  type属性

![image-20211007101319191](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101319191.png)

#### label 标签

<label for="sex">男</label>

    <input type="radio" name="sex"  id="sex" />

#### select表单元素

<label for="sex">男</label>

    <input type="radio" name="sex"  id="sex" />
    核心： <label> 标签的 for 属性应当与相关元素的 id 属性相同。

#### textarea表单元素

1. 使用场景: 当用户输入内容较多的情况下，我们就不能使用文本框表单了，此时我们可以使用 <textarea> 标签。
2. 在表单元素中，<textarea> 标签是用于定义多行文本输入的控件。
3. 使用多行文本输入控件，可以输入更多的文字，该控件常见于留言板，评论。

语法：

	<textarea rows="3" cols="20">  文本内容 </textarea>

### 语义化标签

`<header>` 头部标签

`<nav>` 导航标签

`<article>` 内容标签

`<section>` 定义文档某个区域

`<aside>` 侧边栏标签

`<footer>` 尾部标签

### 多媒体标签

#### 视频标签- video

```
<video src="media/mi.mp4"></video>
```

兼容写法

```
<video  controls="controls"  width="300">
    <source src="move.ogg" type="video/ogg" >
    <source src="move.mp4" type="video/mp4" >
    您的浏览器暂不支持 <video> 标签播放视频
</ video >
```

video 常用属性

![image-20211007101344785](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101344785.png)

#### 音频标签- audio

```
<audio src="media/music.mp3"></audio>
```

兼容写法

```
< audio controls="controls"  >
    <source src="happy.mp3" type="audio/mpeg" >
    <source src="happy.ogg" type="audio/ogg" >
    您的浏览器暂不支持 <audio> 标签。
</ audio>
```

audio 常用属性

![image-20211007101358570](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101358570.png)

### 新增的表单元素

#### type

```
<!-- 我们验证的时候必须添加form表单域 -->
<form action="">
    <ul>
        <li>邮箱: <input type="email" /></li>
        <li>网址: <input type="url" /></li>
        <li>日期: <input type="date" /></li>
        <li>时间: <input type="time" /></li>
        <li>数量: <input type="number" /></li>
        <li>手机号码: <input type="tel" /></li>
        <li>搜索: <input type="search" /></li>
        <li>颜色: <input type="color" /></li>
        <!-- 当我们点击提交按钮就可以验证表单了 -->
        <li> <input type="submit" value="提交"></li>
    </ul>
</form>
```

![image-20211007101715067](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101715067.png)

#### input

![image-20211007101729472](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101729472.png)

------

# CSS3

------

### 选择器

#### 基础选择器

##### 1、标签选择器

```
 标签选择器{
        属性：属性值
        ...
  }
```

##### 2、类选择器

```
 .类名 {
        属性1: 属性值1;  
        ...
 } 
 
  <div class="类名"> 变红色 </div>
```

##### 3、id选择器

```
 #类名 {
            属性1: 属性值1;  
            ...
 } 
 
   <div id="类名"> 变红色 </div>
```

##### 4、通配符选择器

```
 * {
    margin: 0;
    padding: 0;
 } 
```

#### 复合选择器

##### 1、后代选择器

**定义**：后代选择器又称为包含选择器，可以选择父元素里面子元素。其写法就是把外层标签写在前面，内层标签写在后面，中间用空格分隔。当标签发生嵌套时，内层标签就成为外层标签的后代。

**语法：**	

```
ul li {  }

//元素1 是父级，元素2 是子级，最终选择的是元素2
//元素2 可以是儿子，也可以是孙子等，只要是元素1 的后代即可
```

##### 2、子选择器

**定义：**子元素选择器（子选择器）只能选择作为某元素的最近一级子元素。（简单理解就是选亲儿子元素）。

**语法**：

```
div > p {}

//元素1 和 元素2 中间用 大于号 隔开
//元素1 是父级，元素2 是子级，最终选择的是元素2
//元素2 必须是亲儿子，其孙子、重孙之类都不归他管. 你也可以叫他 亲儿子选择器
```

##### 3、并集选择器 

**定义：**并集选择器可以选择多组标签, 同时为他们定义相同的样式，通常用于集体声明。并集选择器是各选择器通过英文逗号（,）连接而成，任何形式的选择器都可以作为并集选择器的一部分。

**语法：**

```
ul, 
div  {

}

//元素1 和 元素2 中间用逗号隔开
//并集选择器通常用于集体声明
```

##### 4、交集选择器 

**定义：**既是又是。

**语法：**

```
p.red {}
 
<p class="red">
```

##### 5、链接伪类选择器

**定义：**伪类选择器用于向某些选择器添加特殊的效果，比如给链接添加特殊效果，或选择第1个，第n个元素。

**语法：**

```
	a:link	没有点击过的(访问过的)链接
	a:visited	点击过的(访问过的)链接
	a:hover	鼠标经过的那个链接
	a:active	鼠标正在按下还没有弹起鼠标的那个链接
	
	//**链接伪类选择器注意事项**
		为了确保生效，请按照 LVHA 的循顺序声明 :link－:visited－:hover－:active。
```

##### 6、属性选择器

根据标签中的属性来选择元素

![image-20211007101920043](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101920043.png)

##### 7、结构伪类选择器

结构伪类选择器主要根据文档结构来选择器元素， 常用于根据父级选择器里面的子元素。

![image-20211007101933924](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101933924.png)

奇数：odd          偶数：even

##### 8、结构伪类选择器

伪元素选择器可以帮助我们利用CSS创建新标签元素，而不需要HTML标签，从而简化HTML结构。

![image-20211007101947936](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007101947936.png)

***注意：***

1、before 和 after 创建一个元素，但是属于行内元素

2、新创建的这个元素在文档树中是找不到的，所以我们称为伪元素

3、语法：  element::before {}   

4、before 和 after 必须有 content 属性 

5、before 在父元素内容的前面创建元素，after 在父元素内容的后面插入元素
伪元素选择器和标签选择器一样，权重为 1。

##### 9、:focus 伪类选择器

**定义：**:focus 伪类选择器用于选取获得焦点的表单元素。焦点就是光标，一般情况 <input> 类表单元素才能获取。

#### 优先级

!important > style="" > id选择器(100) > 类选择器(10) > 标签选择器(1) > 继承/*



与类选择器(10)相同：属性选择器、伪类选择器；

与标签选择器(1) 相同：结构伪类选择器；

------

### 文本属性

#### 字体

| 描述       | 语法                                                         |
| ---------- | ------------------------------------------------------------ |
| 字体大小   | font-size: 20px;                                             |
| 字体       | font-family: '宋体'；-->字体间用“，”隔开；中文要用‘’‘’括起来； |
| 字体的粗细 | font-weight: bold;  --> 默认不加粗normal=400;   加粗bold=700； |
| 字体的风格 | font-style: normal; -->normal标准字体；italic倾斜字体；      |

综合写法：

​		font: font-style  font-weight  font-size/line-height  font-family;

#### 常用属性

| 描述                   | 语法                                                         |
| ---------------------- | ------------------------------------------------------------ |
| 文本内容的水平对齐方式 | text-align: center;   -->left 、right                        |
| 修饰文本（下划线）     | text-decoration：none/underline；                            |
| 文本缩进               | text-indent：2em；                                           |
| 堆叠顺序               | z-index: 1; -->**属性值**：**正整数**、**负整数**或 **0**，默认值是 0，数值越大，盒子越靠上； |
| 行高                   | line-height: 26px;                                           |

#### 元素显示模式的分类

##### 1、块元素

```
<h1>~<h6>、<p>、<div>、<ul>、<ol>、<li>
```

**块级元素的特点**：

​	1、比较霸道，自己独占一行。

​	2、高度，宽度、外边距以及内边距都可以控制。

​	3、宽度默认是容器（父级宽度）的100%。

​	4、是一个容器及盒子，里面可以放行内或者块级元素。

##### 2、行内元素

```
<a>、<strong>、<b>、<em>、<i>、<del>、<s>、<ins>、<u>、<span>
```

**行内元素的特点：**

​	1、相邻行内元素在一行上，一行可以显示多个。

​	2、高、宽直接设置是无效的。

​	3、默认宽度就是它本身内容的宽度。

​	4、行内元素只能容纳文本或其他行内元素。

##### 3、行内块元素

```
<img />、<input />、<td>
```

**行内块元素的特点**：

​	1、和相邻行内元素（行内块）在一行上，但是他们之间会有空白缝隙。

​	2、一行可以显示多个（行内元素特点）。

​	3、默认宽度就是它本身内容的宽度（行内元素特点）。

​	4、高度，行高、外边距以及内边距都可以控制（块级元素特点）。

##### 4、元素显示模式的转换

**转换方式**

- 转换为块元素：display:block;
- 转换为行内元素：display:inline;
- 转换为行内块：display: inline-block;

#### 背景

| 描述         | 语法                                                         |
| ------------ | ------------------------------------------------------------ |
| 背景颜色     | background-color：颜色值；                                   |
| 背景图片     | background-image：url(路径)；                                |
| 背景平铺     | background-repeat：值；-->repeat平铺；no-repeat不平铺；repeat-x水平平铺；repeat-y垂直平铺； |
| 背景图片固定 | background-attachment：值；-->scoll滚动；fiexd固定；         |
| 背景图片位置 | background-position：X Y；                                   |
| 背景色半透明 | background: rgba(0, 0, 0, .3);                               |
| 背景图片大小 | background-size：宽度  高度；-->cover两边都铺满；contain铺满一边即可； |

综合写法：

​		background: 背景颜色 背景图片地址 背景平铺 背景图像滚动 背景图片位置;

```
background ： [background-color] | [background-image]|[background-repeat] | [background-position][/background-size] | 
```

扩展：

​		opacity：0~1；   -->透明度

------

### 边框

| 描述     | 语法                                                         |
| -------- | ------------------------------------------------------------ |
| 边框粗细 | border-width：10px；                                         |
| 边框样式 | border-style：值；  -->solid边框为单实线(最为常用的)；dashed边框为虚线；  dotted边框为点线； |
| 边框颜色 | border-color：值；                                           |

综合写法：

​		 border : border-width  border-style  border-color; 

#### 圆角边框

语法：

```
 border-radius:length;  
```

- 参数值可以为数值或百分比的形式
- 如果是正方形，想要设置为一个圆，把数值修改为高度或者宽度的一半即可，或者直接写为 50%
- 该属性是一个简写属性，可以跟四个值，分别代表左上角、右上角、右下角、左下角
- 分开写：border-top-left-radius、border-top-right-radius、border-bottom-right-radius 和border-bottom-left-radius
- 兼容性 ie9+ 浏览器支持, 但是不会影响页面布局,可以放心使用

#### 表格的细线边框

1、border-collapse 属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框。

2、语法：

```
 border-collapse:collapse; 
```

------

### 内外边距

#### 1、内边距

​	定义：padding 属性用于设置内边距，即边框与内容之间的距离。

![image-20210815163609199](C:\Users\LEO\AppData\Roaming\Typora\typora-user-images\image-20210815163609199.png)

内边距会影响盒子实际大小：

​		1、当我们给盒子指定 padding 值之后，发生了 2 件事情：

​					内容和边框有了距离，添加了内边距。

​					padding影响了盒子实际大小。

​		2、内边距对盒子大小的影响：

​					如果盒子已经有了宽度和高度，此时再指定内边框，会撑大盒子。

​					如何盒子本身没有指定width/height属性, 则此时padding不会撑开盒子大小。

​		3、解决方案：

​					如果保证盒子跟效果图大小保持一致，则让 width/height 减去多出来的内边距大小即可。

#### 2、外边距

定义：margin 属性用于设置外边距，即控制盒子和盒子之间的距离。

![image-20211007102013366](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102013366.png)

**问题：嵌套块元素垂直外边距的塌陷**

​		对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会塌陷较大的外边距值。

解决方案：

​		1、可以为父元素定义上边框。

​		2、可以为父元素定义上内边距。

​		3、可以为父元素添加 overflow:hidden。

------

### 浮动

语法：

```
选择器 { float: 属性值; }
```

![image-20211007102026293](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102026293.png)

#### 清除浮动

原因：由于父级盒子很多情况下，不方便给高度，但是子盒子浮动又不占有位置，最后父级盒子高度为 0 时，就会影响下面的标准流盒子。

##### 1、额外标签法

额外标签法会在浮动元素末尾添加一个空的标签。

```
例如 <div style="clear:both"></div>，或者其他标签（如<br />等）。
```

##### 2、父级添加 overflow 属性

可以给父级添加 overflow 属性，将其属性值设置为 hidden、 auto 或 scroll 。

```
overflow:hidden | auto | scroll;
```

##### 3、父级添加after伪元素

```
  <div class="clearfix"></div>
 
 .clearfix:after {  
   content: ""; 
   display: block; 
   height: 0; 
   clear: both; 
   visibility: hidden;  
 } 
 .clearfix {  /* IE6、7 专有 */ 
   *zoom: 1;
 }   
```

##### 4、父级添加双伪元素

```
 .clearfix:before,
 .clearfix:after {
   content:"";
   display:table; 
 }
 .clearfix:after {
   clear:both;
 }
 .clearfix {
    *zoom:1;
 }   
```



------

### 元素的显示与隐藏

#### 	1、display	显示

```
display: none 隐藏对象

display：block 除了转换为块级元素之外，同时还有显示元素的意思。
```

特点： display 隐藏元素后，**不再占**有原来的位置。

#### 	2、visibility	可见性 

```
visibility：visible ; 　元素可视

visibility：hidden; 　  元素隐藏
```

特点：visibility 隐藏元素后，继续占有原来的位置。（停职留薪）

#### 	3、overflow	溢出

| 属性值      | 描述                                       |
| ----------- | ------------------------------------------ |
| **visible** | 不剪切内容也不添加滚动条                   |
| **hidden**  | 不显示超过对象尺寸的内容，超出的部分隐藏掉 |
| **scroll**  | 不管超出内容否，总是显示滚动条             |
| **auto**    | 超出自动显示滚动条，不超出不显示滚动条     |

实际开发场景：

​	1、清除浮动；

​	2、隐藏超出内容，隐藏掉,  不允许内容超过父盒子。

------

### CSS 用户界面样式

#### 1、 鼠标样式 cursor

语法： cursor: 属性值; 

| 属性值      | 描述         |
| ----------- | ------------ |
| default     | 小白（默认） |
| pointer     | 小手         |
| move        | 移动         |
| text        | 文本         |
| not-allowed | 禁止         |

#### 2、轮廓线 outline

给表单添加 outline: 0;   或者  outline: none; 样式之后，就可以去掉默认的蓝色边框。

#### 3、防止拖拽文本域 resize

语法：resize: none;

------

### vertical-align 属性应用（垂直对齐）

CSS 的 **vertical-align** 属性使用场景： 经常用于设置图片或者表单(行内块元素）和文字垂直对齐。

官方解释： 用于设置一个元素的**垂直对齐方式**，但是它只针对于行内元素或者行内块元素有效。

语法：

```
vertical-align : baseline | top | middle | bottom 
```

![image-20211007102051585](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102051585.png)

应用：

​		1、图片、表单和文字对齐

​					给图片、表单这些行内块元素的 **vertical-align 属性设置为 middle** 就可以让文字和图片垂直居中对齐了。

​		2、解决图片底部默认空白缝隙问题

​					主要解决方法有两种：

​							1.**给图片**添加 **vertical-align:middle | top| bottom** 等。 （提倡使用的）

​							2.把图片转换为块级元素  **display: block**; 

------

### 溢出的文字省略号显示

#### 单行

```
  /*1. 先强制一行内显示文本*/
   white-space: nowrap;  （ 默认 normal 自动换行）
   
  /*2. 超出的部分隐藏*/
   overflow: hidden;
   
  /*3. 文字用省略号替代超出的部分*/
   text-overflow: ellipsis;
```

#### 多行

```
  overflow: hidden;
  text-overflow: ellipsis;
  /* 弹性伸缩盒子模型显示 */
  display: -webkit-box;
  /* 限制在一个块元素显示的文本的行数 */
  -webkit-line-clamp: 2;
  /* 设置或检索伸缩盒对象的子元素的排列方式 */
  -webkit-box-orient: vertical;
```



------

### 网站优化三大标签TDK及favicon图标

```
<!--页面介绍-->
<meta name="description" content="内容">

<!--关键字-->
<meta name="keywords" content="内容">

<!--网站标题-->
<title>品优购</title>

<!-- 引入favicon.ico网页图标 -->
<link rel="shortcut icon" href="路径">
```

#### favicon图标的制作

网站：https://www.bitbug.net/

![image-20211007102110960](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102110960.png)

------

### 字体图标

网站：https://www.iconfont.cn/

#### 使用：

##### 		第一种：Unicode编码

​				步骤：

​						引入样式表：iconfont.css

​						复制粘贴图标对应的Unicode编码

​						设置文字字体

```
                                   例子

引入：
<link rel="stylesheet" href="./iconfont/iconfont.css">

使用：
.side-nav .bd li::after {
    content: "\e6fc";
    font-family: "iconfont";
}
```

##### 		第二种：类名

​				步骤：

​						引入样式表：iconfont.css

​						调用图标对应的类名，必须调用2个类名

```
                                   例子

引入：
<link rel="stylesheet" href="./iconfont/iconfont.css">

使用：
 <span class="iconfont icon-yjt"></span>
 			l iconfont类：基本样式，包含字体的使用等
			2 icon-xxx：图标对应的类名
```

#### 上传：

需要将svg格式图标上传到iconfont得网，站然后下载使用；

------

### 转换transform

#### 	平面转换（2D转换）

###### 				1、位移	translate

​					语法：transform: translate(X,Y);

​							单独设置某个方向的移动距离：translateX() & translateY()；

​					单位：

​							像素单位数值；

​							百分比（参照物为盒子自身尺寸；

###### 				2、旋转	rotate

​					语法：transform: rotate(数字deg);

​							正值：顺时针旋转 ；负值：逆时针旋转 ;

​					单位：

​							deg;

###### 				3、缩放	scale

​					语法：transform: scale(x,y);

​					实际的用法：transform: scale(1);

​							实际开发中取值可以是1个，表示等比缩放，如果取值为1表示原始大小不缩放，如果取值大于1表示放大的倍数，如果取值小于1表示缩小的倍数;

###### 				4、中心点（原点）设置	transform-origin

​					语法：transform-origin: center center;(默认原点为中心点);

###### 				5、复合写法

​					语法：transform: 位移  旋转   缩放;

​					注意：translate位移必须要写在最前面，如果旋转在最前面会导致坐标轴的位置偏移，导致问题；

#### 	空间转换（3D转换）

###### 				1、位移	translate

​					复合书写：translate3d(x,y,z);

​							单独设置某个方向的移动距离：translateX() & translateY() & translateZ()；

​					单位：

​							像素单位数值；

​							百分比（参照物为盒子自身尺寸；

###### 				2、旋转	rotate

​					复合书写：transform: rotate3d(x,y,z,angle);	(用来设置自定义旋转的位置及旋转的角度，x,y,z的取值是0或者1,0表示没有，1表示有；)

​					单独设置某个方向的移动距离：rotateX() &rotateY() & rotateZ()；

​							正值：顺时针旋转 ；负值：逆时针旋转 ;

​					单位：

​							deg;

###### 				3、透视	perspective

​					语法：perspective: 800~1200;

​					注意：属性添加给父级；近大远小、近实远虚；

###### 				4、3D呈现	preserve-3d

​					语法：transform-style: preserve-3d；

​					注意：属性添加给父级；

###### 				5、缩放	scale（了解）

​					语法：transform: scale3d(x, y, z);

​					实际的用法：transform: scale(1);

​							实际开发中取值可以是1个，表示等比缩放，如果取值为1表示原始大小不缩放，如果取值大于1表示放大的倍数，如果取值小于1表示缩小的倍数;

------

### 线性渐变

 用法：linear-gradient(颜色1, 颜色2,颜色3,...)

（设置正常从上到下渐变）

![image-20211007102137938](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102137938.png)

设置渐变的角度：linear-gradient(60deg, red, green)     60度可以换成方位名词（top left, red, blue）

![image-20211007102147496](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102147496.png)

透明渐变：linear-gradient(transparent, rgba(0, 0, 0, .3))

![image-20211007102158335](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102158335.png)

------

### 过渡动画

语法：transition:  属性  动画时间   动画形式  延时;

常用用法：transition: 属性  动画时间 ;

​		

动画形式：

| 默认 ease                     |
| ----------------------------- |
| 匀速 linear                   |
| ease-in以慢速开始 ；          |
| ease-out以慢速结束 ；         |
| ease-in-out以慢速开始和结束； |

------

### 关键帧动画

#### 实现步骤

第一步：定义关键帧动画 @keyframes

```
        @keyframes 动画名称 {
            0% {}

            ...% {}

            100% {}
        }
        
        或者
        
       	@keyframes 动画名称 {
            from {}

            to {}
        }
```

第二步：调用动画

animation: name duration timing-function delay iteration-count direction fill-mode;

animation: 动画名称  动画时长  速度曲线  延迟时间  重复次数  动画方向 执行完毕时的状态;

| animation-name                | 规定 @keyframes 动画的名称。（必须有）                       |
| ----------------------------- | ------------------------------------------------------------ |
| **animation-duration**        | 规定动画完成一个周期所花费的秒或毫秒。默认是 0。（必须有）   |
| animation-timing-function     | 规定动画的速度曲线。默认是 "ease"。steps(步数)   逐帧（步长）动画设置动画完成需要多少帧（步数）；linear	动画从头到尾的速度是相同的。 |
| animation-delay               | 规定动画何时开始。默认是 0。必须写单位s。                    |
| **animation-iteration-count** | 规定动画被播放的次数。默认是 1。循环是infinite；             |
| **animation-direction**       | 规定动画是否在下一周期逆向地播放。默认是 “normal”。  alternate逆向 |
| animation-play-state          | 规定动画是否正在运行或暂停。默认是 "running“,暂停是paused。  |
| **animation-fill-mode**       | 规定对象动画时间之外的状态。保持现状forwards，回到起始backwards。 |

***注意***：

1、animation-iteration-count和animation-fill-mode不能同时出现，同时出现时animation-fill-mode不生效；

2、实际开发中一个元素可以同时调用多组动画，animation在调用动画的时候用英文逗号隔开即可；

------

### 动画库

网站：http://www.dowebok.com/demo/2014/98/

使用步骤：	

​		1、下载并引入.css文件；

​		2、调用（效果看官网）

```
<span class="box animated 类名">

//animated:表示调用了动画库；
//类名：从动画库查找
```

实现页面滚动到某一个位置再去加载动画，需要配合一个wow.js插件

​		使用步骤：

​				1、将代码复制到自己的html结构的最后面 ；

```
<script src="js/wow.min.js"></script>
<script type="text/javascript">
        /*初始化自动动画wow.min.js插件*/
        new WOW().init();
</script>
```

​				2、调用;(在class调用wow类名)

```
 <div class=" animated bounceIn wow">44</div>
```

------

### CSS3滤镜filter

定义：图标模糊处理。

filter:   函数()；

例如： filter: blur(5px)；    -->  blur模糊处理  数值越大越模糊

------

### calc 函数

含义：calc() 此CSS函数让你在声明CSS属性值时执行一些计算

语法：width: calc(100% - 80px); 	 -->括号里面可以使用 + - *  / 来进行计算

------

### 盒子模型

可以分成两种情况：

​		1、box-sizing: content-box  盒子大小为 width + padding + border  （以前默认的）

​		2、box-sizing: border-box  盒子大小为 width

如果盒子模型我们改为了box-sizing: border-box  ， 那padding和border就不会撑大盒子了（前提padding和border不会超过width宽度）

------

### 阴影

#### 1、盒子阴影

```
box-shadow: h-shadow v-shadow blur spread color inset;
```

![image-20211007102218851](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102218851.png)

#### 2、文字阴影

```
text-shadow: h-shadow v-shadow blur color;
```

![image-20211007102228783](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102228783.png)

------

###  定位

定位 = 定位模式 + 边偏移

#### 1、静态定位(static)

​	静态定位 按照标准流特性摆放位置，它没有边偏移。

​	静态定位在布局时我们几乎不用的 

#### 2、相对定位(relative)

**相对定位**是元素在移动位置的时候，是相对于它自己**原来的位置**来说的（自恋型）。

语法：position: relative; 

相对定位的特点：（务必记住）

​		1.它是相对于自己原来的位置来移动的（移动位置的时候参照点是自己原来的位置）。

​		2.**原来**在标准流的**位置**继续占有，后面的盒子仍然以标准流的方式对待它。

因此，**相对定位并没有脱标**。它最典型的应用是给绝对定位当爹的。

#### 3、绝对定位(absolute) 

**绝对定位**是元素在移动位置的时候，是相对于它**祖先元素**来说的（拼爹型）。

特点：

​		**完全脱标** —— 完全不占位置；  

​		**父元素没有定位**，则以**浏览器**为准定位（Document 文档）。

​		**父元素要有定位**元素将依据最近的已经定位（绝对、固定或相对定位）的父元素（祖先）进行定位。

#### 4、固定定位(fixed)

**固定定位**是元素**固定于浏览器可视区的位置**。（认死理型）   主要使用场景： 可以在浏览器页面滚动时元素的位置不会改变。

特点：

- **完全脱标**—— 完全不占位置；
- 只认**浏览器的可视窗口** —— `浏览器可视窗口 + 边偏移属性` 来设置元素的位置；
  - 跟父元素没有任何关系；单独使用的
  - 不随滚动条滚动。

------

### CSS属性书写顺序

建议遵循以下顺序：

1. **布局定位属性**：display / position / float / clear / visibility / overflow（建议 display 第一个写，毕竟关系到模式）
2. **自身属性**：width / height / margin / padding / border / background
3. **文本属性**：color / font / text-decoration / text-align / vertical-align / white- space / break-word
4. **其他属性（CSS3）**：content / cursor / border-radius / box-shadow / text-shadow / background:linear-gradient …

------

# 移动Web开发

------

### 视口

分类：

 	1、布局视口 layout viewport；

​	 2、视觉视口 visual viewport；

​	 3、理想视口 ideal viewport。

**总结：我们开发最终会用理想视口，而理想视口就是将布局视口的宽度修改为视觉视口**

#### meta标签

```
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">

//width=device-width ----  视口的宽度是设备屏幕的宽度
//initial-scale：初始比例，页面加载时的默认比例1.0
//user-scalable：指定用户是否可以对页面进行缩放 yes或者1允许/no或者0不允许
//minimum-scale：最小允许缩放的比率1.0
//maximum-scale：最大允许缩放的比率1.0
```

#### 查看技术是否兼容浏览器版本：https://caniuse.com/

------

### 移动开发选择和技术解决方案

#### 移动端技术解决方案

1.移动端浏览器兼容问题

移动端浏览器基本以 webkit 内核为主，因此我们就考虑webkit兼容性问题。

我们可以放心使用 H5 标签和 CSS3 样式。

同时我们浏览器的私有前缀我们只需要考虑添加 webkit 即可

2.移动端公共样式

移动端 CSS 初始化推荐使用 normalize.css/

Normalize.css：保护了有价值的默认值

Normalize.css：修复了浏览器的bug

Normalize.css：是模块化的

Normalize.css：拥有详细的文档

官网地址： <http://necolas.github.io/normalize.css/>

------

### 移动端特殊样式

```
 	/*CSS3盒子模型*/
    box-sizing: border-box;
    -webkit-box-sizing: border-box;
    /*点击高亮我们需要清除清除  设置为transparent 完成透明*/
    -webkit-tap-highlight-color: transparent;
    /*在移动端浏览器默认的外观在iOS上加上这个属性才能给按钮和输入框自定义样式*/
    -webkit-appearance: none;
    /*禁用长按页面时的弹出菜单*/
    img,a { -webkit-touch-callout: none; }
```

------

### flex布局

#### 父级盒子属性设置

| 描述                             | 属性            | 值                                                           |
| -------------------------------- | --------------- | ------------------------------------------------------------ |
| 设置Flex布局的主轴方向           | flex-direction  | **column**：将主轴改为y轴；**row**：将主轴改为x轴；row- reverse：主轴为x轴，并且翻转，从右到左翻转排列；column- reverse：主轴为y轴，并且翻转，从下到上翻转排列 ； |
| 设置主轴子元素排列形式           | justify-content | flex-start；flex-end；**center**；**space-around**所有子元素平分剩余空间；**space-between**所有子元素中，先两边两个元素贴边，剩余的元素平分剩余空间（常用）;**space-evenly**所有子元素之间的距离都一致 |
| 子元素是否换行                   | flex-wrap       | nowrap；wrap                                                 |
| 设置侧轴子元素对齐的方式（多行） | align-content   | **flex-start**；flex-end；**center**；**space-around**所有子元素平分剩余空间；**space-between**所有子元素中，先两边两个元素贴边，剩余的元素平分剩余空间（常用）;**stretch**默认值（拉升），如果项目未设置高度或设为auto，将占满整个容器的高度； |
| 设置侧轴子元素对齐的方式（单行） | align-items     | **flex-start**；flex-end；**center**；**stretch**默认值（拉升），如果项目未设置高度或设为auto，将占满整个容器的高度； baseline项目（子元素）的第一行文字的基线对齐； ; |

#### 子级盒子属性设置

| 描述                                                         | 属性       | 值                                            |
| ------------------------------------------------------------ | ---------- | --------------------------------------------- |
| 将容器（父级盒子）剩余空间按照占比分配给各个子盒子           | flex       | 实际的数字1；百分比                           |
| 项目（子级盒子）的排列顺序。                                 | order      | 实际的一个数值，数值越小，排列越靠前，默认为0 |
| 单个项目有与其他项目不一样的对齐方式设置，可覆盖align-items属性； | align-self | **flex-start**；flex-end；center； stretch    |

------

### rem布局

**安装px to rem 插件和Easy Less插件**

**rem值	=	px值	/	html文字大小**

**屏幕尺寸	/	划分份数	=	html文字大小**

**不同的视口, HTML标签字号不同, 字号是视口宽度的1/10**

rem的基准是相对于html元素的字体大小。

```
/* 根html 为 12px */
html {
   font-size: 12px;
}
/* 此时 div 的字体大小就是 24px */       
div {
    font-size: 2rem;
}
```

#### 媒体查询

##### 语法：

```
最好的写法：
@media (media feature媒体特性) {}

@media mediatype类型 and|not|only关键字 (media feature媒体特性) {}
```

1、mediatype 查询类型

![image-20211007102255759](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102255759.png)

2、关键字

​	and：可以将多个媒体特性连接到一起，相当于“且”的意思。

​	not：排除某个媒体类型，相当于“非”的意思，可以省略。

​	only：指定某个特定的媒体类型，可以省略。   

3、 媒体特性

![image-20211007102306663](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102306663.png)

##### 媒体查询link写法

```
 <link rel="stylesheet" href="./one.css" media="(min-width: 992px)">
```



##### 媒体查询书写规则

注意： 为了防止混乱，媒体查询我们要按照从小到大或者从大到小的顺序来写,但是我们最喜欢的还是从小到大来写，这样代码更简洁。

![image-20211007102322171](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102322171.png)

#### rem适配方案

技术方案：

​	1.less+rem+媒体查询

​	2.lflexible.js+rem

#### less

Less中文网址：[http://](http://lesscss.cn/)[less](http://lesscss.cn/)[css.cn/](http://lesscss.cn/)

##### Less安装

​	①安装nodejs，可选择版本(8.0)，网址：<http://nodejs.cn/download/>

​	②检查是否安装成功，使用cmd命令（win10是window+r 打开运行输入cmd）  ---输入“node –v”查看版本即可

​	③基于nodejs在线安装Less，使用cmd命令“npm install -g less”即可

​	④检查是否安装成功，使用cmd命令“ lessc -v ”查看版本即可。

##### 用法：

###### 	1、变量

```
@color: pink;

使用：
div {
	@color
}
```

###### 	2、 嵌套

```
// 将css改为less
#header .logo {
  width: 300px;
}

#header {
    .logo {
       width: 300px;
    }
}
```

**如果遇见 （交集|伪类|伪元素选择器） ，利用&进行连接**	

```
a:hover{
    color:red;
}
a{
  &:hover{
      color:red;
  }
}
```

###### 3、运算

```
/*Less 里面写*/
@witdh: 10px + 5;
div {
    border: @witdh solid red;
}
/*生成的css*/
div {
  border: 15px solid red;
}
/*Less 甚至还可以这样 */
width: (@width + 5) * 2;
```

+ 乘号（*）和除号（/）的写法  
+ 除号（/）需要加小括号
+ 运算符中间左右有个空格隔开 1px + 5
+ 对于两个不同的单位的值之间的运算，运算结果的值取第一个值的单位 
+ 如果两个值之间只有一个值有单位，则运算结果就取该单位

##### 样式导入

```
@import "./common.less";
可以简写为：
@import "./common";
```

**导入语句要书写在导入文件的的最前面；**

##### 导出路径设置

实际开发中我们需要将less文件和css文件分开保存，所以我们需要设置less翻译成css的存储位置

###### 导出的路径是统一

```
设置 → 搜索Easy Less → 在setting.json中编辑 → 在less.compile中添加代码----"out":"您的路径"
```

![image-20211007102400611](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102400611.png)

###### 单独路径导出

语法： // out：您要导出的路径 

![image-20211007102411221](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102411221.png)

注意：

​	1、书写单独输出路径的时候最后面不需要加封号；

​	2、必须写在less文件的第一行；

###### 禁止导出

语法：// out:false

注意：禁止导出语句一定要写在文件的第一行，后面一定不能写封号

![image-20211007102420023](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102420023.png)

#### **flexible.js适配**

##### 地址:

github地址：https://github.com/amfe/lib-flexible

官方文档地址：https://github.com/amfe/article/issues/17

##### 工作原理：

flexible.js时间设备的视口平均划分为10份，然后再去按照不同的视口大小计算出各自的html根标签的文字大小。

##### 使用方法：

第一步：将flexible.js拷贝到自己的项目中。

第二步：将flexible.js利用script标签引入到自己html页面的最后面。

------

### vw/vh布局

根据视口的宽高进行相对大小计算结果

**vh = px / (1/100*视口高度)**

**vw = px / (1/100*视口宽度)**

> ***不允许vw vh 混合使用***

变量

```
@vw: 3.75vw;

使用：
div {
	height: (18 / @vw)
}
```

------

# Bootstrap

#### 概念：

在不同屏幕下，通过媒体查询来改变这个布局容器的大小，再改变里面子元素的排列方式和大小，从而实现不同屏幕下，看到不同的页面布局和样式变化。

#### 常见屏幕尺寸下布局容器大小设置

超小屏幕（手机、小于768px）：设置宽度为100%；

小屏幕（平板，大于等于768px）：设置宽度为750px；

中等屏幕（桌面显示器，大于等于992px）：设置宽度为970px；

大屏幕（大桌面显示器，大于等于1200px）：设置宽度为1170px；

#### 中文网站：

http://www.bootcss.com/

#### 使用

01、将下载的生产环境文件夹直接复制到自己的项目中，并且引入css文件

02、布局容器 --- container 类

03、栅格系统

#### bootstrap布局容器

Bootstrap 需要为页面内容和栅格系统包裹一个 .container 或者.container-fluid 容器，它提供了两个作此用处的类。

.container

+ 响应式布局的容器  固定宽度
+ 大屏 ( >=1200px)  宽度定为 1170px
+ 中屏 ( >=992px)   宽度定为  970px
+ 小屏 ( >=768px)   宽度定为  750px
+ 超小屏  (100%) 

.container-fluid

+ 流式布局容器 百分百宽度
+ 占据全部视口（viewport）的容器。

#### bootstrap栅格系统

+ 按照不同屏幕划分为1~12 等份
+ 行（row） 可以去除父容器作用15px的边距
+ xs-extra small：超小； sm-small：小；  md-medium：中等； lg-large：大；
+ 列（column）大于 12，多余的“列（column）”所在的元素将被作为一个整体另起一行排列
+ 每一列默认有左右15像素的 padding
+ 可以同时为一列指定多个设备的类名，以便划分不同份数  例如 class="col-md-4 col-sm-6"

#### 列偏移

使用 .col-md-offset-* 类可以将列向右侧偏移。这些类实际是通过使用 * 选择器为当前元素增加了左侧的边距（margin）。

col-md-offset- 数字 =  12 - 已有的盒子份数；

盒子居中：（12 - 已有的份数） /  2

```
<!-- 列偏移 -->
  <div class="row">
      <div class="col-lg-4">1</div>
      <div class="col-lg-4 col-lg-offset-4">2</div>
  </div>
```

#### 列排序

通过使用 .col-md-push-* 和 .col-md-pull-* 类就可以很容易的改变列（column）的顺序。

push : 推；

pull : 拉；

```
<!-- 列排序 -->
  <div class="row">
      <div class="col-lg-4 col-lg-push-8">左侧</div>
      <div class="col-lg-8 col-lg-pull-4">右侧</div>
  </div>
```

#### 响应式工具

![image-20211007102437694](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102437694.png)

------

# JavaScript

## 基础

### 书写格式

1、行内式

```
<input type="button" value="点我试试" onclick="alert('Hello World')" />
```

2、内嵌式

```
<script>
    alert('Hello  World~!');
</script>
```

3、外部JS文件

```
<script src="my.js"></script>
```

### JavaScript输入输出语句

| 方法               | 说明                           | 归属   |
| ------------------ | ------------------------------ | ------ |
| alert("msg")       | 浏览器弹出警示框               | 浏览器 |
| console.log("msg") | 浏览器控制台打印输出信息       | 浏览器 |
| prompt("info")     | 浏览器弹出输入框，用户可以输入 | 浏览器 |

### 变量

#### 使用

1、变量的声明   

```
//  声明变量  
var age; //  声明一个 名称为age 的变量   
```

2、变量的赋值 

```
age = 10; // 给 age  这个变量赋值为 10   
```

#### 变量的初始化

```
var age  = 18;  // 声明变量同时赋值为 18
// 声明一个变量并赋值， 我们称之为变量的初始化。
```

#### 变量语法扩展

- 更新变量

  ​		一个变量被重新复赋值后，它原有的值就会被覆盖，变量值将以最后一次赋的值为准。

  ```js
  var age = 18;
  
  age = 81;   // 最后的结果就是81因为18 被覆盖掉了          
  ```

- 同时声明多个变量

  ​		同时声明多个变量时，只需要写一个 var， 多个变量名之间使用英文逗号隔开。

  ```js
  var age = 10,  name = 'zs', sex = 2;       
  ```

- 声明变量特殊情况

  | 情况                           | 说明                    | 结果      |
  | ------------------------------ | ----------------------- | --------- |
  | var  age ; console.log (age);  | 只声明 不赋值           | undefined |
  | console.log(age)               | 不声明 不赋值  直接使用 | 报错      |
  | age   = 10; console.log (age); | 不声明   只赋值         | 10        |

#### 变量命名规范

规则：

- 由字母(A-Za-z)、数字(0-9)、下划线(_)、美元符号( $ )组成，如：usrAge, num01, _name
- 严格区分大小写。var app; 和 var App; 是两个变量
- 不能 以数字开头。  18age   是错误的
- 不能 是关键字、保留字。例如：var、for、while
- 变量名必须有意义。 MMD   BBD        nl   →     age  
- 遵守驼峰命名法。首字母小写，后面单词的首字母需要大写。myFirstName![](D:\Program Files\Front End\自学\黑马前端最新就业班-0基础小白到就业\03-阶段三：JavaScript 网页编程资料\01-JavaScript基础语法资料\JavaScript基础第01天（1-3小节）\4-笔记\images\图片15.png)

推荐翻译网站： 有道    爱词霸

### 数据类型

分类：1、简单数据类型 （Number,String,Boolean,Undefined,Null）

​			2、复杂数据类型 （object)	

#### 简单数据类型

![image-20211006211544083](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211544083.png)

##### 1、数字型 Number

JavaScript中数值的最大和最小值

- ​	最大值：Number.MAX_VALUE，这个值为： 1.7976931348623157e+308

- ​	最小值：Number.MIN_VALUE，这个值为：5e-32

数字型三个特殊值

- Infinity ，代表无穷大，大于任何数值

- -Infinity ，代表无穷小，小于任何数值

- NaN ，Not a number，代表一个非数值

isNaN（）：

-  用来判断一个变量是否为非数字的类型，返回 true 或者 false

##### 2、字符串型 String

字符串型可以是引号中的任意文本，其语法为 双引号 "" 和 单引号''

###### 字符串转义符

| 转义符 | 解释说明                          |
| ------ | --------------------------------- |
| \n     | 换行符，n   是   newline   的意思 |
| \ \    | 斜杠   \                          |
| \'     | '   单引号                        |
| \"     | ”双引号                           |
| \t     | tab  缩进                         |
| \b     | 空格 ，b   是   blank  的意思     |

###### 检测字符串长度

 String.length

###### 字符串拼接

```
//1.1 字符串 "相加"
alert('hello' + ' ' + 'world'); // hello world
//1.2 数值字符串 "相加"
alert('100' + '100'); // 100100
//1.3 数值字符串 + 数值
alert('11' + 12);     // 1112 
```

- 经常会将字符串和变量来拼接，变量可以很方便地修改里面的值
- 变量是不能添加引号的，因为加引号的变量会变成字符串
- 如果变量两侧都有字符串拼接，口诀“引引加加 ”，删掉数字，变量写加中间

###### 字符串补全

padStart（目标长度，'填充的字符串'）

```
console.log("h".padStart(5,"o"));  // "ooooh"
```

##### 3、布尔型Boolean

​	布尔类型有两个值：true 和 false ，其中 true 表示真（对），而 false 表示假（错）。

​	布尔型和数字型相加的时候， true 的值为 1 ，false 的值为 0。

##### 4、未定义Undefined

##### 5、空值Null

#### 获取变量数据类型

typeof 可用来获取检测变量的数据类型

```
var num = 18;
console.log(typeof num) // 结果 number    
```

![image-20211006211609174](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211609174.png)

#### 数据类型转换

##### 1、转换为字符串

![image-20211006211621182](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211621182.png)

- 变量.toString() 和 String(变量)  使用方式不一样。
- 三种转换方式，更多第三种加号拼接字符串转换方式， 这一种方式也称之为隐式转换。

##### 2、转换为数字型

![image-20211006211630171](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211630171.png)

- 注意 parseInt 和 parseFloat 单词的大小写，这2个是重点
- 隐式转换是我们在进行算数运算的时候，JS 自动转换了数据类型

#####  3、转换为布尔型

![image-20211006211638473](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211638473.png)

- 代表空、否定的值会被转换为 false  ，如 ''、0、NaN、null、undefined  

- 其余值都会被转换为 true

### 运算符

#### 运算符优先级

![image-20211006211713772](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211713772.png)

#### 1、算数运算符

![image-20211006211725341](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211725341.png)

#### 2、递增和递减运算符

前置递增运算符

```
++num 前置递增，就是自加1，类似于 num =  num + 1，但是 ++num 写起来更简单。

使用口诀：先自加，后返回值
```

后置递增运算符

```
num++ 后置递增，就是自加1，类似于 num =  num + 1 ，但是 num++ 写起来更简单。

使用口诀：先返回原值，后自加 
```

#### 3、比较运算符

![image-20211006211736828](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211736828.png)

#### 4、逻辑运算符

![image-20211006211745058](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211745058.png)

逻辑与&&：两边都是 true才返回 true，否则返回 false；

逻辑或 ||：一边是 true则返回 true，否则返回 false；

逻辑非 ！：逻辑非（!）也叫作取反符，用来取一个布尔值相反的值，如 true 的相反值是 false；



短路运算（逻辑中断）：	

```
逻辑与：		

- 如果第一个表达式的值为真，则返回表达式2

- 如果第一个表达式的值为假，则返回表达式1
```

```
逻辑或

- 如果第一个表达式的值为真，则返回表达式1

- 如果第一个表达式的值为假，则返回表达式2
```

#### 5、赋值运算符

![image-20211006211802478](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211802478.png)

```
var age = 10;
age += 5;  // 相当于 age = age + 5;
age -= 5;  // 相当于 age = age - 5;
age *= 10; // 相当于 age = age * 10;
```

### 流程控制

#### 分支流程控制

##### 1、if 语句

```
// 条件成立执行代码，否则什么也不做
if (条件表达式) {
    // 条件成立执行的代码语句
}


// 条件成立  执行 if 里面代码，否则执行else 里面的代码
if (条件表达式) {
    // [如果] 条件成立执行的代码
} else {
    // [否则] 执行的代码
}


// 适合于检查多重条件。
if (条件表达式1) {
    语句1；
} else if (条件表达式2)  {
    语句2；
} else if (条件表达式3)  {
   语句3；
 ....
} else {
    // 上述条件都不成立执行此处代码
}
```

##### 2、三元表达式

- 语法结构

  ```js
  表达式1 ? 表达式2 : 表达式3;
  ```

- 执行思路

  - 如果表达式1为 true ，则返回表达式2的值，如果表达式1为 false，则返回表达式3的值
  - 简单理解： 就类似于  if  else （双分支） 的简写

##### 3、switch 语句

- 语法结构

```
switch( 表达式 ){ 
    case value1:
        // 表达式 等于 value1 时要执行的代码
        break;
    case value2:
        // 表达式 等于 value2 时要执行的代码
        break;
    default:
        // 表达式 不等于任何一个 value 时要执行的代码
}
```

**注意：** 

​	1、执行case 里面的语句时，如果没有break，则继续执行下一个case里面的语句。

​	2、表达式为固定值，变量时，必须时全等。

#### 循环

##### 1、for循环

- 语法结构

```
for(初始化变量; 条件表达式; 操作表达式 ){
    //循环体
}
```

| 名称       | 作用                                                         |
| ---------- | ------------------------------------------------------------ |
| 初始化变量 | 通常被用于初始化一个计数器，该表达式可以使用 var 关键字声明新的变量，这个变量帮我们来记录次数。 |
| 条件表达式 | 用于确定每一次循环是否能被执行。如果结果是 true 就继续循环，否则退出循环。 |
| 操作表达式 | 用于确定每一次循环是否能被执行。如果结果是 true 就继续循环，否则退出循环。 |

- for 循环小结

  ​		for 循环可以重复执行某些相同代码

  ​		for 循环可以重复执行些许不同的代码，因为我们有计数器

  ​		for 循环可以重复执行某些操作，比如算术运算符加法操作

  ​		随着需求增加，双重for循环可以做更多、更好看的效果

  ​		双重 for 循环，外层循环一次，内层 for 循环全部执行

  ​		for 循环是循环条件和数字直接相关的循环

##### 2、while循环

- 语法结构

```
while (条件表达式) {
    // 循环体代码 
}
```

**注意：**

​		使用 while 循环时一定要注意，它必须要有退出条件，否则会成为死循环

##### 3、do-while循环

- 语法结构

```
do {
    // 循环体代码 - 条件表达式为 true 时重复执行循环体代码
} while(条件表达式);
```

**注意：**

​		先再执行循环体，再判断，do…while循环语句至少会执行一次循环体代码

##### 4、for...in 语句

用于对数组或者对象的属性进行循环操作。

```
for (var k in obj) {
    console.log(k);      // 这里的 k 是属性名
    console.log(obj[k]); // 这里的 obj[k] 是属性值
}
```



##### 5、关键字

continue：continue 关键字用于立即跳出本次循环，继续下一次循环（本次循环体中 continue 之后的代码就会少执行一次）。

break：直接退出整个for 循环，跳到整个for下面的语句。

return ：不仅可以退出循环，还能够返回 return 语句中的值，同时还可以结束当前的函数体内的代码

### 函数

函数：就是**封装了一段可被重复调用执行的代码块**。通过此代码块可以**实现大量代码的重复使用**。  

#### 函数的使用

##### 1、函数声明（命名函数）

```
// 声明函数
function 函数名(形参...) {
    //函数体代码
}

//调用
函数名(实参);
```

##### 2、函数表达式（匿名函数）

```
// 声明函数
var 变量名 = function(形参...) {
    //函数体代码
}

//调用
变量名(实参);
```

##### 3、函数形参和实参

![image-20210820152258757](C:\Users\LEO\AppData\Roaming\Typora\typora-user-images\image-20210820152258757.png)

小结：

-  函数可以带参数也可以不带参数
-  声明函数的时候，函数名括号里面的是形参，形参的默认值为 undefined
-  调用函数的时候，函数名括号里面的是实参
-  多个参数中间用逗号分隔
-  形参的个数可以和实参个数不匹配，但是结果不可预计，我们尽量要匹配

#### 函数返回值

返回值：函数调用整体代表的数据；函数执行完成后可以通过return语句将指定数据返回 。

```
// 声明函数
function 函数名（）{
    ...
    return  需要返回的值；
}
// 调用函数
函数名();    // 此时调用函数就可以得到函数体内return 后面的值
```

-  在使用 return 语句时，函数会停止执行，并返回指定的值
-  如果函数没有 return ，返回的值是 undefined

#### arguments的使用

arguments 对象中存储了传递的所有实参。

具有以下特点：

- 具有 length 属性

- 按索引方式储存数据

- 不具有数组的 push , pop 等方法

  注意：在函数内部使用该对象，用此对象获取函数调用时传的实参。

#### 立即执行函数

含义： 不需要调用，立马执行的函数。

1、 （ function () {} ）（）   //常用，多个时要用“；”隔开。

2、 （ function () {} （））

*立即执行函数最大的作用就是 独立创建了一个作用域, 里面所有的变量都是局部变量 不会有命名冲突的情况*

### 对象

#### 创建对象

##### 1、使用对象字面量创建

```
//创建对象
var 对象名 = {};     // 键值对的形式，多个属性用“ ，”隔开

var star = {
    name : 'pink',
    age : 18,
    sex : '男',
    sayHi : function(){			//sayHi属于对象的方法
        alert('大家好啊~');
    }
};


//调用
对象里面的属性调用:对象.属性名；  
					或者   
				对象[‘属性名’]//也可以判断对象中是否有这个属性；
对象里面的方法调用:	对象.方法名()；
```

##### 2、利用 new Object 创建

```
var andy = new Object();
andy.属性名 = 'pink';
andy.属性名 = 18;
andy.属性名 = '男';
andy.方法名 = function(){
    alert('大家好啊~');
}
```

##### 3、利用构造函数创建

构造函数：把对象中一些公共的属性和方法抽取出来，然后封装到这个函数里面。

```
//创建
function 构造函数名(形参1,形参2,形参3) {
     this.属性名1 = 参数1;
     this.属性名2 = 参数2;
     this.属性名3 = 参数3;
     this.方法名 = 函数体;
}

//调用
var obj = new 构造函数名(实参1，实参2，实参3)
```

**注意事项**：

1.   构造函数约定**首字母大写**。
2.   函数内的属性和方法前面需要添加 **this** ，表示当前对象的属性和方法。
3.   构造函数中**不需要 return 返回结果**。
4.   当我们创建对象的时候，**必须用 new 来调用构造函数**。

#### 遍历对象

for...in 语句

用于对数组或者对象的属性进行循环操作。

```
for (var k in obj) {
    console.log(k);      // 这里的 k 是属性名
    console.log(obj[k]); // 这里的 obj[k] 是属性值
}
```

#### 内置对象

 JavaScript 中的对象分为3种：**自定义对象 、内置对象、 浏览器对象**

MDN:https://developer.mozilla.org/zh-CN/

##### 1、Math对象

Math 对象不是构造函数。

| 属性、方法名          | 功能                                         |
| --------------------- | -------------------------------------------- |
| Math.PI               | 圆周率                                       |
| Math.floor()          | 向下取整                                     |
| Math.ceil()           | 向上取整                                     |
| Math.round()          | 四舍五入版 就近取整   注意 -3.5   结果是  -3 |
| Math.abs()            | 绝对值                                       |
| Math.max()/Math.min() | 求最大和最小值                               |
| Math.random()         | 获取范围在[0,1)内的随机值                    |

**获取指定范围内的随机整数**：

```
function getRandom(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min; 
}
```

##### 2、Date对象（日期）

Date是一个构造函数。

###### 使用Date实例化日期对象：

```
获取当前时间必须实例化
var now = new Date();

获取指定时间的日期对象
var future = new Date('2019-10-1');
//参数常用的写法  数字型  2019, 10, 01  或者是 字符串型 '2019-10-1 8:8:8'

注意：如果创建实例时并未传入参数，则得到的日期对象是当前时间对应的日期对象
```

###### Date实例的方法和属性

| 代码                | 说明                                     |
| ------------------- | ---------------------------------------- |
| date.getFullYear(); | 返回当前年                               |
| date.getMonth() +1; | 返回当前月，要+1                         |
| date.getDate();     | 返回当前几号                             |
| date.getDay();      | 返回当前周几，周一为1，周六为6， 周日为0 |
| date.getHours();    | 返回当前小时                             |
| date.getMinutes();  | 返回当前分钟                             |
| date.getSeconds();  | 返回当前秒钟                             |

###### 获取总毫秒数

总毫秒数的含义：基于1970年1月1日（世界标准时间）起的毫秒数。

```
// 实例化Date对象
var date = new Date();
// 1. 用于获取对象的原始值
console.log(date.valueOf())	
console.log(date.getTime())	

// 2. 简单写可以这么做                   // 常用
var date = +new Date();	

// 3. HTML5中提供的方法，有兼容性问题
var date = Date.now();
```

###### 毫秒数转为天、时、时、秒

毫秒数 / 1000 = 秒数

天：parseInt（秒数 / 60 / 60 / 24）;

时：parseInt（秒数 / 60 / 60 % 24）;

时：parseInt（秒数 / 60 % 60）;

秒：parseInt（秒数 %60）;

##### 3、数组对象

###### 创建数组

1、利用  new 创建数组  

```
var 数组名 = new Array() ；
var arr = new Array();   // 创建一个新的空数组
```

2、利用数组字面量创建数组

```
//1. 使用数组字面量方式创建空的数组
var  数组名 = []；
//2. 使用数组字面量方式创建带初始值的数组
var  数组名 = ['小白','小黑','大黄','瑞奇'];
```

###### 获取数组中的元素

数组可以通过索引来访问、设置、修改对应的数组元素，可以通过“数组名[索引]”的形式来获取数组中的元素。

![image-20211006211925140](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211925140.png)

```
// 定义数组
var arrStus = [1,2,3];
// 获取数组中的第2个元素
alert(arrStus[1]);   
```

**注意：**

​		如果访问时数组没有和索引值对应的元素，则得到的值是undefined。

###### 遍历数组

```
var arr = ['red','green', 'blue'];
for(var i = 0; i < arr.length; i++){
    console.log(arrStus[i]);
}
```

###### 数组的长度

```
var arrStus = [1,2,3];
alert(arrStus.length);  // 3
```

###### 新增数组元素

​		数组中可以通过以下方式在数组的末尾插入新元素

```
数组[ 数组.length ] = 新数据;
```

###### 检测是否为数组

```
1、数组名 instanceof Array；
2、Array.isArray(数组名)；     // 常用
```

###### 添加删除数组元素的方法

![image-20211006212056706](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006212056706.png)

![image-20211008165353295](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211008165353295.png)

```
var arr1 = [1, 2, 3],
            arr2 = [4, 5, 6];
        console.log(arr1.concat(arr2));

        var arr3 = [1, 2, 3, 4, 5, 6];
        //不包括end;当只有一个数字时，从start到结尾全部
        console.log(arr3.slice(2, 5));

        var arr4 = [1, 2, 3, 4, 5, 6];
        //删除（索引号，删除个数）
        //添加 （索引号，0，添加的值）
        //替换 （索引号， 替换几个，替换的值）
        arr4.splice(2, 1);
        console.log(arr4);
```

###### 数组排序

![image-20211006212117354](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006212117354.png)

注意：sort方法需要传入参数来设置升序、降序排序

- 如果传入“function(a,b){ return a-b;}”，则为升序
- 如果传入“function(a,b){ return b-a;}”，则为降序

###### 获取数组索引方法

```
1、数组名.indexOf(数组元素)  //从前往后找
2、数组名.lastIndexOf(数组元素)  //从后往前找
```

**注意：**

​		只返回第一个满足的元素的索引号；找不到则返回“-1”；

###### 数组转换为字符串

![image-20211006212130313](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006212130313.png)

**注意：**

​		join方法如果不传入参数，则按照 “ , ”拼接元素。常用//

##### 4、字符串对象

基本数据类型包装为复杂数据类型，其执行过程如下（浏览器自动执行） ：

```
// 1. 生成临时变量，把简单类型包装为复杂数据类型
var temp = new String('andy');
// 2. 赋值给我们声明的字符变量
str = temp;
// 3. 销毁临时变量
temp = null;
```

###### 根据字符返回位置

```
1、变量名.indexOf(‘查的字符串’，[起始位置])  //从前往后找
2、变量名.lastIndexOf(‘查的字符串’，[起始位置])  //从后往前找
```

**注意：**

​		只返回第一个满足的元素的索引号；找不到则返回“-1”；

###### 根据位置返回字符

![image-20211006212144883](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006212144883.png)

**注意：**

​		常用第三种；

###### 字符串操作方法

![image-20211006212159339](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006212159339.png)

**注意：**

​		常用第二种；

```
//替换字符   注意：只会替换第一个字符串
字符串.replace("被替换的字符串"， "要替换为的字符串")；

//转为数组
字符串.split("分割字符")

//去除左右两边空白+
字符串.trim()

//补零
padStart(补零后几位数,'0')

例如：var str ='8'
str.padStart(2,'0')
输出：08
```

## 高级

### 面向对象

面向对象是把事务分解成为一个个对象，然后由对象之间分工与合作。

|      | 面向过程                                                     | 面向对象                                                     |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 优点 | 性能比面向对象高，适合跟硬件联系很紧密的东西，例如单片机就采用的面向过程编程。 | 易维护、易复用、易扩展，由于面向对象有封装、继承、多态性的特性，可以设计出低耦合的系统，使系统 更加灵活、更加易于维护 |
| 缺点 | 不易维护、不易复用、不易扩展                                 | 性能比面向过程低                                             |

### ES6中的对象与类

#### 创建类

```
 // 1. 创建类 class  创建一个 明星类
 class 类名 {
   // 类的共有属性放到 constructor 里面
   constructor(name, age) {
   		this.name = name;
   		this.age = age;
   }
 }
   // 2. 利用类创建对象 new
   var 变量 = new 类名('刘德华', 18);
```

#### 类创建添加属性和方法

```
 // 1. 创建类 class  创建一个类
class Star {
    // 类的共有属性放到 constructor 里面 constructor是 构造器或者构造函数
    constructor(uname, age) {
      this.uname = uname;
      this.age = age;
    }//------------------------------------------->注意,方法与方法之间不需要添加逗号
    sing(song) {
      console.log(this.uname + '唱' + song);
    }
}
// 2. 利用类创建对象 new
var ldh = new Star('刘德华', 18);
console.log(ldh); // Star {uname: "刘德华", age: 18}
ldh.sing('冰雨'); // 刘德华唱冰雨
```



注意哟:**

1. 通过class 关键字创建类, 类名我们还是习惯性定义首字母大写
2. 类里面有个constructor 函数,可以接受传递过来的参数,同时返回实例对象
3. constructor 函数 只要 new 生成实例时,就会自动调用这个函数, 如果我们不写这个函数,类也会自动生成这个函数
4. 多个函数方法之间不需要添加逗号分隔
5. 生成实例 new 不能省略
6. 语法规范, 创建类 类名后面不要加小括号,生成实例 类名后面加小括号, 构造函数不需要加function

### 类的继承

```
// 父类
class Father{   
} 

// 子类继承父类
class  Son  extends Father {  
}  
```

子类使用super关键字访问父类的方法

​			**super 必须在子类this之前调用**

```
//定义了父类
class Father {
   constructor(x, y) {
   this.x = x;
   this.y = y;
   }
   sum() {
   		console.log(this.x + this.y);
	}
 }
//子元素继承父类
    class Son extends Father {
   		 constructor(x, y) {
    		super(x, y); //使用super调用了父类中的构造函数
    	}
    }
    var son = new Son(1, 2);
    son.sum(); //结果为3
```

时刻注意this的指向问题,类里面的共有的属性和方法一定要加this使用.

1. constructor中的this指向的是new出来的实例对象 
2. 自定义的方法,一般也指向的new出来的实例对象
3. 绑定事件之后this指向的就是触发事件的事件源

在 ES6 中类没有变量提升，所以必须先定义类，才能通过类实例化对象

### 构造函数和原型

#### 定义：

1、实例成员就是构造函数内部通过this添加的成员；

```
uname age sing 就是实例成员,实例成员只能通过实例化的对象来访问

 function Star(uname, age) {
     this.uname = uname;
     this.age = age;
     this.sing = function() {
     console.log('我会唱歌');
    }
}
var ldh = new Star('刘德华', 18);
console.log(ldh.uname);//实例成员只能通过实例化的对象来访问
```

2、静态成员 在构造函数本身上添加的成员

```
如下列代码中 sex 就是静态成员,静态成员只能通过构造函数来访问

 function Star(uname, age) {
     this.uname = uname;
     this.age = age;
     this.sing = function() {
     console.log('我会唱歌');
    }
}
Star.sex = '男';
var ldh = new Star('刘德华', 18);
console.log(Star.sex);//静态成员只能通过构造函数来访问
```

#### 构造函数原型（原型对象）prototype

JavaScript 规定，每一个构造函数都有一个prototype 属性，指向另一个对象。注意这个prototype就是一个对象，这个对象的所有属性和方法，都会被构造函数所拥有。

我们可以把那些不变的方法，直接**定义在 prototype 对象上**，这样所有对象的实例就可以**共享这些方法。**

```
function Star(uname, age) {
    this.uname = uname;
    this.age = age;
}
Star.prototype.sing = function() {
	console.log('我会唱歌');
}
var ldh = new Star('刘德华', 18);
var zxy = new Star('张学友', 19);
console.log(ldh.sing === zxy.sing)//true
ldh.sing();//我会唱歌
zxy.sing();//我会唱歌
```

#### 对象原型

```
对象都会有一个属性 __proto__ 指向构造函数的 prototype 原型对象。
__proto__对象原型和原型对象 prototype 是等价的
__proto__对象原型的意义就在于为对象的查找机制提供一个方向，或者说一条路线，但是它是一个非标准属性，因此实际开发中，不可以使用这个属性，它只是内部指向原型对象 prototype
```

![image-20211007102527456](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102527456.png)

#### 构造函数constructor

指回构造函数本身

```
对象原型（ __proto__）和构造函数（prototype）原型对象里面都有一个属性 constructor 属性 ，constructor 我们称为构造函数，因为它指回构造函数本身。
constructor 主要用于记录该对象引用于哪个构造函数，它可以让原型对象重新指向原来的构造函数。
一般情况下，对象的方法都在构造函数的原型对象中设置。如果有多个对象的方法，我们可以给原型对象采取对象形式赋值，但是这样就会覆盖构造函数原型对象原来的内容，这样修改后的原型对象 constructor  就不再指向当前构造函数了。此时，我们可以在修改后的原型对象中，添加一个 constructor 指向原来的构造函数。
```

如果我们修改了原来的原型对象,给原型对象赋值的是一个对象,则必须手动的利用constructor指回原来的构造函数如:

```
 function Star(uname, age) {
     this.uname = uname;
     this.age = age;
 }
 // 很多情况下,我们需要手动的利用constructor 这个属性指回 原来的构造函数
 Star.prototype = {
 // 如果我们修改了原来的原型对象,给原型对象赋值的是一个对象,则必须手动的利用constructor指回原来的构造函数
   constructor: Star, // 手动设置指回原来的构造函数
   sing: function() {
     console.log('我会唱歌');
   },
   movie: function() {
     console.log('我会演电影');
   }
}
var zxy = new Star('张学友', 19);
console.log(zxy)
```

#### 原型链

​	每一个实例对象又有一个__proto__属性，指向的构造函数的原型对象，构造函数的原型对象也是一个对象，也有__proto__属性，这样一层一层往上找就形成了原型链。

```
当访问一个对象的属性（包括方法）时，首先查找这个对象自身有没有该属性。
如果没有就查找它的原型（也就是 __proto__指向的 prototype 原型对象）。
如果还没有就查找原型对象的原型（Object的原型对象）。
依此类推一直找到 Object 为止（null）。
__proto__对象原型的意义就在于为对象成员查找机制提供一个方向，或者说一条路线。
```

![image-20211007102541740](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102541740.png)

#### 构造函数实例和原型对象三角关系

```
1.构造函数的prototype属性指向了构造函数原型对象
2.实例对象是由构造函数创建的,实例对象的__proto__属性指向了构造函数的原型对象
3.构造函数的原型对象的constructor属性指向了构造函数,实例对象的原型的constructor属性也指向了构造函数
```

![image-20211007102646069](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102646069.png)

#### 原型对象中this指向

```
function Star(uname, age) {
    this.uname = uname;
    this.age = age;
}
var that;
Star.prototype.sing = function() {
    console.log('我会唱歌');
    that = this;
}
var ldh = new Star('刘德华', 18);
// 1. 在构造函数中,里面this指向的是对象实例 ldh
console.log(that === ldh);//true
// 2.原型对象函数里面的this 指向的是 实例对象 ldh
```

#### 通过原型为数组扩展内置方法

```
Array.prototype.sum = function() {
   var sum = 0;
   for (var i = 0; i < this.length; i++) {
   sum += this[i];
   }
   return sum;
 };
 //此时数组对象中已经存在sum()方法了  可以始终 数组.sum()进行数据的求
```

### 继承

#### 1、call()

- 函数名.call（）---> 可以调用函数
- 函数名.call（thisAry，arg1.....）--->可以修改this的指向,使用call()的时候 参数一是修改后的this指向,参数2,参数3..使用逗号隔开连接
  - thisAry：修改当前this指向为这个
  - arg1：传递参数

```
 function fn(x, y) {
     console.log(this);
     console.log(x + y);
}
  var o = {
  	name: 'andy'
  };
  fn.call(o, 1, 2);//调用了函数此时的this指向了对象o,
```

![image-20211007102700361](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102700361.png)

#### 2、子构造函数继承父构造函数中的属性

1. 先定义一个父构造函数
2. 再定义一个子构造函数
3. 子构造函数继承父构造函数的属性(使用call方法)

```
 // 1. 父构造函数
 function Father(uname, age) {
   // this 指向父构造函数的对象实例
   this.uname = uname;
   this.age = age;
 }
  // 2 .子构造函数 
function Son(uname, age, score) {
  // this 指向子构造函数的对象实例
  3.使用call方式实现子继承父的属性
  Father.call(this, uname, age);
  this.score = score;
}
var son = new Son('刘德华', 18, 100);
console.log(son);
```

![image-20211007102710441](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102710441.png)

#### 3、借用原型对象继承方法

1. 先定义一个父构造函数
2. 再定义一个子构造函数
3. 子构造函数继承父构造函数的属性(使用call方法)

```
// 1. 父构造函数
function Father(uname, age) {
  // this 指向父构造函数的对象实例
  this.uname = uname;
  this.age = age;
}
Father.prototype.money = function() {
  console.log(100000);
 };
 // 2 .子构造函数 
  function Son(uname, age, score) {
      // this 指向子构造函数的对象实例
      Father.call(this, uname, age);
      this.score = score;
  }
-------------------------------------------------
// Son.prototype = Father.prototype;  这样直接赋值会有问题,如果修改了子原型对象,父原型对象也会跟着一起变化
-------------------------------------------------
  Son.prototype = new Father();
  // 如果利用对象的形式修改了原型对象,别忘了利用constructor 指回原来的构造函数
  Son.prototype.constructor = Son;
  // 这个是子构造函数专门的方法
  Son.prototype.exam = function() {
    console.log('孩子要考试');

  }
  var son = new Son('刘德华', 18, 100);
  console.log(son);
```

如上代码结果如图:

![image-20211007102724649](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102724649.png)

### ES5新增方法

#### 数组方法

##### 1、forEach遍历数组

主要用于遍历数组，没有返回值

```js
 数组.forEach(function(value, index, array) {
       //参数一是:数组元素
       //参数二是:数组元素的索引
       //参数三是:当前的数组
 })
  //相当于数组遍历的 for循环 没有返回值
```

##### 2、filter过滤数组

主要用于筛选数组，返回的是一个新数组；

满足条件的元素都返回来，需要申明一个变量来接收 

```js
  var arr = [12, 66, 4, 88, 3, 7];
  var newArr = arr.filter(function(value, index,array) {
  	 //参数一是:数组元素
     //参数二是:数组元素的索引
     //参数三是:当前的数组
     return value >= 20;
  });
  console.log(newArr);//[66,88] //返回值是一个新数组
```

##### 3、some

查找数组中是否有满足条件的元素 

返回值是布尔值,只要查找到满足条件的一个元素就立马终止循环

```
some 查找数组中是否有满足条件的元素 
 var arr = [10, 30, 4];
 var flag = arr.some(function(value,index,array) {
    //参数一是:数组元素
     //参数二是:数组元素的索引
     //参数三是:当前的数组
     return value < 3;
  });
console.log(flag);//false返回值是布尔值,只要查找到满足条件的一个元素就立马终止循环
```

##### 扩展：

```
return  true;
	1、在forEach中不会终止遍历
	2、在some中会终止遍历，效率更高
```

#### 字符串方法trim

返回的是新字符串，需要用一个变量接收

```
var str = '   hello   '
console.log(str.trim()）  //hello 去除两端空格
var str1 = '   he l l o   '
console.log(str.trim()）  //he l l o  去除两端空格
```

#### 对象方法

##### 1、获取对象的属性名

Object.keys(对象) //获取到当前对象中的属性名 ，返回值是一个**数组**

```
var obj = {
     id: 1,
     pname: '小米',
     price: 1999,
     num: 2000
};
var result = Object.keys(obj)
console.log(result)//[id，pname,price,num]
```

##### 2、设置或修改对象中的属性

**三个参数必须写**

```js
Object.defineProperty(对象，修改或新增的属性名，{
		value:修改或新增的属性的值,
		writable:true/false,//如果值为false 不允许修改这个属性值
		enumerable: false,//enumerable 如果值为false 则不允许遍历
        configurable: false  //configurable 如果为false 则不允许删除这个属性 属性是否可以被删除或是否可以再次修改特性
})	
```

### 函数的定义和调用

#### 1、定义

1. 方式1： 函数声明方式 function 关键字 (命名函数)

   ```js
   function fn(){}
   ```

2. 方式2： 函数表达式(匿名函数)

   ```js
   var fn = function(){}
   ```

3. 方式3 ：new Function() 

   ```js
   var f = new Function('a', 'b', 'console.log(a + b)');
   f(1, 2);
   
   var fn = new Function('参数1','参数2'..., '函数体')
   注意
   /*Function 里面参数都必须是字符串格式
   第三种方式执行效率低，也不方便书写，因此较少使用
   所有函数都是 Function 的实例(对象)  
   函数也属于对象
   */
   ```

#### 2、函数的调用

```js
/* 1. 普通函数 */
function fn() {
	console.log('人生的巅峰');
}
 fn(); 
/* 2. 对象的方法 */
var o = {
  sayHi: function() {
  	console.log('人生的巅峰');
  }
}
o.sayHi();
/* 3. 构造函数*/
function Star() {};
new Star();
/* 4. 绑定事件函数*/
 btn.onclick = function() {};   // 点击了按钮就可以调用这个函数
/* 5. 定时器函数*/
setInterval(function() {}, 1000);  这个函数是定时器自动1秒钟调用一次
/* 6. 立即执行函数(自调用函数)*/
(function() {
	console.log('人生的巅峰');
})();
```

### this指向

#### 1、函数内部的this指向

这些 this 的指向，是当我们调用函数的时候确定的。调用方式的不同决定了this 的指向不同，一般指向我们的调用者.

![image-20211007102943214](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102943214.png)

#### 2、改变函数内部 this 指向

##### 2.1、call方法

call()方法调用一个对象。简单理解为调用函数的方式，但是它可以改变函数的 this 指向；

应用场景:  经常做继承. 

```js
var o = {
	name: 'andy'
}
 function fn(a, b) {
      console.log(this);
      console.log(a+b)
};
fn(1,2)// 此时的this指向的是window 运行结果为3
fn.call(o,1,2)//此时的this指向的是对象o,参数使用逗号隔开,运行结果为3
```

以上代码运行结果为:

![image-20211007102956000](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007102956000.png)

##### 2.2、apply方法

apply() 方法调用一个函数。简单理解为调用函数的方式，但是它可以改变函数的 this 指向。

应用场景:  经常跟数组有关系

```js
var o = {
	name: 'andy'
}
 function fn(a, b) {
      console.log(this);
      console.log(a+b)
};
fn()// 此时的this指向的是window 运行结果为3
fn.apply(o,[1,2])//此时的this指向的是对象o,参数使用数组传递 运行结果为3
```

![image-20211007103006476](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103006476.png)

#### 2.3 、bind方法（常用）

bind() 方法不会调用函数,但是能改变函数内部this 指向,返回的是原函数改变this之后产生的新函数，需用一个变量来接收

如果只是想改变 this 指向，并且不想调用这个函数的时候，可以使用bind

应用场景:不调用函数,但是还想改变this指向

```js
 var o = {
 name: 'andy'
 };

function fn(a, b) {
	console.log(this);
	console.log(a + b);
};
var f = fn.bind(o, 1, 2); //此处的f是bind返回的新函数
f();//调用新函数  this指向的是对象o 参数使用逗号隔开
```

![image-20211007103017634](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103017634.png)

### 严格模式

#### 1、开启严格模式

严格模式可以应用到整个脚本或个别函数中。因此在使用时，我们可以将严格模式分为为脚本开启严格模式和为函数开启严格模式两种情况。

- 情况一 :为脚本开启严格模式

  - 有的 script 脚本是严格模式，有的 script 脚本是正常模式，这样不利于文件合并，所以可以将整个脚本文件放在一个立即执行的匿名函数之中。这样独立创建一个作用域而不影响其他
    script 脚本文件。

    ```js
    (function (){
      //在当前的这个自调用函数中有开启严格模式，当前函数之外还是普通模式
    　　　　"use strict";
           var num = 10;
    　　　　function fn() {}
    })();
    
    //或者 
    
    //当前script标签开启了严格模式，第一行
    <script>"use strict"; </script>
    ```

- 情况二: 为函数开启严格模式

  - 要给某个函数开启严格模式，需要把“use strict”;  (或 'use strict'; ) 声明放在函数体所有语句之前。

    ```js
    function fn(){
    　　"use strict";
    　　return "123";
    } 
    //当前fn函数开启了严格模式
    ```

#### 2、严格模式中的变化

```js
'use strict'
num = 10 
console.log(num)//严格模式后使用未声明的变量
--------------------------------------------------------------------------------
var num2 = 1;
delete num2;//严格模式不允许删除变量
--------------------------------------------------------------------------------
function fn() {
 console.log(this); // 严格模式下全局作用域中函数中的 this 是 undefined
}
fn();  
---------------------------------------------------------------------------------
function Star() {
	 this.sex = '男';
}
// Star();严格模式下,如果 构造函数不加new调用, this 指向的是undefined 如果给他赋值则 会报错.
var ldh = new Star();
console.log(ldh.sex);
----------------------------------------------------------------------------------
setTimeout(function() {
  console.log(this); //严格模式下，定时器 this 还是指向 window
}, 2000);  
```

### 高阶函数

1、接收函数作为参数；

2、将函数作为返回值输出。

### 闭包

闭包（closure）指有权访问另一个函数作用域中变量的函数。简单理解就是 ，一个作用域可以访问另外一个函数内部的局部变量。 

![image-20211007103032723](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103032723.png)

#### 闭包的作用

作用：延伸变量的作用范围。

```js
 function fn() {
   var num = 10;
   function fun() {
       console.log(num);
 	}
    return fun;
 }
var f = fn();
f();
```

### 递归

**递归：**如果一个函数在内部可以调用其本身，那么这个函数就是递归函数。简单理解:函数内部自己调用自己, 这个函数就是递归函数

**注意：**递归函数的作用和循环效果一样，由于递归很容易发生“栈溢出”错误（stack overflow），所以必须要加退出条件return。

```js
//利用递归函数求1~n的阶乘 1 * 2 * 3 * 4 * ..n
 function fn(n) {
     if (n == 1) { //结束条件
       return 1;
     }
     return n * fn(n - 1);
 }
 console.log(fn(3));
```

### 拷贝

#### 1、浅拷贝

object.assign(target , sources)

- target: 拷贝给谁
- sources： 拷贝谁

#### 2、深拷贝

利用递归函数来深拷贝。//需要判断值为什么类型

### 正则表达式

正则表达式（ Regular Expression ）是用于匹配字符串中字符组合的模式。在JavaScript中，正则表达式也是对象。

#### 1、正则表达式在js中的使用

##### 正则表达式的创建

在 JavaScript 中，可以通过两种方式创建一个正则表达式。

方式一：通过调用RegExp对象的构造函数创建 

```js
var regexp = new RegExp(/123/);
console.log(regexp);
```

方式二：利用字面量创建 正则表达式（常用）

```js
 var rg = /123/;
```

##### 测试正则表达式 

test() 正则对象方法，用于检测字符串是否符合该规则，该对象会返回 true 或 false，其参数是测试字符串。

```js
var rg = /123/;
console.log(rg.test(123));//匹配字符中是否出现123  出现结果为true
console.log(rg.test('abc'));//匹配字符中是否出现123 未出现结果为false
```

![image-20211007103054036](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103054036.png)

#### 2、正则表达式中的特殊字符

##### 2.1、边界符

正则表达式中的边界符（位置符）用来提示字符所处的位置，主要有两个字符

| 边界符 | 说明                           |
| ------ | ------------------------------ |
| ^      | 表示匹配行首的文本（以谁开始） |
| $      | 表示匹配行尾的文本（以谁结束） |

如果 ^和 $ 在一起，表示必须是精确匹配。

```js
var rg = /abc/; // 正则表达式里面不需要加引号 不管是数字型还是字符串型
// /abc/ 只要包含有abc这个字符串返回的都是true
console.log(rg.test('abc'));
console.log(rg.test('abcd'));
console.log(rg.test('aabcd'));
console.log('---------------------------');
var reg = /^abc/;
console.log(reg.test('abc')); // true
console.log(reg.test('abcd')); // true
console.log(reg.test('aabcd')); // false
console.log('---------------------------');
var reg1 = /^abc$/; // 精确匹配 要求必须是 abc字符串才符合规范
console.log(reg1.test('abc')); // true
console.log(reg1.test('abcd')); // false
console.log(reg1.test('aabcd')); // false
console.log(reg1.test('abcabc')); // false
```

##### 2.2、字符类

字符类表示有一系列字符可供选择，只要匹配其中一个就可以了。所有可供选择的字符都放在方括号内。

表示有一系列字符可供选择，只要匹配其中一个就可以了

```js
var rg = /[abc]/; // 只要包含有a 或者 包含有b 或者包含有c 都返回为true
console.log(rg.test('andy'));//true
console.log(rg.test('baby'));//true
console.log(rg.test('color'));//true
console.log(rg.test('red'));//false
var rg1 = /^[abc]$/; // 三选一 只有是a 或者是 b  或者是c 这三个字母才返回 true
console.log(rg1.test('aa'));//false
console.log(rg1.test('a'));//true
console.log(rg1.test('b'));//true
console.log(rg1.test('c'));//true
console.log(rg1.test('abc'));//true
----------------------------------------------------------------------------------
var reg = /^[a-z]$/ //26个英文字母任何一个字母返回 true  - 表示的是a 到z 的范围  
console.log(reg.test('a'));//true
console.log(reg.test('z'));//true
console.log(reg.test('A'));//false
-----------------------------------------------------------------------------------
//字符组合
var reg1 = /^[a-zA-Z0-9]$/; // 26个英文字母(大写和小写都可以)任何一个字母返回 true  
------------------------------------------------------------------------------------
//取反 方括号内部加上 ^ 表示取反，只要包含方括号内的字符，都返回 false 。
var reg2 = /^[^a-zA-Z0-9]$/;
console.log(reg2.test('a'));//false
console.log(reg2.test('B'));//false
console.log(reg2.test(8));//false
console.log(reg2.test('!'));//true
```

##### 2.3、量词符

量词符用来设定某个模式出现的次数。

| 量词  | 说明            |
| ----- | --------------- |
| *     | 重复0次或更多次 |
| +     | 重复1次或更多次 |
| ?     | 重复0次或1次    |
| {n}   | 重复n次         |
| {n,}  | 重复n次或更多次 |
| {n,m} | 重复n到m次      |

##### 2.4、预定义类

预定义类指的是某些常见模式的简写方式.

![image-20211007103113291](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103113291.png)

#### 括号总结

1.大括号  量词符.  里面表示重复次数

2.中括号 字符集合。匹配方括号中的任意字符. 

3.小括号表示优先级

#### 正则替换replace

replace() 方法可以实现替换字符串操作，用来替换的参数可以是一个字符串或是一个正则表达式。

（）里的正则： /表达式/[swith]

​						1、g: 全局匹配

​						2、i：忽略大小写

​						3、gi：全局匹配，忽略大小写																				

```js
var str = 'andy和red';
var newStr = str.replace('andy', 'baby');
console.log(newStr)//baby和red
//等同于 此处的andy可以写在正则表达式内
var newStr2 = str.replace(/andy/, 'baby');
console.log(newStr2)//baby和red
//全部替换
var str = 'abcabc'
var nStr = str.replace(/a/,'哈哈')
console.log(nStr) //哈哈bcabc
//全部替换g
var nStr = str.replace(/a/a,'哈哈')
console.log(nStr) //哈哈bc哈哈bc
//忽略大小写i
var str = 'aAbcAba';
var newStr = str.replace(/a/gi,'哈哈')//"哈哈哈哈bc哈哈b哈哈"
```

**案例:过滤敏感词汇**

```js
<textarea name="" id="message"></textarea> <button>提交</button>
<div></div>
<script>
    var text = document.querySelector('textarea');
    var btn = document.querySelector('button');
    var div = document.querySelector('div');
    btn.onclick = function() {
    	div.innerHTML = text.value.replace(/激情|gay/g, '**');
    }
</script>
```

### ES6语法

#### let

##### 块级作用域

et声明的变量只在所处于的块级有效

```
 if (true) { 
     let a = 10;
 }
console.log(a) // a is not defined
```

**注意：**使用let关键字声明的变量才具有块级作用域，使用var声明的变量不具备块级作用域特性。

##### 不存在变量提升

```
console.log(a); // a is not defined 
let a = 20;
```

##### 暂时性死区

利用let声明的变量会绑定在这个块级作用域，不会受外界的影响

```javascript
 var tmp = 123;
 if (true) { 
     tmp = 'abc';
     let tmp; 
 } 
```

##### 经典面试题

```javascript
 var arr = [];
 for (var i = 0; i < 2; i++) {
     arr[i] = function () {
         console.log(i); 
     }
 }
 arr[0]();
 arr[1]();

```

![image-20211007103135616](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103135616.png)

**经典面试题图解：**此题的关键点在于变量i是全局的，函数执行时输出的都是全局作用域下的i值。

```javascript
 let arr = [];
 for (let i = 0; i < 2; i++) {
     arr[i] = function () {
         console.log(i); 
     }
 }
 arr[0]();
 arr[1]();

```

![image-20211007103146743](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103146743.png)

**经典面试题图解：**此题的关键点在于每次循环都会产生一个块级作用域，每个块级作用域中的变量都是不同的，函数执行时输出的是自己上一级（循环产生的块级作用域）作用域下的i值.

##### 小结

- let关键字就是用来声明变量的
- 使用let关键字声明的变量具有块级作用域
- 在一个大括号中 使用let关键字声明的变量才具有块级作用域 var关键字是不具备这个特点的
- 防止循环变量变成全局变量
- 使用let关键字声明的变量没有变量提升
- 使用let关键字声明的变量具有暂时性死区特性

#### const

声明常量，常量就是值（内存地址）不能变化的量

##### 具有块级作用域

```javascript
 if (true) { 
     const a = 10;
 }
console.log(a) // a is not defined
```

##### 声明常量时必须赋值

```javascript
const PI; // Missing initializer in const declaration
```

##### 常量赋值后，值不能修改

```javascript
const PI = 3.14;
PI = 100; // Assignment to constant variable.

const ary = [100, 200];
ary[0] = 'a';
ary[1] = 'b';
console.log(ary); // ['a', 'b']; 
ary = ['a', 'b']; // Assignment to constant variable.
```

##### 小结

- const声明的变量是一个常量
- 既然是常量不能重新进行赋值，如果是基本数据类型，不能更改值，如果是复杂数据类型，不能更改地址值
- 声明 const时候必须要给定值

#### let、const、var 的区别

- 使用 var 声明的变量，其作用域为该语句所在的函数内，且存在变量提升现象
- 使用 let 声明的变量，其作用域为该语句所在的代码块内，不存在变量提升
- 使用 const 声明的是常量，在后面出现的代码中不能再修改该常量的值

![image-20211007103200630](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103200630.png)

#### 解构赋值

##### 数组解构

```javascript
 let [a, b, c] = [1, 2, 3];
 console.log(a)//1
 console.log(b)//2
 console.log(c)//3
//如果解构不成功，变量的值为undefined
```

##### 对象解构

```javascript
 let person = { name: 'zhangsan', age: 20 }; 
 let { name, age } = person;
 console.log(name); // 'zhangsan' 
 console.log(age); // 20

 let {name: myName, age: myAge} = person; // myName myAge 属于别名
 console.log(myName); // 'zhangsan' 
 console.log(myAge); // 20

```

##### 小结

- 解构赋值就是把数据结构分解，然后给变量进行赋值
- 如果结构不成功，变量跟数值个数不匹配的时候，变量的值为undefined
- 数组解构用中括号包裹，多个变量用逗号隔开，对象解构用花括号包裹，多个变量用逗号隔开
- 利用解构赋值能够让我们方便的去取对象中的属性跟方法

#### 箭头函数

ES6中新增的定义函数的方式。

```javascript
() => {} //()：代表是函数； =>：必须要的符号，指向哪一个代码块；{}：函数体
const fn = () => {}//代表把一个函数赋值给fn
```

1、函数体中只有一句代码，且代码的执行结果就是返回值，可以省略大括号

```javascript
 function sum(num1, num2) { 
     return num1 + num2; 
 }
 //es6写法
 const sum = (num1, num2) => num1 + num2; 

```

2、如果形参只有一个，可以省略小括号

```javascript
 function fn (v) {
     return v;
 } 
//es6写法
 const fn = v => v;

```

3、箭头函数不绑定this关键字，箭头函数中的this，指向的是函数定义位置的上下文this

```javascript
const obj = { name: '张三'} 
 function fn () { 
     console.log(this);//this 指向 是obj对象
     return () => { 
         console.log(this);//this 指向 的是箭头函数定义的位置，那么这个箭头函数定义在fn里面，而这个fn指向是的obj对象，所以这个this也指向是obj对象
     } 
 } 
 const resFn = fn.call(obj); 
 resFn();

```

##### 小结

- 箭头函数中不绑定this，箭头函数中的this指向是它所定义的位置，可以简单理解成，定义箭头函数中的作用域的this指向谁，它就指向谁
- 箭头函数的优点在于解决了this执行环境所造成的一些问题。比如：解决了匿名函数this指向的问题（匿名函数的执行环境具有全局性），包括setTimeout和setInterval中使用this所造成的问题

##### 面试题

```javascript
var age = 100;

var obj = {
	age: 20,
	say: () => {
		alert(this.age)
	}
}

obj.say();//箭头函数this指向的是被声明的作用域里面，而对象没有作用域的，所以箭头函数虽然在对象中被定义，但是this指向的是全局作用域
```

#### 剩余参数

剩余参数语法允许我们将一个不定数量的参数表示为一个数组，不定参数定义方式，这种方式很方便的去声明不知道参数情况下的一个函数

```javascript
function sum (first, ...args) {
     console.log(first); // 10
     console.log(args); // [20, 30] 
 }
 sum(10, 20, 30)
```

##### 剩余参数和解构配合使用

```javascript
let students = ['wangwu', 'zhangsan', 'lisi'];
let [s1, ...s2] = students; 
console.log(s1);  // 'wangwu' 
console.log(s2);  // ['zhangsan', 'lisi']

```

#### ES6 的内置对象扩展

##### Array 的扩展方法

###### 1、扩展运算符（展开语法）

可以将数组或者对象转为用逗号分隔的参数序列

```js
 let ary = [1, 2, 3];
 ...ary  // 1, 2, 3
 console.log(...ary);    // 1 2 3,相当于下面的代码
 console.log(1,2,3);
```

扩展运算符可以应用于合并数组

```js
// 方法一 
 let ary1 = [1, 2, 3];
 let ary2 = [3, 4, 5];
 let ary3 = [...ary1, ...ary2];
 // 方法二 
 ary1.push(...ary2);
```

将类数组或可遍历对象转换为真正的数组

```javascript
let oDivs = document.getElementsByTagName('div'); 
oDivs = [...oDivs];
```

###### 2、构造函数方法：Array.from()

将伪数组或可遍历对象转换为真正的数组

```javascript
//定义一个集合
let arrayLike = {
    '0': 'a',
    '1': 'b',
    '2': 'c',
    length: 3
}; 
//转成数组
let arr2 = Array.from(arrayLike); // ['a', 'b', 'c']
```

方法还可以接受第二个参数，作用类似于数组的map方法，用来对每个元素进行处理，将处理后的值放入返回的数组

```javascript
 let arrayLike = { 
     "0": 1,
     "1": 2,
     "length": 2
 }
 let newAry = Array.from(arrayLike, item => item *2)//[2,4]

```

注意：如果是对象，那么属性需要写对应的索引

###### 实例方法：find()

用于找出**第一个符合条件的数组成员**，如果没有找到返回undefined

```javascript
let ary = [{
     id: 1,
     name: '张三'
 }, { 
     id: 2,
     name: '李四'
 }]; 
 let target = ary.find((item, index) => item.id == 2);//找数组里面符合条件的值，当数组中元素id等于2的查找出来，注意，只会匹配第一个

```

###### 实例方法：findIndex()

用于找出第一个符合条件的数组成员的位置，如果没有找到返回-1

```javascript
let ary = [1, 5, 10, 15];
let index = ary.findIndex((value, index) => value > 9); 
console.log(index); // 2
```

###### 实例方法：includes()

判断某个数组是否包含给定的值，返回布尔值。

```javascript
[1, 2, 3].includes(2) // true 
[1, 2, 3].includes(4) // false
```

##### String 的扩展方法

###### 模板字符串

ES6新增的创建字符串的方式，使用反引号定义

```javascript
let name = `zhangsan`;
```

模板字符串中可以解析变量

```javascript
let name = '张三'; 
let sayHello = `hello,my name is ${name}`; // hello, my name is zhangsan
```

模板字符串中可以换行

```javascript
 let result = { 
     name: 'zhangsan', 
     age: 20,
     sex: '男' 
 } 
 let html = ` <div>
     <span>${result.name}</span>
     <span>${result.age}</span>
     <span>${result.sex}</span>
 </div> `;
```

在模板字符串中可以调用函数

```javascript
const sayHello = function () { 
    return '哈哈哈哈 追不到我吧 我就是这么强大';
 }; 
 let greet = `${sayHello()} 哈哈哈哈`;
 console.log(greet); // 哈哈哈哈 追不到我吧 我就是这么强大 哈哈哈哈
```

###### 实例方法：startsWith() 和 endsWith()

- startsWith()：表示参数字符串是否在原字符串的头部，返回布尔值
- endsWith()：表示参数字符串是否在原字符串的尾部，返回布尔值

```javascript
let str = 'Hello world!';
str.startsWith('Hello') // true 
str.endsWith('!')       // true
```

###### 实例方法：repeat()

repeat方法表示将原字符串重复n次，返回一个新字符串

```javascript
'x'.repeat(3)      // "xxx" 
'hello'.repeat(2)  // "hellohello"
```

##### Set 数据结构

ES6 提供了新的数据结构  Set。它类似于数组，但是**成员的值都是唯一的，没有重复的值**。

Set本身是一个构造函数，用来生成  Set  数据结构

```javascript
const s = new Set();
```

Set函数可以接受一个数组作为参数，用来初始化。

```javascript
const set = new Set([1, 2, 3, 4, 4]);//{1, 2, 3, 4}
```

###### 实例方法

- add(value)：添加某个值，返回 Set 结构本身
- delete(value)：删除某个值，返回一个布尔值，表示删除是否成功
- has(value)：返回一个布尔值，表示该值是否为 Set 的成员
- clear()：清除所有成员，没有返回值

```javascript
 const s = new Set();
 s.add(1).add(2).add(3); // 向 set 结构中添加值 
 s.delete(2)             // 删除 set 结构中的2值   
 s.has(1)                // 表示 set 结构中是否有1这个值 返回布尔值 
 s.clear()               // 清除 set 结构中的所有值
 //注意：删除的是元素的值，不是代表的索引
```

###### 遍历

Set 结构的实例与数组一样，也拥有forEach方法，用于对每个成员执行某种操作，没有返回值。

```javascript
s.forEach(value => console.log(value))
```

------

# Web  API

------

## DOM

文档对象模型        编程接口

```
console.dir 打印我们返回的元素对象 更好的查看里面的属性和方法
```

### 获取元素

#### 1、根据ID获取

```
语法：document.getElementById("id")
作用：根据ID获取元素对象
参数：id值，区分大小写的字符串
返回值：元素对象 或 null
```

#### 2、根据标签名获取元素

```
语法：document.getElementsByTagName('标签名')
作用：根据标签名获取元素对象
参数：标签名
返回值：元素对象集合（伪数组，数组元素是元素对象）


//element.getElementsByTagName()  可以得到这个元素里面的某些标签
        var nav = document.getElementById('nav'); // 这个获得nav 元素
        var navLis = nav.getElementsByTagName('li');
```

#### 3、H5新增获取元素方式

![image-20211006204800581](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204800581.png)

```
document.getElementsByClassName('box');
document.querySelector('.box');
document.querySelectorAll('.box');  返回一个集合
```

### 获取特殊元素（body，html）

![image-20211006204814216](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204814216.png)

### 事件

#### 事件三要素

- 事件源（谁）：触发事件的元素
- 事件类型（什么事件）： 例如 click 点击事件
- 事件处理程序（做啥）：事件触发后要执行的代码(函数形式)，事件处理函数

```
<body>
    <button id="btn">唐伯虎</button>
    <script>
        // 点击一个按钮，弹出对话框
        // 1. 事件是有三部分组成  事件源  事件类型  事件处理程序   我们也称为事件三要素
        //(1) 事件源 事件被触发的对象   谁  按钮
        var btn = document.getElementById('btn');
        //(2) 事件类型  如何触发 什么事件 比如鼠标点击(onclick) 还是鼠标经过 还是键盘按下
        //(3) 事件处理程序  通过一个函数赋值的方式 完成
        btn.onclick = function() {
            alert('点秋香');
        }
    </script>
</body>
```

#### 常见的鼠标事件

![image-20211006204828983](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204828983.png)

mouseenter  鼠标经过，不会冒泡，只有经过自身才会触发事件；

mouseleave  鼠标离开，不会冒泡，只有经过自身才会触发事件；

#### 高级事件

##### 注册事件

![image-20211006204943447](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204943447.png)

###### 1、addEventListener()事件监听（IE9以后支持）

![image-20211006204959097](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204959097.png)

![image-20211006205012049](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205012049.png)

```
btns[1].addEventListener('click', function() {
            alert(22);
        })
```

###### 2、attacheEvent()事件监听（IE678支持）

![image-20211006205028197](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205028197.png)

​	eventTarget.attachEvent()方法将指定的监听器注册到 eventTarget（目标对象） 上，当该对象触发指定的事件时，指定的回调函数就会被执行。

![image-20211006205041057](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205041057.png)

###### 事件监听兼容性解决方案

封装一个函数，函数中判断浏览器的类型：

![image-20211006205119596](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205119596.png)

##### 删除事件（解绑事件）

![image-20211006205130496](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205130496.png)

```
            // 1. 传统方式删除事件
            divs[0].onclick = null;
            
            // 2. removeEventListener 删除事件
        divs[1].removeEventListener('click', fn) // 里面的fn 不需要调用加小括号
```

###### 删除事件兼容性解决方案

![image-20211006205146722](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205146722.png)

#### DOM 事件流

DOM 事件流会经历3个阶段： 

捕获阶段

当前目标阶段

冒泡阶段 

![image-20211006205254481](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205254481.png)

![image-20211006205309332](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205309332.png)

#### 事件对象

![image-20211006205321743](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205321743.png)

###### 事件对象的兼容性处理

![image-20211006205332165](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205332165.png)

```
	只要“||”前面为false, 不管“||”后面是true 还是 false，都返回 “||” 后面的值。
只要“||”前面为true, 不管“||”后面是true 还是 false，都返回 “||” 前面的值。
	
	<div>123</div>
    <script>
        var div = document.querySelector('div');
        div.onclick = function(e) {
                // 事件对象
                e = e || window.event;
                console.log(e);
        }
    </script>
```

#### 事件对象的属性和方法

![image-20211006205343450](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205343450.png)

1\3\6\7

#### 禁止选中文字和禁止右键菜单

```
		// 1. contextmenu 我们可以禁用右键菜单        document.addEventListener('contextmenu', function(e) {
                e.preventDefault();
        })
        
        // 2. 禁止选中文字 selectstart        document.addEventListener('selectstart', function(e) {
            e.preventDefault();
        })
```

#### 鼠标事件对象

![image-20211006205555410](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205555410.png)

#### 常用的键盘事件

![image-20211006205625497](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205625497.png)

![image-20211006205633529](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205633529.png)

####  键盘事件对象

![image-20211006205700652](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205700652.png)

![image-20211006205708314](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205708314.png)

```
document.addEventListener('keyup', function(e) {
            console.log('up:' + e.keyCode);
            // 我们可以利用keycode返回的ASCII码值来判断用户按下了那个键
}
```

### 操作元素

#### 改变元素内容

常用：innerHTML

![image-20211006205744646](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205744646.png)

**innerText和innerHTML的区别**

- 获取内容时的区别：

​	innerText会去除空格和换行，而innerHTML会保留空格和换行	

- 设置内容时的区别：

​	innerText不会识别html，而innerHTML会识别

#### 表单元素的属性操作

**获取属性的值**

> 元素对象.属性名

**设置属性的值**

> 元素对象.属性名 = 值
>
> 表单元素中有一些属性如：disabled、checked、selected，元素对象的这些属性的值是布尔型。

```
<body>
    <button>按钮</button>
    <input type="text" value="输入内容">
    <script>
        // 1. 获取元素
        var btn = document.querySelector('button');
        var input = document.querySelector('input');
        // 2. 注册事件 处理程序
        btn.onclick = function() {
            // 表单里面的值 文字内容是通过 value 来修改的
            input.value = '被点击了';
            // 如果想要某个表单被禁用 不能再点击 disabled  我们想要这个按钮 button禁用
            // btn.disabled = true;
            this.disabled = true;
            // this 指向的是事件函数的调用者 btn
        }
    </script>
</body>
```



#### 样式属性操作

![image-20211006205812843](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205812843.png)

##### 方式1：通过操作style属性

> 元素对象的style属性也是一个对象！
>
> 元素对象.style.样式属性 = '值';
>
> ![image-20211006205823704](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205823704.png)

##### 方式2：通过操作className属性

> 元素对象.className = '值';
>
> 因为class是关键字，所有使用className。
>
> ![image-20211006205843309](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006205843309.png)
>
> ```
> //如果想要保留原先的类名，我们可以这么做 多类名选择器
>             // this.className = 'change';
>             this.className = 'first change';
> ```

### 自定义属性操作

#### 获取属性值

![image-20211006210044119](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210044119.png)

```
    <div id="demo" index="1" class="nav"></div>
    <script>
        var div = document.querySelector('div');
        // 1. 获取元素的属性值
        // (1) element.属性
        console.log(div.id);
        //(2) element.getAttribute('属性')  get得到获取 attribute 属性的意思 我们程序员自己添加的属性我们称为自定义属性 index
        console.log(div.getAttribute('id'));
        console.log(div.getAttribute('index'));
	</script>
```

#### 设置属性值

![image-20211006210056003](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210056003.png)

```
	 	// 2. 设置元素属性值
        // (1) element.属性= '值'
        div.id = 'test';
        div.className = 'navs';
        // (2) element.setAttribute('属性', '值');  主要针对于自定义属性
        div.setAttribute('index', 2);
        div.setAttribute('class', 'footer'); // class 特殊  这里面写的就是
```

#### 移出属性

![image-20211006210106203](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210106203.png)

```
		// class 不是className
        // 3 移除属性 removeAttribute(属性)    
        div.removeAttribute('index');
```

#### H5自定义属性

![image-20211006210122489](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210122489.png)

![image-20211006210131332](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210131332.png)

### 节点操作

  节点至少拥有nodeType（节点类型）、nodeName（节点名称）和nodeValue（节点值）这三个基本属性。

1. nodeType
   **1.1 元素节点，nodeType为1**
   1.2 属性节点，nodeType为2
   1.3 文本节点，nodeType为3（文本节点包含文字、空格、换行等）

#### 父级节点

![image-20211006210157915](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210157915.png)

#### 子节点

![image-20211006210209121](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210209121.png)

![image-20211006210220024](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210220024.png)

##### **第1个子节点**

![image-20211006210232664](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210232664.png)

##### **最后1个子节点**

![image-20211006210242065](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210242065.png)

##### **第1个子元素节点**

![image-20211006210253388](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210253388.png)

##### **最后1个子元素节点**

![image-20211006210303986](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210303986.png)

​	**<u>实际开发中，firstChild 和 lastChild 包含其他节点，操作不方便，而 firstElementChild 和 lastElementChild 又有兼容性问题，那么我们如何获取第一个子元素节点或最后一个子元素节点呢？</u>**

![image-20211006210314086](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210314086.png)

#### 兄弟节点 

```
//包括元素和文本节点
node.nextSibling   //下一个
node.previousSibling  //上一个


//元素节点    常用
node.nextElementSibling   //下一个兄弟元素节点
node.previousElementSibling   //上一个兄弟元素节点
```

#### 创建节点

![image-20211006210338486](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210338486.png)

#### 添加节点

![image-20211006210346708](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210346708.png)

常用第一种；

#### 删除节点

```
node.removeChild(child)
```

#### 复制（克隆）节点

![image-20211006210416492](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210416492.png)

## BOM

BOM（Browser Object Model）即浏览器对象模型，它提供了独立于内容而与浏览器窗口进行交互的对象，其核心对象是 window。

###  window对象的常见事件

#### 页面（窗口）加载事件

1、**当文档内容完全加载完成**会触发该事件(包括图像、脚本文件、CSS 文件等), 就调用的处理函数。

![image-20211006210451191](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210451191.png)

![image-20211006210500748](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210500748.png)

2、仅当DOM加载完成，不包括样式表，图片，flash等等。

![image-20211006210514633](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210514633.png)

注意：

​	IE9以上才支持！！！

​	如果页面的图片很多的话, 从用户访问到onload触发可能需要较长的时间, 交互效果就不能实现，必然影响用户的体验，此时用 DOMContentLoaded 事件比较合适。

#### 调整窗口大小事件

![image-20211006210525660](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210525660.png)

window.onresize 是调整窗口大小加载事件,  当触发时就调用的处理函数。

注意：

1. 只要窗口大小发生像素变化，就会触发这个事件。

2. 我们经常利用这个事件完成响应式布局。 window.innerWidth 当前屏幕的宽度

### 定时器

**重点：**

​		**防止刷新时有空白，需先调用一次定时器；**

#### setTimeout() 炸弹定时器

![image-20211006210551904](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210551904.png)

![image-20211006210600209](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210600209.png)

![image-20211006210610314](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210610314.png)

###### 使用方式：

```
1、
	setTimeout(function() {}， 延时时长)
	
2、常用
	callback();  //防止刷新时有空白，需先调用一次定时器；
	function callback() {};
	//调用
	setTimeout( callback, 延时时长)
```

###### 清除定时器

```
clearTimeout(定时器名)；
```

#### setInterval() 闹钟定时器

![image-20211006210626654](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210626654.png)

```
 	<script>
        // 1. setInterval 
        setInterval(function() {
            console.log('继续输出');
        }, 1000);
    </script>
```

###### 使用方式：

```
1、
	setInerval(function() {}， 延时时长)
	
2、常用
	callback();  //防止刷新时有空白，需先调用一次定时器；
	function callback() {};
	//调用
	setInerval( callback, 延时时长)
```



###### 清除定时器

```
clearInterval(定时器名)；
```

### location对象

![1551322373704](E:/Materials/自学/黑马全栈教程/07-10 JavaScript网页编程/02-WebAPI编程资料/Web APIs-day04/4-笔记/images/1551322373704.png)

![1551322387201](E:/Materials/自学/黑马全栈教程/07-10 JavaScript网页编程/02-WebAPI编程资料/Web APIs-day04/4-笔记/images/1551322387201.png)

#### location 对象的属性

#### location 对象的属性

![image-20211006210728199](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210728199.png)

#### location对象的常见方法

![image-20211006210741076](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210741076.png)

### history对象

window对象给我们提供了一个 history对象，与浏览器历史记录进行交互。该对象包含用户（在浏览器窗口中）访问过的URL。

![image-20211006210751999](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006210751999.png)

## PC端网页特效

### 元素偏移量 (offset)

1. 获得元素距离带有定位父元素的位置
2. 获得元素自身的大小（宽度高度）
3. 注意：返回的数值都不带单位
4. 注意：offsetWidth 包含padding+border+width;
5. 注意：offsetParent如果父亲没有定位,则返回body;

![image-20211006211029772](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211029772.png)

### 元素可视区 (client )

获取该元素的边框大小、元素大小等。

![image-20211006211059039](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211059039.png)

### 元素滚动 (scroll ) 

获取滚动距离

![图片5](E:/Materials/自学/黑马前端最新就业班-0基础小白到就业/03-阶段三：JavaScript 网页编程资料/02-WebAPI编程资料/Web APIs-day05（12-14小节）/4-笔记/images/图片5.png)

![图片6](E:/Materials/自学/黑马前端最新就业班-0基础小白到就业/03-阶段三：JavaScript 网页编程资料/02-WebAPI编程资料/Web APIs-day05（12-14小节）/4-笔记/images/图片6.png)

页面被卷去的头部：window.pageYoffset

元素被卷去的头部：element.scrollTop 

页面滚动：window.scroll(0,0)      //不跟单位

### 动画函数封装

核心原理：通过定时器 setInterval() 不断移动盒子位置。

实现步骤：

1. 获得盒子当前位置
2. 让盒子在当前位置加上1个移动距离
3. 利用定时器不断重复这个操作
4. 加一个结束定时器的条件
5. 注意此元素需要添加定位，才能使用element.style.left

#### 动画函数给不同元素记录不同定时器 

```
 function animate(obj, target) {
            // 当我们不断的点击按钮，这个元素的速度会越来越快，因为开启了太多的定时器
            // 解决方案就是 让我们元素只有一个定时器执行
            // 先清除以前的定时器，只保留当前的一个定时器执行
            clearInterval(obj.timer);
            obj.timer = setInterval(function() {
                if (obj.offsetLeft >= target) {
                	obj.style.left = target + "px";
                    // 停止动画 本质是停止定时器
                    clearInterval(obj.timer);
                }
                obj.style.left = obj.offsetLeft + 1 + 'px';

            }, 30);
        }

```

#### 缓动效果原理  

核心算法： (目标值 - 现在的位置)   /  10  =  做为每次移动的距离步长。

取整：step = step > 0 ? Math.ceil(step) : Math.floor(step);

#### 动函数添加回调函数 

回调函数原理：函数可以作为一个参数。将这个函数作为参数传到另一个函数里面，当那个函数执行完之后，再执行传进去的这个函数，这个过程就叫做回调。

回调函数写的位置：定时器结束的位置。

#### 动画完整版代码:

```
1、左右运动
function animate(obj, target, callback) {
    // console.log(callback);  callback = function() {}  调用的时候 callback()

    // 先清除以前的定时器，只保留当前的一个定时器执行
    clearInterval(obj.timer);
    obj.timer = setInterval(function() {
        // 步长值写到定时器的里面
        // 把我们步长值改为整数 不要出现小数的问题
        // var step = Math.ceil((target - obj.offsetLeft) / 10);
        var step = (target - obj.offsetLeft) / 10;
        step = step > 0 ? Math.ceil(step) : Math.floor(step);
        if (obj.offsetLeft == target) {
            // 停止动画 本质是停止定时器
            clearInterval(obj.timer);
            // 回调函数写到定时器结束里面
            // if (callback) {
            //     // 调用函数
            //     callback();
            // }
            callback && callback();
        }
        // 把每次加1 这个步长值改为一个慢慢变小的值  步长公式：(目标值 - 现在的位置) / 10
        obj.style.left = obj.offsetLeft + step + 'px';

    }, 15);
}
-------------------------------------------------------------------------------------------------
2、页面回到顶部
function animateGoTop(target, callback) {
            clearInterval(window.timer);
            window.timer = setInterval(function() {
                // 步长值
                // var step = Math.ceil((target - obj.offsetLeft) / 10);
                var step = (target - window.pageYOffset) / 10;
                step = step > 0 ? Math.ceil(step) : Math.floor(step);

                if (window.pageYOffset == target) {
                    // 停止动画 本质是停止定时器
                    clearInterval(window.timer);
                    callback && callback();
                }
                // 设置页面滚动到的位置
                window.scroll(0, window.pageYOffset + step);
            }, 15);
        }
```

### 节流阀

节流阀目的：当上一个函数动画内容执行完毕，再去执行下一个函数动画，让事件无法连续触发。

核心实现思路：利用回调函数，添加一个变量来控制，锁住函数和解锁函数。

```
var  flag = true;
if (flag) {
	flag = false;   //先关闭节流阀
	.
	.
	.
	animate(obj，target , function() {
		flag = true;   //打开节流阀
	})
}
```

### 网页轮播图

轮播图也称为焦点图，是网页中比较常见的网页特效。

功能需求：

​	1.鼠标经过轮播图模块，左右按钮显示，离开隐藏左右按钮。

​	2.点击右侧按钮一次，图片往左播放一张，以此类推，左侧按钮同理。

​	3.图片播放的同时，下面小圆圈模块跟随一起变化。

​	4.点击小圆圈，可以播放相应图片。

​	5.鼠标不经过轮播图，轮播图也会自动播放图片。

​	6.鼠标经过，轮播图模块， 自动播放停止。

```
window.addEventListener('load', function() {
    // 1. 获取元素
    var arrow_l = document.querySelector('.arrow-l');
    var arrow_r = document.querySelector('.arrow-r');
    var focus = document.querySelector('.focus');
    var focusWidth = focus.offsetWidth;
    // 2. 鼠标经过focus 就显示隐藏左右按钮
    focus.addEventListener('mouseenter', function() {
        arrow_l.style.display = 'block';
        arrow_r.style.display = 'block';
        clearInterval(timer);
        timer = null; // 清除定时器变量
    });
    focus.addEventListener('mouseleave', function() {
        arrow_l.style.display = 'none';
        arrow_r.style.display = 'none';
        timer = setInterval(function() {
            //手动调用点击事件
            arrow_r.click();
        }, 2000);
    });
    // 3. 动态生成小圆圈  有几张图片，我就生成几个小圆圈
    var ul = focus.querySelector('ul');
    var ol = focus.querySelector('.circle');
    // console.log(ul.children.length);
    for (var i = 0; i < ul.children.length; i++) {
        // 创建一个小li 
        var li = document.createElement('li');
        // 记录当前小圆圈的索引号 通过自定义属性来做 
        li.setAttribute('index', i);
        // 把小li插入到ol 里面
        ol.appendChild(li);
        // 4. 小圆圈的排他思想 我们可以直接在生成小圆圈的同时直接绑定点击事件
        li.addEventListener('click', function() {
            // 干掉所有人 把所有的小li 清除 current 类名
            for (var i = 0; i < ol.children.length; i++) {
                ol.children[i].className = '';
            }
            // 留下我自己  当前的小li 设置current 类名
            this.className = 'current';
            // 5. 点击小圆圈，移动图片 当然移动的是 ul 
            // ul 的移动距离 小圆圈的索引号 乘以 图片的宽度 注意是负值
            // 当我们点击了某个小li 就拿到当前小li 的索引号
            var index = this.getAttribute('index');
            // 当我们点击了某个小li 就要把这个li 的索引号给 num  
            num = index;
            // 当我们点击了某个小li 就要把这个li 的索引号给 circle  
            circle = index;
            // num = circle = index;
            console.log(focusWidth);
            console.log(index);

            animate(ul, -index * focusWidth);
        })
    }
    // 把ol里面的第一个小li设置类名为 current
    ol.children[0].className = 'current';
    // 6. 克隆第一张图片(li)放到ul 最后面
    var first = ul.children[0].cloneNode(true);
    ul.appendChild(first);
    // 7. 点击右侧按钮， 图片滚动一张
    var num = 0;
    // circle 控制小圆圈的播放
    var circle = 0;
    // flag 节流阀
    var flag = true;
    arrow_r.addEventListener('click', function() {
        if (flag) {
            flag = false; // 关闭节流阀
            // 如果走到了最后复制的一张图片，此时 我们的ul 要快速复原 left 改为 0
            if (num == ul.children.length - 1) {
                ul.style.left = 0;
                num = 0;
            }
            num++;
            animate(ul, -num * focusWidth, function() {
                flag = true; // 打开节流阀
            });
            // 8. 点击右侧按钮，小圆圈跟随一起变化 可以再声明一个变量控制小圆圈的播放
            circle++;
            // 如果circle == 4 说明走到最后我们克隆的这张图片了 我们就复原
            if (circle == ol.children.length) {
                circle = 0;
            }
            // 调用函数
            circleChange();
        }
    });

    // 9. 左侧按钮做法
    arrow_l.addEventListener('click', function() {
        if (flag) {
            flag = false;
            if (num == 0) {
                num = ul.children.length - 1;
                ul.style.left = -num * focusWidth + 'px';

            }
            num--;
            animate(ul, -num * focusWidth, function() {
                flag = true;
            });
            // 点击左侧按钮，小圆圈跟随一起变化 可以再声明一个变量控制小圆圈的播放
            circle--;
            // 如果circle < 0  说明第一张图片，则小圆圈要改为第4个小圆圈（3）
            // if (circle < 0) {
            //     circle = ol.children.length - 1;
            // }
            circle = circle < 0 ? ol.children.length - 1 : circle;
            // 调用函数
            circleChange();
        }
    });

    function circleChange() {
        // 先清除其余小圆圈的current类名
        for (var i = 0; i < ol.children.length; i++) {
            ol.children[i].className = '';
        }
        // 留下当前的小圆圈的current类名
        ol.children[circle].className = 'current';
    }
    // 10. 自动播放轮播图
    var timer = setInterval(function() {
        //手动调用点击事件
        arrow_r.click();
    }, 2000);

})
```

### 返回顶部

1. 带有动画的返回顶部
2. 此时可以继续使用我们封装的动画函数
3. 只需要把所有的left 相关的值改为 跟 页面垂直滚动距离相关就可以了
4. 页面滚动了多少，可以通过 window.pageYOffset 得到
5. 最后是页面滚动，使用 window.scroll(x,y) 

```
  //1. 获取元素
        var sliderbar = document.querySelector('.slider-bar');
        var banner = document.querySelector('.banner');
        // banner.offestTop 就是被卷去头部的大小 一定要写到滚动的外面
        var bannerTop = banner.offsetTop
            // 当我们侧边栏固定定位之后应该变化的数值
        var sliderbarTop = sliderbar.offsetTop - bannerTop;
        // 获取main 主体元素
        var main = document.querySelector('.main');
        var goBack = document.querySelector('.goBack');
        var mainTop = main.offsetTop;
        // 2. 页面滚动事件 scroll
        document.addEventListener('scroll', function() {
                // console.log(11);
                // window.pageYOffset 页面被卷去的头部
                // console.log(window.pageYOffset);
                // 3 .当我们页面被卷去的头部大于等于了 172 此时 侧边栏就要改为固定定位
                if (window.pageYOffset >= bannerTop) {
                    sliderbar.style.position = 'fixed';
                    sliderbar.style.top = sliderbarTop + 'px';
                } else {
                    sliderbar.style.position = 'absolute';
                    sliderbar.style.top = '300px';
                }
                // 4. 当我们页面滚动到main盒子，就显示 goback模块
                if (window.pageYOffset >= mainTop) {
                    goBack.style.display = 'block';
                } else {
                    goBack.style.display = 'none';
                }

            })
            // 3. 当我们点击了返回顶部模块，就让窗口滚动的页面的最上方
        goBack.addEventListener('click', function() {
            // 里面的x和y 不跟单位的 直接写数字即可
            // window.scroll(0, 0);
            // 因为是窗口滚动 所以对象是window
            animate(window, 0);
        });
```

### 筋头云案例

1. 利用动画函数做动画效果
2. 原先筋斗云的起始位置是0
3. 鼠标经过某个小li，把当前小li的offsetLeft 位置做为目标值即可
4. 鼠标离开某个小li，就把目标值设为 0
5. 如果点击了某个小li， 就把li当前的位置存储起来，做为筋斗云的起始位置

```
 window.addEventListener('load', function() {
            // 1. 获取元素
            var cloud = document.querySelector('.cloud');
            var c_nav = document.querySelector('.c-nav');
            var lis = c_nav.querySelectorAll('li');
            // 2. 给所有的小li绑定事件 
            // 这个current 做为筋斗云的起始位置
            var current = 0;
            for (var i = 0; i < lis.length; i++) {
                // (1) 鼠标经过把当前小li 的位置做为目标值
                lis[i].addEventListener('mouseenter', function() {
                    animate(cloud, this.offsetLeft);
                });
                // (2) 鼠标离开就回到起始的位置 
                lis[i].addEventListener('mouseleave', function() {
                    animate(cloud, current);
                });
                // (3) 当我们鼠标点击，就把当前位置做为目标值
                lis[i].addEventListener('click', function() {
                    current = this.offsetLeft;
                });
            }
        })
```

## 移动端网页特效

### 触屏事件

![image-20211006211238576](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211238576.png)

### 触摸事件对象

![image-20211006211342930](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006211342930.png)

**因为平时我们都是给元素注册触摸事件，所以重点记住 targetTocuhes**

### 拖动元素

拖动元素三步曲：

（1） 触摸元素 touchstart： 获取手指初始坐标，同时获得盒子原来的位置

（2） 移动手指 touchmove： 计算手指的滑动距离，并且移动盒子

（3） 离开手指 touchend:

**注意： 手指移动也会触发滚动屏幕所以这里要阻止默认的屏幕滚动 e.preventDefault();**

### classList 属性

classList属性是HTML5新增的一个属性，返回元素的类名。但是ie10以上版本支持。

该属性用于在元素中添加，移除及切换 CSS 类。有以下方法

**获取元素类名：**

element.classList [ 索引号 ]；

```javascript
focus.classList[ 索引号 ];
```

**添加类：**

element.classList.add（’类名’）；

```javascript
focus.classList.add('current');
```

**移除类：**

element.classList.remove（’类名’）;

```javascript
focus.classList.remove('current');
```

**切换类：**

element.classList.toggle（’类名’）;

```javascript
focus.classList.toggle('current');
```

`注意:以上方法里面，所有类名都不带点`

### click 延时解决方案（常用第三种方法）

移动端 click 事件会有 300ms 的延时，原因是移动端屏幕双击会缩放(double tap to zoom) 页面。

解决方案：

​	1. 禁用缩放。 浏览器禁用默认的双击缩放行为并且去掉300ms 的点击延迟。

```html
  <meta name="viewport" content="user-scalable=no">
```

​	2.利用touch事件自己封装这个事件解决300ms 延迟。 

​	原理就是：

​		1、当我们手指触摸屏幕，记录当前触摸时间

​		2、当我们手指离开屏幕， 用离开的时间减去触摸的时间

​		3、如果时间小于150ms，并且没有滑动过屏幕， 那么我们就定义为点击

代码如下:

```javascript
//封装tap，解决click 300ms 延时
function tap (obj, callback) {
        var isMove = false;
        var startTime = 0; // 记录触摸时候的时间变量
        obj.addEventListener('touchstart', function (e) {
            startTime = Date.now(); // 记录触摸时间
        });
        obj.addEventListener('touchmove', function (e) {
            isMove = true;  // 看看是否有滑动，有滑动算拖拽，不算点击
        });
        obj.addEventListener('touchend', function (e) {
            if (!isMove && (Date.now() - startTime) < 150) {  // 如果手指触摸和离开时间小于150ms 算点击
                callback && callback(); // 执行回调函数
            }
            isMove = false;  //  取反 重置
            startTime = 0;
        });
}
//调用  
  tap(div, function(){   // 执行代码  });

```

3. 使用插件。fastclick 插件解决300ms 延迟。

   GitHub官网地址： [https://](https://github.com/ftlabs/fastclick)[github.com/ftlabs/fastclick](https://github.com/ftlabs/fastclick)

   插件的使用：

   1. 引入 js 插件文件。

   2. 按照规定语法使用。

   3. fastclick 插件解决 300ms 延迟。 使用延时

      ```javascript
      if ('addEventListener' in document) {
                  document.addEventListener('DOMContentLoaded', function() {
                             FastClick.attach(document.body);
                  }, false);
      }
      ```


![image-20211007103251254](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103251254.png)

## 本地存储

### 本地存储特性

1、数据存储在用户浏览器中

2、设置、读取方便、甚至页面刷新不丢失数据

3、容量较大，sessionStorage约5M、localStorage约20M

4、只能存储字符串，可以将对象JSON.stringify() 编码后存储

5、获取是要是对象形式： JSON.parse()



###  window.sessionStorage

1、生命周期为关闭浏览器窗口

2、在同一个窗口(页面)下数据可以共享

3、以键值对的形式存储使用

存储数据：

```javascript
sessionStorage.setItem('key', value)
```

获取数据：

```javascript
sessionStorage.getItem('key')
```

删除数据：

```javascript
sessionStorage.removeItem('key')
```

清空数据：(所有都清除掉)

```javascript
sessionStorage.clear()
```

### window.localStorage

1、声明周期永久生效，除非手动删除 否则关闭页面也会存在

2、可以多窗口（页面）共享（同一浏览器可以共享）

3.  以键值对的形式存储使用

存储数据：

```javascript
localStorage.setItem('key', value)
```

获取数据：

```javascript
localStorage.getItem('key')
```

删除数据：

```javascript
localStorage.removeItem('key')
```

清空数据：(所有都清除掉)

```javascript
localStorage.clear()
```

------

# jQuery

------

官网地址： https://jquery.com/

步骤：

- 引入jQuery文件。
- 在文档最末尾插入 script 标签，书写体验代码。
- $('div').hide() 可以隐藏盒子。

## jQuery 插件

1.  jQuery 插件库  http://www.jq22.com/     
2.  jQuery 之家   http://www.htmleaf.com/ 
3.  全屏滚动插件  http://www.dowebok.com/demo/2014/77/

## 入口函数

相当于原生 js 中的 DOMContentLoaded。

```
// 第一种: 简单易用。
$(function () {   
    ...  // 此处是页面 DOM 加载完成的入口
}) ; 

// 第二种: 繁琐，但是也可以实现
$(document).ready(function(){
   ...  //  此处是页面DOM加载完成的入口
});
```

##  jQuery 对象和 DOM 对象转换

jQuery 对象本质是： 利用$对DOM 对象包装后产生的对象（伪数组形式存储）。

```
// 1.DOM对象转换成jQuery对象，方法只有一种
var box = document.getElementById('box');  // 获取DOM对象
var jQueryObject = $(box);  // 把DOM对象转换为 jQuery 对象

// 2.jQuery 对象转换为 DOM 对象有两种方法：
//   2.1 jQuery对象[索引值]
var domObject1 = $('div')[0]

//   2.2 jQuery对象.get(索引值)
var domObject2 = $('div').get(0)
```

## jQuery 选择器

### 基础选择器

```
$("选择器")   //  里面选择器直接写 CSS 选择器即可，但是要加引号 
```

![image-20211006203752658](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203752658.png)

### 层级选择器

![image-20211006203805309](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203805309.png)

### 筛选选择器

![image-20211006203819746](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203819746.png)

## 查元素

![image-20211006203837102](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203837102.png)

## 排他思想

```
// 想要多选一的效果，排他思想：当前元素设置样式，其余的兄弟元素清除样式。
$(this).css(“color”,”red”);
$(this).siblings(). css(“color”,””);
```

## 链式编程

```
// 链式编程是为了节省代码量，看起来更优雅。
$(this).css('color', 'red').sibling().css('color', ''); 
```

## 样式操作

### 操作 css 方法

```
// 1.参数只写属性名，则是返回属性值
var strColor = $(this).css('color');

// 2.  参数是属性名，属性值，逗号分隔，是设置一组样式，属性必须加引号，值如果是数字可以不用跟单位和引号
$(this).css(''color'', ''red'');

// 3.  参数可以是对象形式，方便设置多组样式。属性名和属性值用冒号隔开， 属性可以不用加引号
$(this).css({ "color":"white","font-size":"20px"});

```

### 设置类样式方法

removeClass

```
// 1.添加类
$("div").addClass("current");

// 2.删除类
$("div").removeClass("current");

// 3.切换类
$("div").toggleClass("current");

```

## jQuery 效果

###  显示隐藏

show

hide

显示隐藏动画，常见有三个方法：show() / hide() / toggle() ;

![image-20211006203853340](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203853340.png)

![image-20211006203904934](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203904934.png)

![image-20211006203913400](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203913400.png)

### 滑入滑出

滑入滑出动画，常见有三个方法：slideDown() / slideUp() / slideToggle() ; 

![image-20211006203940696](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203940696.png)

![image-20211006203947997](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203947997.png)

![image-20211006203955009](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006203955009.png)

### 淡入淡出

淡入淡出动画，常见有四个方法：fadeIn() / fadeOut() / fadeToggle() / fadeTo() ; 

![image-20211006204012818](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204012818.png)

![image-20211006204020229](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204020229.png)

![image-20211006204031752](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204031752.png)

![image-20211006204119223](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204119223.png)

### 自定义动画

animate

![image-20211006204130772](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204130772.png)

### 停止动画排队

动画或者效果一旦触发就会执行，如果多次触发，就造成多个动画或者效果排队执行。

​	停止动画排队的方法为：stop() ; 

- stop() 方法用于停止动画或效果。
- stop() 写到动画或者效果的前面， 相当于停止结束上一次的动画。

​        总结: 每次使用动画之前，先调用 stop() ,在调用动画。

### 事件切换

jQuery中为我们添加了一个新事件 hover() ; 功能类似 css 中的伪类 :hover 。介绍如下

**语法**

```javascript
hover([over,]out)     // 其中over和out为两个函数
```

- over:鼠标移到元素上要触发的函数（相当于mouseenter）
- out:鼠标移出元素要触发的函数（相当于mouseleave）
- 如果只写一个函数，则鼠标经过和离开都会触发它

## jQuery 属性操作

### 元素固有属性值

![image-20211006204224544](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204224544.png)

​	注意：prop() 除了普通属性操作，更适合操作表单属性：disabled / checked / selected 等。

### 元素自定义属性值 

![image-20211006204233277](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204233277.png)

注意：attr() 除了普通属性操作，更适合操作自定义属性。（该方法也可以获取 H5 自定义属性）

### 数据缓存

![image-20211006204242526](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204242526.png)

注意：同时，还可以读取 HTML5 自定义属性  data-index ，得到的是数字型。

## jQuery 文本属性值

​	jQuery的文本属性值常见操作有三种：html() / text() / val() ; 分别对应JS中的 innerHTML 、innerText 和 value 属性。

（）为空为赋值；填写内容是为修改

```
 		//1. 获取设置元素内容 html()
       $("div").html();
        
        // 2. 获取设置元素文本内容 text()
       $("div").text();
       
        // 3. 获取设置表单值 val()
       $("input").val();
      
```

##  jQuery 元素操作

### 遍历元素each

![image-20211006204304670](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204304670.png)

​	注意：此方法用于遍历 jQuery 对象中的每一项，回调函数中元素为 DOM 对象，想要使用 jQuery 方法需要转换。

![image-20211006204312675](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204312675.png)

​	注意：此方法用于遍历 jQuery 对象中的每一项，回调函数中元素为 DOM 对象，想要使用 jQuery 方法需要转换。

### 创建元素

![image-20211006204332407](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204332407.png)

### 添加元素

append

after

before

![image-20211006204347701](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204347701.png)

![image-20211006204356648](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204356648.png)

### 删除元素

remove

empty

![image-20211006204408343](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204408343.png)

注意：以上只是元素的创建、添加、删除方法的常用方法，其他方法请参详API。

##  jQuery 尺寸、位置操作

###  jQuery 尺寸操作

width

![image-20211006204433326](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204433326.png)

### jQuery 位置操作

offset

position

scroll

![image-20211006204449113](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204449113.png)

![image-20211006204458776](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204458776.png)

![image-20211006204505770](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204505770.png)

## jQuery 事件处理

### 事件注册

单个事件注册:

```
element.事件(function() {});
```

多个事件注册:

```
element.on({
	事件1： function() {},
	事件2： function() {}
})

//当事件处理相同时，可以简写：
	element.on("事件1，事件2",function() {});
```

### 事件解绑

![image-20211006204558097](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204558097.png)

### 自动触发事件

![image-20211006204613883](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204613883.png)

![image-20211006204622444](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204622444.png)

### 事件委托

// click 是绑定在ul 身上的，但是 触发的对象是 ul 里面的小li

```
 			$("ul").on("click", "li", function() {
                alert(11);
            });
```

### 给未来动态创建的元素绑定事件

```
 			$("ol").on("click", "li", function() {
                alert(11);
            })
            var li = $("<li>我是后来创建的</li>");
            $("ol").append(li);
```

## jQuery 事件对象

![image-20211006204637867](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204637867.png)

注意：jQuery中的 event 对象使用，可以借鉴 API 和 DOM 中的 event 。

##  jQuery 拷贝对象

![image-20211006204647038](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204647038.png)

## jQuery 多库共存

![image-20211006204658067](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006204658067.png)

```
<script>
	$(function() {
  		// 让jquery 释放对$ 控制权 让用自己决定
  		var suibian = jQuery.noConflict();
  		console.log(suibian("span"));
	})
</script>
```

------

# Echarts

------

ECharts，一个使用 JavaScript 实现的开源可视化库，可以流畅的运行在 PC 和移动设备上，兼容当前绝大部分浏览器（IE8/9/10/11，Chrome，Firefox，Safari等），底层依赖矢量图形库 [ZRender](https://github.com/ecomfe/zrender)，提供直观，交互丰富，可高度个性化定制的数据可视化图表。

官网：**https://www.echartsjs.com/zh/tutorial.html**

## 使用步骤：

- 下载echarts  https://github.com/apache/incubator-echarts/tree/4.5.0  
- 引入echarts  `dist/echarts.min.js`
- 准备一个具备大小的DOM容器

```html
<div id="main" style="width: 600px;height:400px;"></div>
```

- ###### 初始化echarts实例对象

```js
var myChart = echarts.init(document.getElementById('main'));
```

- 指定配置项和数据(option)

```js
var option = {
    xAxis: {
        type: 'category',
        data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
    },
    yAxis: {
        type: 'value'
    },
    series: [{
        data: [820, 932, 901, 934, 1290, 1330, 1320],
        type: 'line'
    }]
};
```

- 将配置项设置给echarts实例对象

```js
myChart.setOption(option);
```

## 基础配置

- series

  ​	通过type：选择类型；data:[ ]写数据

  ```
  bar  柱状图
  line  折线/面积图
  pie  饼图
  ```

  - 系列列表。每个系列通过 `type` 决定自己的图表类型
  - 大白话：图标数据，指定什么类型的图标，可以多个图表重叠。

- xAxis：直角坐标系 grid 中的 x 轴

  -  boundaryGap: 坐标轴两边留白策略 true，这时候刻度只是作为分隔线，标签和数据点都会在两个刻度之间的带(band)中间。

- yAxis：直角坐标系 grid 中的 y **轴**

- grid：直角坐标系内绘图网格。 

  - //containLabel 区域是否包含坐标轴的刻度标签。

- title：标题组件

- tooltip：提示框组件（提示）

- legend：图例组件（有多组数据时进行筛选，series中药有name属性）

- color：调色盘颜色列表

  数据堆叠，同个类目轴上系列配置相同的`stack`值后 后一个系列的值会在前一个系列的值上相加。
  
  ```
  var option = {
              color: ['pink', 'blue', 'green', 'skyblue', 'red'],
              title: {
                  text: '我的折线图'
              },
              tooltip: {
                  trigger: 'axis'
              },
              legend: {
                  data: ['直播营销', '联盟广告', '视频广告', '直接访问']
              },
              grid: {
                  left: '3%',
                  right: '3%',
                  bottom: '3%',
                  // 当刻度标签溢出的时候，grid 区域是否包含坐标轴的刻度标签。如果为true，则显示刻度标签
                  // 如果left right等设置为 0% 刻度标签就溢出了，此时决定是否显示刻度标签
                  //containLabel 区域是否包含坐标轴的刻度标签。
                  containLabel: true
              },
              toolbox: {
                  feature: {
                      saveAsImage: {}
                  }
              },
              xAxis: {
                  type: 'category',
                  // 坐标轴两边留白策略 true，这时候刻度只是作为分隔线，标签和数据点都会在两个刻度之间的带(band)中间。
                  boundaryGap: false,
                  data: ['星期一', '星期二', '周三', '周四', '周五', '周六', '周日']
              },
              yAxis: {
                  type: 'value'
              },
              series: [
                  {
                      name: '直播营销',
                      // 图表类型是线形图
                      type: 'line',
                      data: [120, 132, 101, 134, 90, 230, 210]
                  },
                  {
                      name: '联盟广告',
                      type: 'line',
  
                      data: [220, 182, 191, 234, 290, 330, 310]
                  },
                  {
                      name: '视频广告',
                      type: 'line',
  
                      data: [150, 232, 201, 154, 190, 330, 410]
                  },
                  {
                      name: '直接访问',
                      type: 'line',
  
                      data: [320, 332, 301, 334, 390, 330, 320]
                  }
              ]
          };
  ```
  
  

## 适配方案

flexible.js  +   rem  +  flex布局

基准 = （效果图大小 / 划分份数）       //相当于html大小

## 边框图片

![image-20211007103327666](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103327666.png)

组合写法：

```css
border-image: url("images/border.jpg") 167/20px round;
```

拆分写法：

```css
1、路径
border-image-source: url("images/border.jpg");

2、裁剪尺寸（上，右，下，左）
border-image-slice: 167 167 167 167;

3、图片边框的宽度
border-image-width: 20px;

4、平铺repeat  铺满round(常用)  拉伸stretch(默认)
border-image-repeat: round;
```

解释：

- 边框图片资源地址
- 裁剪尺寸（上 右 下 左）单位默认px，可使用百分百。
- 边框图片的宽度，默认边框的宽度。
- 平铺方式：
  - stretch 拉伸（默认）
  - repeat 平铺，从边框的中心向两侧开始平铺，会出现不完整的图片。
  - round 环绕，是完整的使用切割后的图片进行平铺。

## 公用面板样式

![image-20211007103340226](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103340226.png)

------

------

# Ajax

------

### Ajax简介

1、全称为 Asynchronous JavaScript And XML，就是异步的 JS 和 XML。 

2、通过 AJAX 可以在浏览器中向服务器发送异步请求，最大的优势：无刷新获取数据。 

3、AJAX 不是新的编程语言，而是一种将现有的标准组合在一起使用的新方式。

4、默认同源发请求

#### 优点：

1、可以无需刷新页面而与服务器端进行通信。 

2、允许你根据用户事件来更新部分页面内容。

#### 缺点：

1、没有浏览历史，不能回退 。

2、存在跨域问题(同源) 。

3、SEO 不友好 。

#### 典型应用场景

1、页面上拉加载更多数据
		2、列表数据无刷新分页
		3、表单项离开焦点数据验证
		4、搜索框提示文字下拉列表

### Ajax的使用

1、创建 AJAX  (XMLHttpRequest) 对象

```js
var xhr = new XMLHttpRequest();
```

2、初始化 设置请求方法和 url

```js
xhr.open('method', 'url');

//可以设置请求头，一般不设
xhr.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded')
```

3、发送请求

```js
//get 请求不传 body 参数，只有 post 请求使用
xhr.send(body) 
```

4、 接收响应 

```js
1：
xhr.onload = function (){
			console.log(xhr.responseText)
		}
		

2:常用
//xhr.responseXML 接收 xml 格式的响应数据 
//xhr.responseText 接收文本格式的响应数据 
//当 Ajax 状态码发生变化时将自动触发该事件。

xhr.onreadystatechange = function (){ 
	if(xhr.readyState == 4 && xhr.status == 200){ 
		var text = xhr.responseText; console.log(text); 
	} else{
	// console.log(xhr.status);//状态码
	// console.log(xhr.statusText);//状态字符串
	// console.log(xhr.getAllResponseHeaders());//所有响应头
	// console.log(xhr.response);//响应体
	//设置 result 的文本
    result.innerHTML = xhr.response;
    }
}
```

------

### **AJAX** 请求状态

#### 1、状态码

| **值** | **状态**         | **描述**                                            |
| ------ | ---------------- | --------------------------------------------------- |
| 0      | UNSENT           | XMLHttpRequest 对象已被创建，但尚未调用 open方法。  |
| 1      | OPENED           | open() 方法已经被调用。                             |
| 2      | HEADERS_RECEIVED | send() 方法已经被调用，响应头也已经被接收。         |
| 3      | LOADING          | 数据接收中，此时 response 属性中已经包含部分数据。  |
| 4      | DONE             | Ajax 请求完成，这意味着数据传输已经彻底完成或失败。 |

#### 2、获取Ajax状态码

```
xhr.readyState
```

#### 3、当状态码发生改变时触发

```js
//需要放到xhr.send的前面
xhr.onreadystatechange = function() {
	 // 判断当Ajax状态码为4时
     if (xhr.readyState == 4) {
         // 获取服务器端的响应数据
         console.log(xhr.responseText);
     }

}
```

------

### URL编码与解码

​	URL 地址中，只允许出现英文相关的字母、标点符号、数字，因此，在 URL 地址中不允许出现中文字符。如果 URL 中需要包含中文这样的字符，则必须对中文字符进行编码（转义）。
​	URL编码的原则：使用安全的字符（没有特殊用途或者特殊意义的可打印字符）去表示那些不安全的字符。
URL编码原则的通俗理解：使用英文字符去表示非英文字符。



浏览器提供了 URL 编码与解码的 API，分别是：
			encodeURI()  编码的函数
			decodeURI()  解码的函数

```js
encodeURI('黑马程序员')
// 输出字符串  %E9%BB%91%E9%A9%AC%E7%A8%8B%E5%BA%8F%E5%91%98
decodeURI('%E9%BB%91%E9%A9%AC')
// 输出字符串  黑马
```

### 请求参数传递

查询字符串

格式：将英文的 ? 放在URL 的末尾，然后再加上 参数＝值 ，想加上多个参数的话，使用 & 符号进行分隔。以这个形式，可以将想要发送给服务器的数据添加到 URL 中

```
// 不带参数的 URL 地址
http://www.liulongbin.top:3006/api/getbooks
// 带一个参数的 URL 地址
http://www.liulongbin.top:3006/api/getbooks?id=1
// 带两个参数的 URL 地址
http://www.liulongbin.top:3006/api/getbooks?id=1&bookname=西游记
```

#### 1、get请求方式

```js
// 配置ajax对象
xhr.open('get', 'http://localhost:3000/get?'+params)
// 发送请求
xhr.send();

		// 获取姓名文本框
        var username = document.getElementById('username');
        // 获取年龄文本框
        var age = document.getElementById('age');
        // 获取用户在文本框中输入的值
        var nameValue = username.value;
        var ageValue = age.value;
		// 拼接请求参数
		var params = 'username='+ nameValue +'&age=' + ageValue;
```

简单写法：

```
xhr.open('GET', 'http://www.liulongbin.top:3006/api/getbooks?id=1')
```

#### 2、post请求方式

```js
// 配置ajax对象
xhr.open('post', 'http://localhost:3000/post');
// 设置请求头的类型（post请求必须要设置）
xhr.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded') 
// 发送请求
xhr.send(params);

            // 获取姓名文本框
            var username = document.getElementById('username');
            // 获取年龄文本框
            var age = document.getElementById('age');
            // 获取用户在文本框中输入的值
            var nameValue = username.value;
            var ageValue = age.value;
            // 拼接请求参数
            var params = 'username='+ nameValue +'&age=' + ageValue;

```

简单写法：

```
// 3. 设置 Content-Type 属性
      xhr.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded')
// 4. 调用 send 函数
      xhr.send('bookname=水浒传&author=施耐庵&publisher=上海图书出版社')
```

#### 3、数据格式

##### 1、响应数据格式

在 http 请求与响应的过程中，无论是请求参数还是响应内容，如果是对象类型，最终都会被转换为**对象字符串进行传输**。

```
 // 将 json 字符串转换为json对象,把字符串转换为数据对象的过程，叫做反序列化
JSON.parse()

// 将json对象转换为json字符串,把数据对象转换为字符串的过程，叫做序列化
JSON.stringify()

			//当设置了响应体数据的类型，则不需要手动转换了
            xhr.responseType = 'json';
```

##### 2、请求数据格式（  请求头类型（Conent-Type））

类型: 

​	1、application/x-www-form-urlencoded

​		`name=zhangsan&age=20&sex=男`

​				解析：app.use(bodyParser.urlencoded())

​	2、application/json

​	对象结构：key 必须是使用英文的双引号包裹的字符串，value 的数据类型可以是数字、字符串、布尔值、null、数组、对象6种类型

​		`{"name": "zhangsan", "age": "20", "sex": "男"}`

​	数组结构：数组结构在 JSON 中表示为 [ ] 括起来的内容。数据结构为 [ "java", "javascript", 30, true … ] 。数组中数据的类型可以是数字、字符串、布尔值、null、数组、对象6种类型。

```
[ "java", "python", "php" ]
[ 100, 200, 300.5 ]
[ true, false, null ]
[ { "name": "zs", "age": 20}, { "name": "ls", "age": 30} ]
[ [ "苹果", "榴莲", "椰子" ], [ 4, 50, 5 ] ]
```

​				解析：app.use(bodyParser.json())

*在请求头中指定 Content-Type 属性的值是 application/json，告诉服务器端当前请求参数的格式是 json。*

<!--注意：get 请求是不能提交 json 对象数据格式的，传统网站的表单提交也是不支持 json 对象数据格式的。-->

------

### Ajax 错误处理

#### **解决** **IE** 缓存问题

问题：

​		在一些浏览器中(IE),由于缓存机制的存在，ajax 只会发送的第一次请求，剩 余多次请求不会在发送给浏览器而是直接加载缓存中的数据。 

解决方式：

​		浏览器的缓存是根据 url 地址来记录的，所以我们只需要修改 url 地址 即可避免缓存问题 

```
xhr.open("get","'http://localhost:3000/cache?t=" + Date.now()); 
或者
xhr.open('get', 'http://localhost:3000/cache?t=' + Math.random()); 
```

#### 网络错误处理

```
1、网络畅通，服务器端能接收到请求，服务器端返回的结果不是预期结果。
     		可以判断服务器端返回的状态码，分别进行处理。xhr.status 获取http状态码

2、网络畅通，服务器端没有接收到请求，返回404状态码。
			检查请求地址是否错误。
			
3、网络畅通，服务器端能接收到请求，服务器端返回500状态码。
			服务器端错误，找后端程序员进行沟通。

4、网络超时。
			 xhr.ontimeout = function(){
                alert("网络异常, 请稍后重试!!");
            }
			
5、网络中断，请求无法发送到服务器端。
			会触发xhr对象下面的onerror事件，在onerror事件处理函数中对错误进行处理。
			xhr.onerror = function(){
                alert("你的网络似乎出了一些问题!");
            }
```

#### 取消请求

```
 //获取元素对象
        const btns = document.querySelectorAll('button');
 // abort
        btns[1].onclick = function(){
            x.abort();
        }
```

#### 重复请求问题

```
//获取元素对象
const btns = document.querySelectorAll('button');
let x = null;
//标识变量
	// 是否正在发送AJAX请求
let isSending = false; 

btns[0].onclick = function(){
	//判断标识变量
		// 如果正在发送, 则取消该请求, 创建一个新的请求
    if(isSending) x.abort();
    x = new XMLHttpRequest();
    //修改 标识变量的值
    isSending = true;
    x.open("GET",'http://127.0.0.1:8000/delay');
    x.send();
    x.onreadystatechange = function(){
    	if(x.readyState === 4){
       		//修改标识变量
       		isSending = false;
     	}
    }
}

// abort
btns[1].onclick = function(){
   x.abort();
}
```



------

### 封装Ajax

调用：

```
ajax({
	type: 'post',
	// 请求地址
	url: 'http://localhost:3000/responseData',
	success: function (data) {
		console.log('这里是success函数');
		console.log(data)
	}
})

请求参数位置的问题
	将请求参数传递到ajax函数内部, 在函数内部根据请求方式的不同将请求参数放置在不同的位置
	get 放在请求地址的后面
	post 放在send方法中
```

封装：

```
function ajax (options) {
	// 默认值
	var defaults = {
		type: 'get',
		url: '',
		data: {},
		header: {
			'Content-Type': 'application/x-www-form-urlencoded'
		},
		success: function () {},
		error: function () {}
	}
	// 使用用户传递的参数替换默认值参数
	Object.assign(defaults, options);
	// 创建ajax对象
	var xhr = new XMLHttpRequest();
	// 参数拼接变量
	var params = '';
	// 循环参数
	for (var attr in defaults.data) {
		// 参数拼接
		params += attr + '=' + defaults.data[attr] + '&';
		// 去掉参数中最后一个&
		params = params.substr(0, params.length-1)
	}
	// 如果请求方式为get
	if (defaults.type == 'get') {
		// 将参数拼接在url地址的后面
		defaults.url += '?' + params;
	}

	// 配置ajax请求
	xhr.open(defaults.type, defaults.url);
	// 如果请求方式为post
	if (defaults.type == 'post') {
		// 设置请求头
		xhr.setRequestHeader('Content-Type', defaults.header['Content-Type']);
		// 如果想服务器端传递的参数类型为json
		if (defaults.header['Content-Type'] == 'application/json') {
			// 将json对象转换为json字符串
			xhr.send(JSON.stringify(defaults.data))
		}else {
			// 发送请求
			xhr.send(params);
		}
	} else {
		xhr.send();
	}
	// 请求加载完成
	xhr.onload = function () {
		// 获取服务器端返回数据的类型
		var contentType = xhr.getResponseHeader('content-type');
		// 获取服务器端返回的响应数据
		var responseText = xhr.responseText;
		// 如果服务器端返回的数据是json数据类型
		if (contentType.includes('application/json')) {
			// 将json字符串转换为json对象
			responseText = JSON.parse(responseText);
		}
		// 如果请求成功
		if (xhr.status == 200) {
			// 调用成功回调函数, 并且将服务器端返回的结果传递给成功回调函数
			defaults.success(responseText, xhr);
		} else {
			// 调用失败回调函数并且将xhr对象传递给回调函数
			defaults.error(responseText, xhr);
		} 
	}
	// 当网络中断时
	xhr.onerror = function () {
		// 调用失败回调函数并且将xhr对象传递给回调函数
		defaults.error(xhr);
	}
}
```

### 模板引擎

作用：使用模板引擎提供的模板语法，可以将数据和 HTML 拼接起来。

官方地址： https://aui.github.io/art-template/zh-cn/index.html

#### 使用步骤

```
1、下载 art-template 模板引擎库文件并在 HTML 页面中引入库文件
<script src="./js/template-web.js"></script>

2、准备 art-template 模板
<script id="tpl" type="text/html">
     <div class="box"></div>
 </script>
 
 3、告诉模板引擎将哪一个模板和哪个数据进行拼接（数据是对象的形式）
var html = template('tpl', {username: 'zhangsan', age: '20'});

4、将拼接好的html字符串添加到页面中document.getElementById('container').innerHTML = html;

5、通过模板语法告诉模板引擎，数据和html字符串要如何拼接
<script id="tpl" type="text/html">
     <div class="box"> {{ username }} </div>
 </script>
```

#### 输出：

​	数据可为：属性名，运算， 三元表达式。。。

```
{{value}}
{{data.key}}
{{data['key']}}
{{a ? b : c}}
{{a || b}}
{{a + b}}
```

​	注意点：如果内含标签，需要解析 

```
{{@ 数据}}
```

#### 条件判断：

```html
1、{{if 条件}}... {{/if}}
2、{{if 条件}}... {{else}}... {{/if}}
3、{{if 条件}}... {{else if 条件}}... {{/if}}
```

#### 循环：

```html
{{each 数据}}
	{{$index}}   //当前循环索引
	{{$value}}   //当前循环数据
{{/each}}
```

#### 过滤器:

​	要写再template函数渲染之前

​	注册过滤器时一定要有return

```
1、注册
template.defaults.imports.dateFormat = function(date, format){/*[code..]*/};
template.defaults.imports.timestamp = function(value){return value * 1000};

过滤器函数第一个参数接受目标值。

2、使用
{{date | timestamp | dateFormat 'yyyy-MM-dd hh:mm:ss'}}
```

#### 模板引擎的实现原理

##### 1、exec(）

​	函数用于检索字符串中的正则表达式的匹配。如果字符串中有匹配的值，则返回该匹配值，否则返回 null。



```
RegExpObject（正则规则）.exec(string)
```

示例

```
1、
var str = 'hello'
var pattern = /o/
// 输出的结果["o", index: 4, input: "hello", groups: undefined]
console.log(pattern.exec(str)) 

2、正则表达式中 ( ) 包起来的内容表示一个分组，可以通过分组来提取自己想要的内容
	  var obj = {
        name: '杨明'
      }

      var str = '我的名字是{{name}}'
      var reg = /{{(\w+)}}/
      //2、1------------------------------------
      var arr = reg.exec(str)
      console.log(arr)
      // ["{{name}}", "name", index: 7, input: "<div>我是{{name}}</div>", groups: undefined]
      
      str = str.replace(arr[0], obj[arr[1]])
      console.log(str)
      
      //2、2------------------------------------
      var arr
      while(arr = reg.exec(str)) {
      	str.replace(arr[0], obj[arr[1]])
      }
      console.log(str)
```

### 设置HTTP请求时限

- ***写于xhr.open之前***

有时，Ajax 操作很耗时，而且无法预知要花多少时间。如果网速很慢，用户可能要等很久。新版本的 XMLHttpRequest 对象，增加了 timeout 属性，可以设置 HTTP 请求的时限：

```
 xhr.timeout = 3000
```

上面的语句，将最长等待时间设为 3000 毫秒。过了这个时限，就自动停止HTTP请求。与之配套的还有一个 timeout 事件，用来指定回调函数：

```
xhr.ontimeout = function(event){
     alert('请求超时！')
 }
```

### FormData 对象

#### 作用

1、模拟HTML表单，相当于将HTML表单映射成表单对象，自动将表单对象中的数据拼接成请求参数的格式。

2、异步上传二进制文件

#### 基本使用步骤

```
1.   准备 HTML 表单 //要有name属性
<form id="form">
     <input type="text" name="username" />
     <input type="password" name="password" />
     <input type="button"/>
</form>

2.1. 新建 FormData 对象
var formData = new FormData();
2.2.   向表单对象中追加属性值
formData.append('key', 'value');

3. 创建 XHR 对象
var xhr = new XMLHttpRequest()
4. 指定请求类型与URL地址
xhr.open('POST', 'url')
5   提交表单对象
xhr.send(formData);

注意：
Formdata 对象不能用于 get 请求，因为对象需要被传递到 send 方法中，而 get 请求方式的请求参数只能放在请求地址的后面。
服务器端 bodyParser 模块不能解析 formData 对象表单数据，我们需要使用 formidable 模块进行解析。

```

#### 获取网页表单的值

```js
  <form id="form1">
    <input type="text" name="uname" autocomplete="off" />
    <input type="password" name="upwd" />
    <button type="submit">提交</button>
  </form>

  <script>
    // 1. 通过 DOM 操作，获取到 form 表单元素
    var form = document.querySelector('#form1')

    form.addEventListener('submit', function (e) {
      // 阻止表单的默认提交行为
      e.preventDefault()

      // 创建 FormData，快速获取到 form 表单中的数据
      var fd = new FormData(form)

      var xhr = new XMLHttpRequest()
      xhr.open('POST', 'http://www.liulongbin.top:3006/api/formdata')
      xhr.send(fd)

      xhr.onreadystatechange = function () {
        if (xhr.readyState === 4 && xhr.status === 200) {
          console.log(JSON.parse(xhr.responseText))
        }
      }
    })
  </script>
```

#### 实例方法

```
1.   获取表单对象中属性的值
formData.get('key');
 
2.   设置表单对象中属性的值
formData.set('key', 'value');

3.   删除表单对象中属性的值
formData.delete('key');

4.   向表单对象中追加属性值
formData.append('key', 'value');


注意：set 方法与 append 方法的区别是，在属性名已存在的情况下，set 会覆盖已有键名的值，append会保留两个值。
```

#### 二进制文件上传

```
<input type="file" id="file"/>

//获取元素
var file = document.getElementById('file')
// 当用户选择文件的时候
 file.onchange = function () {
     // 创建空表单对象
     var formData = new FormData();
     // 将用户选择的二进制文件追加到表单对象中
     formData.append('attrName', this.files[0]);
     // 创建ajax对象，配置ajax对象，请求方式必须为post
     var xhr = new XMLHttpRequest();
     xhr.open('post', 'www.example.com');
     xhr.send(formData);
 }
 
 
 
 //app.js文件
 app.post('/upload', (req, res) => {
 	//创建formidable表单解析对象
 	const form = new formidable.IncomingForm();
 	//设置客户端上传文件的存储路基
 	form.uploadDir = path.join(__dirname, 'public', 'uploads');
 	//保留上传稳健的后缀名字
 	form.keepExtensions = true;
 	//解析客户端传递的FormData对象
 	form.pares(req, (err, fields, files) => {
 		res.send('ok');
 	})
 })
```

#### 二进制文件上传进度提示

```
	 // 文件上传过程中持续触发onprogress事件
     xhr.upload.onprogress = function (ev) {
         // 当前上传文件大小(ev.loaded)/文件总大小(ev.total) 再将结果转换为百分数
         // 将结果赋值给进度条的宽度属性 
          var result = Math.ceil((e.loaded / e.total) * 100) + '%';
          bar.style.width = resule;
         //将百分比显示在进度条中
         bar.innerHTML = result;
     }
     
      // 文件上传完成触发onlload事件
      xhr.upload.onload = function () {
    	$('#percent').removeClass().addClass('progress-bar progress-bar-success')
      }
```

#### 使用jQuery实现文件上传

```
$('#btnUpload').on('click', function () {
          var files = $('#file1')[0].files
          if (files.length <= 0) {
            return alert('请选择文件后再上传！')
          }

          var fd = new FormData()
          fd.append('avatar', files[0])

          // 发起 jQuery 的 Ajax 请求，上传文件
          $.ajax({
            method: 'POST',
            url: 'http://www.liulongbin.top:3006/api/upload/avatar',
            data: fd,
            processData: false,//不要序列化
            contentType: false,//不设置请求头
            success: function (res) {
              console.log(res)
            }
          })
        })
```

#### jQuery实现loading效果

写于Ajax发起请求之前

```
<img src="./images/loading.gif" alt="" style="display: none" id="loading" />

		Ajax 请求开始时，执行 ajaxStart 函数。可以在 ajaxStart 的 callback 中显示 loading 效果
		
		// 监听到Ajax请求被发起了
        $(document).ajaxStart(function () {
          $('#loading').show()
        })
        
注意： $(document).ajaxStart() 函数会监听当前文档内所有的 Ajax 请求。

		Ajax 请求结束时，执行 ajaxStop 函数。可以在 ajaxStop 的 callback 中隐藏 loading 效果
		
		 // 监听到 Ajax 完成的事件
		 $(document).ajaxStop(function() {
     		$('#loading').hide()
 		 })
```

#### 文件上传图片即时预览

```
xhr.onload = function () {
	//将服务器返回的数据显示在控制台中
     var result = JSON.parse(xhr.responseText);
     //动态创建img标签
     var img = document.createElement('img');
     //给img设置src属性
     img.src = result.src;
     //当图片加载完成后的
     img.onload = function () {
     	//将图片显示在页面中
         document.body.appendChild(this);
     }
 }
```

------

### jQuery中的Ajax

#### 1、$.get()

```
$.get(url, [data], [callback], [type])url:请求的 URL 地址。 data:请求携带的参数。 callback:载入成功时回调函数。 type:设置返回内容格式，xml, html, script, json, text, _default。
```

#### 2、$.post()

```
$.post(url, [data], [callback], [type])url:请求的 URL 地址。 data:请求携带的参数。 callback:载入成功时回调函数。 type:设置返回内容格式，xml, html, script, json, text, _default。
```

#### 3、$.ajax()

```
$.ajax({
   // 请求的方式，例如 GET 或 POST
   type: '',    
   // 请求的 URL 地址
   url: '',    
   // 这次请求要携带的数据
   data: { },   
   contentType: 'application/x-www-form-urlencoded',
   beforeSend: function () { 
       return false
   },
   // 请求成功之后的回调函数
   success: function(res) { 
   		// response为服务器端返回的数据
		// 方法内部会自动将json字符串转换为json对象
		console.log(response);
   },
   // 请求失败以后函数被调用
   error: function (xhr) {
		console.log(xhr)
   },
   //超时时间
   timeout: 2000,
   //失败的回调
   error: function(){
     console.log('出错啦!!');
   },
   //头信息
   headers: {
     c:300,
     d:400
   }             
})

```

#### 4、$.ajax()中的方法

1、beforeSend

```
// 在请求发送之前调用
beforeSend: function () {
	alert('请求不会被发送')
	// 请求不会被发送
	return false;
},
```

2、serialize

​	作用：将表单中的数据自动拼接成字符串类型的参数

```
var params = $('#form').serialize();
// name=zhangsan&age=30

// 将内容转换为数组、对象类型
var params = obj.serializeArray();
var params = obj.serializeObject();
```

#### 5、全局事件（NProgress）

官宣：纳米级进度条，使用逼真的涓流动画来告诉用户正在发生的事情

https://github.com/rstacruz/nprogress

```
只要页面中有Ajax请求被发送，对应的全局事件就会被触发
.ajaxStart()     // 当请求开始发送时触发
.ajaxComplete()  // 当请求完成时触发

//引入文件
<link rel='stylesheet' href='nprogress.css'/>
<script src='nprogress.js'></script>

NProgress.start();  // 进度条开始运动 
NProgress.done();   // 进度条结束运动
```

例子：

```
			// 当页面中有ajax请求发送时触发			
			$(document).on('ajaxStart', function () {				 
				NProgress.start() 			
			})			
			
			// 当页面中有ajax请求完成时触发			
			$(document).on('ajaxComplete', function () {				
				NProgress.done() 			
			})
```

#### 6、RESTful 风格的 API

传统请求地址回顾

```
GET http://www.example.com/getUsers         
// 获取用户列表GET http://www.example.com/getUser?id=1     
// 比如获取某一个用户的信息
POST http://www.example.com/modifyUser      
// 修改用户信息
GET http://www.example.com/deleteUser?id=1  
// 删除用户信息
```

RESTful API 概述

```
GET：      获取数据
POST：    添加数据
PUT：      更新数据    
	http://www.example.com/users/1 修改用户ID为1的用户信息
DELETE： 删除数据      
	http://www.example.com/users/1 删除用户ID为1的用户信息
```



------

### Axios

简介：

​		基于promise用于浏览器和node.js的http客户端

 	   支持浏览器和node.js

​		支持promise

​		能拦截请求和响应

​		自动转换JSON数据

​		能转换请求和响应数据

官网：

​		https://github.com/axios/axios

​		https://www.npmjs.com/package/axios

基本用法：

> ```
> axios.get('http://localhost:3000/adata').then(function(ret){
>    // 注意data属性是固定的用法，用于获取后台的实际数据
>    // console.log(ret.data)
>    console.log(ret)
> })
> ```

发送get 请求：

> ```
> axios.get('http://localhost:3000/adata').then(function(ret){ 
>    #  拿到 ret 是一个对象      所有的对象都存在 ret 的data 属性里面
>    // 注意data属性是固定的用法，用于获取后台的实际数据
>    // console.log(ret.data)
>    console.log(ret)
> })
> ```

#### vue中的使用

```js
常用
下载： npm install axios -S
在src/utils下封装一个request.js模块
	import axios from 'axios'
	const request = axios.create({
		baseURL: '请求根路径'
	})
	export default request
	
使用：
（项目中常用）
	1、在src/api下封装请求接口文件xxxxAPI.js
			import request from '@/utils/request.js'

			// 按需导出
			export const getArticleAPI = function(_page, _limit) {
  				return request.get('/articles', {
    				// 请求参数
   				 	params: {
      					_page,
      					_limit
    				}
  				})
			}
            
    2、使用
    	// 按需导入API接口
  		import { getArticleAPI } from '@/api/articleAPI.js'

  		export default {
    		name: 'Home',
    		data() {
      			return {
        			page: 1,
        			limit: 10
      			}
    		},
    		created() {
      			this.initArticleList()
    		},
    		methods: {
      			// 封装获取文章列表数据的方法
      			async initArticleList() {
        			const { data: res } = await getArticleAPI(this.page, this.limit)
        			console.log(res)
      			}
    		}
  		}
   ----------------------------------------------------------------------------------------------
（常规使用）
// 导入封装axios文件
  import request from '@/utils/request.js'
  export default {
    name: 'Home',
    data() {
      return {
        page: 1,
        limit: 10
      }
    },
    created() {
      this.initArticleList()
    },
    methods: {
      // 封装获取文章列表数据的方法
      async initArticleList() {
        const { data: res } = await request.get('/articles', {
          // 请求参数
          params: {
            _page: this.page,
            _limit: this.limit
          }
        })
        console.log(res)
      }
    }
  }
```

```
在main.js中(不利于复用)

1、引入
	import axios from 'axios'

2、把axios挂载到vue实例对象上：
	配置公共的请求根路径 
	axios.defaults.baseURL = 'http://localhost:3000/';
	Vue.protoype.$http = axios
	
3、其他组件使用
	this.$http.get/post()
```

#### 请求传递参数(自服务器)

##### 1、get和 delete请求传递参数（相似）

 通过传统的url 以 ? 的形式传递参数 ：

> ```
> axios.get('http://localhost:3000/axios?id=123').then(function(ret){   console.log(ret.data)})
> ```

restful 形式传递参数 ：

> ```
> axios.get('http://localhost:3000/axios/123').then(function(ret){
>    console.log(ret.data)
> })
> ```

 通过params 形式传递参数：

> ```
> axios.get('http://localhost:3000/axios', {
>    	params: {
>      		id: 789
>    	}
> }).then(function(ret){
>   	console.log(ret.data)
> })
> ```

##### 2、post 和 put 请求传递参数（相似）

通过选项传递参数

> ```
> axios.post('http://localhost:3000/axios', {
>    	uname: 'lisi',
>    	pwd: 123
> }).then(function(ret){
>    console.log(ret.data)
> })
> ```

通过 URLSearchParams 传递参数 

> ```
> var params = new URLSearchParams();
>  params.append('uname', 'zhangsan');
>  params.append('pwd', '111');
>  axios.post('http://localhost:3000/axios', 	params).then(function(ret){
>    console.log(ret.data)
> })
> ```

#### 请求传递参数(引入文件)

```
<script crossorigin="anonymous" src="https://cdn.bootcdn.net/ajax/libs/axios/0.19.2/axios.js"></script>
```

```
			axios({
                //请求方法
                method : 'POST',
                //url
                url: '/axios-server',              
                params: {
                	/* GET参数 */
                    vip:10,
                    level:30
                },
                //请求体参数
                data: {
                	/* POST数据 */
                    username: 'admin',
                    password: 'admin'
                }，
                //头信息
                headers: {
                    a:100,
                    b:200
                }                
            }).then(response=>{
                //响应状态码
                console.log(response.status);
                //响应状态字符串
                console.log(response.statusText);
                //响应头信息
                console.log(response.headers);
                //响应体
                console.log(response.data);
            })
```



#### Axios响应结果

 data 实际响应回来的数据
 	    headers 响应头
 	    status响应状态码 
		 statusText响应状态信息

#### Axios中全局配置

```
配置公共的请求根路径
axios.defaults.baseURL = 'http://localhost:3000/';

配置 超时时间 
axios.defaults.timeout

配置公共的请求头 
axios.defaults.headers.common['Authorization']
  //配置请求头信息
  axios.defaults.headers['mytoken'] = 'hello';

总写：
axios.create({
  baseURL: 'https://some-domain.com/api/',
  timeout: 1000,
  headers: {'X-Custom-Header': 'foobar'}
});
```

#### Axios拦截器用法

##### 1、请求拦截器

> ```
> axios.interceptors.request.use(function(config) {
>    console.log(config.url)
>    config.headers.mytoken = 'nihao';
>    //必须有
>    return config;
> }, function(err){
>    console.log(err)
> })
> ```

##### 2、响应拦截器

> ```
> axios.interceptors.response.use(function(res) {
>    // console.log(res)
>    var data = res.data;
>    //必须有
>    return data;
> }, function(err){
>    console.log(err)
> })
> ```

#### async/await用法

async用于函数上，返回值为promise实例对象；

await用于async函数中，可以得到异步结果。

```
async function 函数名() {
	var ret = await axios.get('/data');
	return ret
}
函数名.then(ret => {console.log(ret)})
```

#### 取消请求

> ```
> axios({
>  url: 'http://localhost:4000/products1',
>  cancelToken: new axios.CancelToken(function executor(c){ // c是用于取消当前请求的函数
>    // 保存取消函数，用于之后可能需要取消当前请求
>    cancel = c;
>  })
> }).then(
>  response => {
>    cancel = null
>    console.log('请求1成功了', response.data)
>  },
>  error => {
>    cancel = null
>    console.log('请求1失败了', error.message, error) // 请求1失败了 强制取消请求 Cancel {message: "强制取消请求"}
>  }
> )
> ```



------

### Fetch

简介：

​	fetch默认是get请求；

​	返回promise对象。

官网：

 	https://developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API

基本用法：

> ```
> fetch('http://localhost:3000/fdata').then(function(data){
>    // text()方法属于fetchAPI的一部分，它返回一个Promise实例对象，用于获取后台返回的数据
>    return data.text();
> }).then(function(data){
>    console.log(data);
> })
> ```

注意事项：

​	 需要在 options 对象中 指定对应的 method    method:请求使用的方法 

 	post 和 普通请求的时候 需要在options 中 设置 请求头 headers  和请求体 body

#### 请求传递参数

##### 1、get和 delete请求传递参数（相似）

GET参数传递-传统URL

> ```
> fetch('http://localhost:3000/books?id=123', {
>     method: 'get'
> }).then(function(data){
>     return data.text();
> }).then(function(data){
>     console.log(data)
> });
> ```

GET参数传递-restful形式的URL

> ```
> fetch('http://localhost:3000/books/456', {
> 	method: 'get'
> }).then(function(data){
> 	return data.text();
> }).then(function(data){
> 	console.log(data)
> });
> ```

##### 2、post 和 put 请求传递参数（相似）

post 和 普通请求的时候 需要在options 中 设置 请求头 headers  和请求体 body

> ```
> fetch('http://localhost:3000/books', {
>  method: 'post',
>  body: 'uname=lisi&pwd=123',
>  headers: {
>       'Content-Type': 'application/x-www-form-urlencoded'
>  }
> }).then(function(data){
>  return data.text();
> }).then(function(data){
>  console.log(data)
> });
> ```

#### Fetch响应结果

用fetch来获取数据，如果响应正常返回，我们首先看到的是一个response对象，其中包括返回的一堆原始字节，这些字节需要在收到后，需要我们通过调用方法将其转换为相应格式的数据，比如`JSON`，`BLOB`或者`TEXT`等等。

> ```
> /*
>    Fetch响应结果的数据格式
> */
>  fetch('http://localhost:3000/json').then(function(data){
>    // return data.json();   //  将获取到的数据使用 json 转换对象
>    return data.text(); //  //  将获取到的数据 转换成字符串 
>  }).then(function(data){
>    // console.log(data.uname)
>    // console.log(typeof data)
>    var obj = JSON.parse(data);
>    console.log(obj.uname,obj.age,obj.gender)
>  })
> ```



------

### Promise

作用：

​	主要解决异步深层嵌套（回调地狱）；
​			语法更加简洁。

官网：

​	https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise

基本使用：我们使用new来构建一个Promise Promise的构造函数接收一个参数，是函数，并且传入两个参数：resolve，reject， 分别表示异步操作执行成功后的回调函数和异步操作执行失败后的回调函数

> ```
> var p = new Promise(function(resolve, reject){
>    // 这里用于实现异步任务
>    setTimeout(function(){
>      var flag = false;
>      if(flag) {
>        // 正常情况
>        resolve('hello');
>      }else{
>        // 异常情况
>        reject('出错了');
>      }
>    }, 100);
> });
> 
> p.then(function(data){
>    console.log(data)
> },function(info){
>    console.log(info)
> });
> //或者
> p.then(function(data){
>    console.log(data)
> }).catch(function(info){
>    console.log(info)
> });
> ```

#### 基于Promise发送Ajax请求

```
function queryData(url) {
     #   1.1 创建一个Promise实例
      var p = new Promise(function(resolve, reject){
        var xhr = new XMLHttpRequest();
        xhr.onreadystatechange = function(){
          if(xhr.readyState != 4) return;
          if(xhr.readyState == 4 && xhr.status == 200) {
            # 1.2 处理正常的情况
            resolve(xhr.responseText);
          }else{
            # 1.3 处理异常情况
            reject('服务器错误');
          }
        };
        xhr.open('get', url);
        xhr.send(null);
      });
      return p;
}
	# 注意：  这里需要开启一个服务 
    # 在then方法中，你也可以直接return数据而不是Promise对象，在后面的then中就可以接收到数据了
    queryData('http://localhost:3000/data')
      .then(function(data){
        console.log(data)
        #  1.4 想要继续链式编程下去 需要 return  
        return queryData('http://localhost:3000/data1');
      })
      .then(function(data){
        console.log(data);
        return queryData('http://localhost:3000/data2');
      })
      .then(function(data){
        console.log(data)
      });
```

#### Promise常用API

##### 1、实例方法

1、.then()得到异步任务正确的结果/2、

2、.catch()获取异常信息

3、.finally()成功与否都会执行（不是正式标准）

##### 2、对象方法

1、 .all()

Promise.all方法接受一个数组作参数，数组中的对象（p1、p2、p3）均为promise实例（如果不是一个promise，该项会被用Promise.resolve转换为一个promise)。它的状态由这三个promise实例决定。

2、.race()

Promise.race方法同样接受一个数组作参数。当p1, p2, p3中有一个实例的状态发生改变（变为fulfilled或rejected`），p的状态就跟着改变。并把第一个改变状态的promise的返回值，传给p的回调函数

例子：

> ```
> Promise.all([p1,p2,p3]).then(function(result){
> 	//all 中的参数  [p1,p2,p3]   和 返回的结果一 一对应["HELLO TOM", "HELLO JERRY", "HELLO SPIKE"]
>  console.log(result) //["HELLO TOM", "HELLO JERRY", "HELLO SPIKE"]
> })
> ```



------

### 同源、跨域、**JSONP** 

同源：协议、域名、端口号 必须完全相同，违背同源策略就是跨域。

#### **JSONP** 解决跨域问题

1、将不同源的服务器端请求地址写在 script 标签的 src 属性中

> ```
> <script src="http://localhost:3001/test"></script>
> <script src=“https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js"></script>
> ```

2、服务器端响应数据必须是一个函数的调用，真正要发送给客户端的数据需要作为函数调用的参数。

> ```
> const data = 'fn({name: "张三", age: "20"})';res.send(data);
> ```

3、在客户端全局作用域下定义函数 fn。

> ```
> function fn (data) { }
> ```

4、在 fn 函数内部对服务器端返回的数据进行处理。

> ```
> function fn (data) { console.log(data); }
> ```

##### JSONP 的使用

```
// 创建script标签
var script = document.createElement('script');
// 设置src属性，设置回调函数
script.src = 'http://localhost:3001/better?callback=fn2';
function abc(data) {
	alert(data.name); 
};
// 将script标签追加到页面中
document.body.appendChild(script);
// 为script标签添加onload事件
script.onload = function () {	
	// 将body中的script标签删除掉	
	document.body.removeChild(script);
}
	
--------------------------------------------------	
	//服务器中路由的处理
	router.get("/testAJAX" , function (req , res) { 	
		console.log("收到请求"); 	
		var data = {name:"孙悟空", age:18}	
		//将数据转化为字符串    
		let str = JSON.stringify(data);	
		var callback = req.query.callback; 	
		res.send(callback+"("+JSON.stringify(obj)+")"); 
	});
```

#### 封装JSONP

调用：

```
jsonp({	
	// 请求地址	
	url: 'http://localhost:3001/better',	
	data:{		
		source: 'pc',		
		weather_type: 'forecast_1h',		
		// weather_type: 'forecast_1h|forecast_24h',province: '黑龙江省',city: '哈尔滨市'
		}	
		success: function (data) {		
			console.log(456789)		
			console.log(data)	
		}
	})
```

封装：

```
function jsonp (options) {	
	// 动态创建script标签	
	var script = document.createElement('script');	
	// 拼接字符串的变量	
	var params = '';	
	for (var attr in options.data) {		
		params += '&' + attr + '=' + options.data[attr];	
	}// myJsonp0124741	
	var fnName = 'myJsonp' + Math.random().toString().replace('.', '');	
	// 它已经不是一个全局函数了	// 我们要想办法将它变成全局函数				window[fnName] = options.success;	
	// 为script标签添加src属性	
	script.src = options.url + '?callback=' + fnName + params;	
	// 将script标签追加到页面中	
	document.body.appendChild(script);	
	// 为script标签添加onload事件	
	script.onload = function () {										document.body.removeChild(script);	
	}
}
```

服务器端优化:

```
app.get('/user', (req, res) => {
	res.jsonp({name:'lisi', age:'19'})
})
```

#### **CORS** 解决跨域问题

简介：

​	CORS（Cross-Origin Resource Sharing），跨域资源共享。CORS 是官方的跨域解决方 案，它的特点是不需要在客户端做任何特殊的操作，完全在服务器中进行处理，支持 get 和 post 请求。跨域资源共享标准新增了一组 HTTP 首部字段，允许服务器声明哪些 源站通过浏览器有权限访问哪些资源 。

工作流程：

​	CORS 是通过设置一个响应头来告诉浏览器，该请求允许跨域，浏览器收到该响应 以后就会对响应放行。

CORS 的使用：（主要是服务器端的设置）

```
app.use((req, res, next) => { 	 
	//1.允许哪些客户端访问我、 	 
	// * 代表允许所有的客户端访问我	 // 注意：如果跨域请求中涉及到cookie信息传递，值不可以为*号 比如是具体的域名信息     
	res.header('Access-Control-Allow-Origin', '*');     
	// 2.允许客户端使用哪些请求方法访问我     
	res.header('Access-Control-Allow-Methods', 'GET, POST');     
	// 3.允许客户端发送跨域请求时携带cookie信息	 
	res.header('Access-Control-Allow-Credentials', true);     		next(); 
})//setHeader设置请求头
```

#### 访问非同源数据服务器端解决方案

```
//服务器端
app.get('/server', (req, res) => {	
	request('其它服务器请求地址', (err, response, body) => {					res.send(body);	
	})
});
```

#### withCredentials属性

1、在使用Ajax技术发送跨域请求时，默认情况下不会在请求中携带cookie信息

2、withCredentials：指定在涉及到跨域请求时，是否携带cookie信息，默认值为false

3、Access-Control-Allow-Credentials：true 允许客户端发送请求时携带cookie

## HTTP协议

通信三要素：通信的主体；通信的内容；通信的方式。



### HTTP请求消息的组成部分

​		HTTP 请求消息由请求行（request line）、请求头部（ header ） 、空行 和 请求体 4 个部分组成。

![image-20211010164654270](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010164654270.png)

**注意：只有 POST 请求才有请求体，GET 请求没有请求体！**



### HTTP响应消息的组成部分

​		HTTP响应消息由状态行、响应头部、空行 和 响应体 4 个部分组成，如下图所示：

![image-20211010183608953](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010183608953.png)



### HTTP的请求方法

![image-20211010183759466](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010183759466.png)



### HTTP响应状态码

​		HTTP 状态码由三个十进制数字组成，第一个十进制数字定义了状态码的类型，后两个数字用来对状态码进行细分。
HTTP 状态码共分为 5 种类型：

![image-20211010183850661](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010183850661.png)



![image-20211010184858750](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010184858750.png)



![image-20211010184919828](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010184919828.png)



![image-20211010184949461](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010184949461.png)



![image-20211010185001556](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211010185001556.png)

------

# Git

------

## **安装并配置** Git

https://git-scm.com/downloads

**配置用户信息**

安装完 Git 之后，要做的第一件事就是设置自己的用户名和邮件地址。因为通过 Git 对项目进行版本管理的时候，Git 需要使用这些基本信息，来记录是谁对项目进行了操作：

```
1、git config --global user.name "提交人姓名"
2、git config --global user.email "邮箱"
```

通过 git config --global user.name 和 git config --global user.email 配置的用户名和邮箱地址，会被写入到 C:/Users/用户名文件夹/.gitconfig 文件中。这个文件是 Git 的**全局配置文件**，**配置一次即可永久生效**。

## **检查配置信息**

```
1、查询安装版本
	git --version
2、查看配置信息
	git config --list
3、获取帮助信息
	git help <verb>
4、更新
	git update -git-for-windows
```

## **提交步骤**

```
1、初始化仓库
	git init
2、查看文件状态( git status 输出的状态报告很详细，但有些繁琐。如果希望以精简的方式显示文件的状态，可以使用如下两条完全等价的命令，其中 -s 是 --short 的简写形式)
	git status    或者  git status -s
3、跟踪新文件，添加到暂存区
	git add          git add .  //添加所有文件
4、向仓库提交代码
	git commit -m "提交信息"
5、查看提交信息
	git log
```

## **取消暂存的文件**

```
git reset HEAD 要移除的文件名称
```

##  跳过使用暂存区域，提交

```
git commit -a -m "提交信息"
```

## **移除文件**

```
1、从 Git 仓库和工作区中同时移除对应的文件
	git rm -f 文件名
2、只从 Git 仓库中移除指定的文件，但保留工作区中对应的文件
	git rm --cached 文件名
```

## 覆盖文件

```
1、暂存区的目录覆盖工作区文件
	git checkedout 文件
2、将git仓库中指定的更新记录恢复出来，并覆盖暂存区和工作目录
	git rest --hard commitID(黄色的)
```

## 回退到指定的版本

```
1、从新到旧
	git log --pretty=oneline//提交历史
	git rest --hard commitID(黄色的)//回退到指定的版本

2、从旧到新
	gie reflog --pretty=oneline//提交历史
	git rest --hard commitID(黄色的)//回退到指定的版本
```

## Github - 远程仓库的使

SSH key 由**两部分组成**，分别是：

​		① id_rsa（私钥文件，存放于客户端的电脑中即可）

​		② id_rsa.pub（公钥文件，需要配置到 Github 中）

**生成 SSH key**

​		① 打开 Git Bash

​		② 粘贴如下的命令，并将 your_email@example.com 替换为注册 Github 账号时填写的邮箱：

​			⚫ ssh-keygen -t rsa -b 4096 -C "your_email@example.com" 

​		③ 连续敲击 3 次回车，即可在 C:\Users\用户名文件夹\.ssh 目录中生成 id_rsa 和 id_rsa.pub 两个文件

**配置 SSH key**

​		① 使用记事本打开 id_rsa.pub 文件，复制里面的文本内容

​		② 在浏览器中登录 Github，点击头像 -> Settings -> SSH and GPG Keys -> New SSH key

​		③ 将 id_rsa.pub 文件中的内容，粘贴到 Key 对应的文本框中

​		④ 在 Title 文本框中任意填写一个名称，来标识这个 Key 从何而来

**检测 Github 的 SSH key 是否配置成功**

打开 Git Bash，输入如下的命令并回车执行：

- ```
  ssh -T git@github.com
  ```

上述的命令执行成功后，可能会看到如下的提示消息：

![image-20211007103449381](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103449381.png)

输入 yes 之后，如果能看到类似于下面的提示消息，证明 SSH key 已经配置成功

![image-20211007103457448](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103457448.png)

## 将本地仓库上传到 Github

```
1、   git push 远程地址 分支名称
2、   git push 远程地址别名 分支名称
			远程地址别名： git remote add 别名 远程地址
3、	 git push -u 远程地址别名 分支名
			-u 记住推送的远程地址及分支，下次只需git push即可
```

## 将远程仓库克隆到本地

```
git clone 远程仓库地址
```

## 本地分支操作

主分支： master

功能分支：feature

开发分支：develop

```
1、查看分支
	git branch
2、创建新分支
	git branch 分支名
3、切换分支
	git checkout 分支名
4、分支的快速创建和切换（创建新分支，并立即切换到新分支上）
	git checkout -b 分支名
5、合并分支（合并到哪先切换到哪分支）
	git merge 来源分支
6、删除分支（分支合并后才允许删除）  -D：强制删除
	git branch -d 分支名
```

## 远程分支操作

```
1、推送分支
	git push -u 远程仓库分支 本地分支
2、查看远程仓库所有分支列表
	git remote show 远程仓库名称
3、拉取远程库的最新版
	git pull 远程地址 分支名
4、删除远程分支
	git push 远程仓库名称 --delete 远程分支名称
```

## 为仓库添加详细说明

新建文件： README.m

------

# Vue

------

补充：安装Vetur插件可以使得.vue文件中的代码高亮

官网：https://cn.vuejs.org/v2/guide

## 使用步骤：

![image-20211006202619055](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006202619055.png)

模板：    差值表达式----{{  }}

## 指令

###   v-on（事件绑定）

- 用来绑定事件的
- 形式如：v-on:click  缩写为 @click;

![image-20211006202637144](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211006202637144.png)

事件函数调用：

​		1、直接调用: <xxx  @click='handle'>;

​		2、调用函数：<xxx  @click='handle（）'>;

处理逻辑：

```
写于methods中，

methods: {
	handle: function() {
		this.num++;     //一定要加this
	}
}

可以写成

methods: {              //常用
	handle () {
		this.num++;     //一定要加this  
	}
}
```

#### v-on事件函数中传入参数

```

            <!-- 如果事件直接绑定函数名称，那么默认会传递事件对象作为事件函数的第一个参数 -->
            <button v-on:click='handle1'>点击1</button>
            
            
            <!-- 2、如果事件绑定函数调用，那么事件对象必须作为最后一个参数显示传递，
                 并且事件对象的名称必须是$event 
            -->
            <button v-on:click='handle2(123, 456, $event)'>点击2</button>
      
      
      
<script type="text/javascript">
        var vm = new Vue({
            el: '#app',
            data: {
                num: 0
            },
            methods: {
                handle1: function(e) {
                    console.log(e.target.innerHTML)
                },
                handle2: function(p, p1, e) {
                    console.log(p, p1)
                    console.log(e.target.innerHTML)
                    this.num++;
                }
            }
        });
</script>
```



### v-model（双向数据绑定）

- **v-model**是一个指令，限制在 `<input>、<select>、<textarea>、components`中使用
- 数据发生变化的时候，视图也就发生变化
- 当视图发生变化的时候，数据也会跟着同步变化

```html
 <div id="app">
      <div>{{msg}}</div>
      <div>
          当输入框中内容改变的时候，  页面上的msg  会自动更新
        <input type="text" v-model='msg'>
      </div>
  </div>
```

### v-bind（属性绑定）

- v-bind 指令被用来响应地更新 HTML 属性（动态）

- v-bind:href    可以缩写为    :href;

- 可以使用js代码

- 单向数据绑定

  ```
  <!-- 绑定一个属性 -->
  <img v-bind:src="imageSrc">
  
  <!-- 缩写 -->
  <img :src="imageSrc">
  ```

### v-cloak     

- 防止页面加载时出现闪烁问题

```
 <style type="text/css">
  /* 
    1、通过属性选择器 选择到 带有属性 v-cloak的标签  让他隐藏
 */
  [v-cloak]{
    /* 元素隐藏    */
    display: none;
  }
  </style>
  
  /* 
    2、在差值表达式中插入指令
 */
  <div  v-cloak >{{msg}}</div>
```

### v-text

- v-text指令用于将数据填充到标签中，作用于插值表达式类似，但是没有闪动问题
- 如果数据中有HTML标签会将html标签一并输出
- 注意：此处为单向绑定，数据对象上的值改变，插值会发生变化；但是当插值发生变化并不会影响数据对象的值
- 会覆盖元素原有的默认值

```
<div id="app">
    <!--  
		注意:在指令中不要写插值语法  直接写对应的变量名称 
        在 v-text 中 赋值的时候不要在写 插值语法
		一般属性中不加 {{}}  直接写 对应 的数据名 
	-->
    <p v-text="msg"></p>
    <p>
        <!-- Vue  中只有在标签的 内容中 才用插值语法 -->
        {{msg}}
    </p>
</div>

<script>
    new Vue({
        el: '#app',
        data: {
            msg: 'Hello Vue.js'
        }
    });

</script>
```

### v-html

- 用法和v-text 相似  但是他可以将HTML片段填充到标签中

- 可能有安全问题, 一般只在可信任内容上使用 `v-html`，**永不**用在用户提交的内容上

- 它与v-text区别在于v-text输出的是纯文本，浏览器不会对其再进行html解析，但v-html会将其当html标签解析后输出。

```
<div id="app">
　　<p v-html="html"></p> <!-- 输出：html标签在渲染的时候被解析 -->
    
    <p>{{message}}</p> <!-- 输出：<span>通过双括号绑定</span> -->
    
　　<p v-text="text"></p> <!-- 输出：<span>html标签在渲染的时候被源码输出</span> -->
</div>
<script>
　　let app = new Vue({
　　el: "#app",
　　data: {
　　　　message: "<span>通过双括号绑定</span>",
　　　　html: "<span>html标签在渲染的时候被解析</span>",
　　　　text: "<span>html标签在渲染的时候被源码输出</span>",
　　}
 });
</script>
```

### v-pre

- 显示原始信息跳过编译过程
- 跳过这个元素和它的子元素的编译过程。
- **一些静态的内容不需要编译加这个指令可以加快渲染**

```
<span v-pre>{{ this will not be compiled }}</span>    
	<!--  显示的是{{ this will not be compiled }}  -->
	<span v-pre>{{msg}}</span>  
     <!--   即使data里面定义了msg这里仍然是显示的{{msg}}  -->
<script>
    new Vue({
        el: '#app',
        data: {
            msg: 'Hello Vue.js'
        }
    });

</script>
```

### **v-once**

- (只执行一次)执行一次性的插值【当数据改变时，插值处的内容不会继续更新】

```html
  <!-- 即使data里面定义了msg 后期我们修改了 仍然显示的是第一次data里面存储的数据即 Hello Vue.js  -->
     <span v-once>{{ msg}}</span>    
<script>
    new Vue({
        el: '#app',
        data: {
            msg: 'Hello Vue.js'
        }
    });
</script>
```

## 事件函数的调用

```
1、直接绑定
<button @click="handle">
//默认事件对象为第一参数
-----------------------------------------
2、函数调用
<button @click="handle(参数，$event)">
//参数之间使用","分隔
//$event为事件对象，必须作为最后一个参数传递 
```

## 事件修饰符

- 在事件处理程序中调用 `event.preventDefault()` 或 `event.stopPropagation()` 是非常常见的需求。
- Vue 不推荐我们操作DOM    为了解决这个问题，Vue.js 为 `v-on` 提供了**事件修饰符**
- 修饰符是由点开头的指令后缀来表示的

```
！！！<!-- 阻止冒泡 -->
<a v-on:click.stop="doThis"></a>

！！！<!-- 阻止默认事件 -->
<form v-on:submit.prevent="onSubmit"></form>

<!-- 修饰符可以串联   即阻止冒泡也阻止默认事件 -->
<a v-on:click.stop.prevent="doThat"></a>

<!-- 只当在 event.target 是当前元素自身时触发处理函数 -->
<!-- 即事件不是从内部元素触发的 -->
<div v-on:click.self="doThat">...</div>

使用修饰符时，顺序很重要；相应的代码会以同样的顺序产生。因此，用 v-on:click.prevent.self 会阻止所有的点击，而 
v-on:click.self.prevent 只会阻止对元素自身的点击。
```

## 按键修饰符

- 在做项目中有时会用到键盘事件，在监听键盘事件时，我们经常需要检查详细的按键。Vue 允许为 `v-on` 在监听键盘事件时添加按键修饰符

```html
<!-- 只有在 `keyCode` 是 13 时调用 `vm.submit()` -->
<input v-on:keyup.13="submit">

<!-- -当点击enter 时调用 `vm.submit()` -->
<input v-on:keyup.enter="submit">

<!--当点击enter或者space时  时调用 `vm.alertMe()`   -->
<input type="text" v-on:keyup.enter.space="alertMe" >

常用的按键修饰符
.enter =>    enter键
.tab => tab键
.delete (捕获“删除”和“退格”按键) =>  删除键
.esc => 取消键
.space =>  空格键
.up =>  上
.down =>  下
.left =>  左
.right =>  右

<script>
	var vm = new Vue({
        el:"#app",
        methods: {
              submit:function(){},
              alertMe:function(){},
        }
    })

</script>
```

## 自定义按键修饰符别名

- 在Vue中可以通过`config.keyCodes`自定义按键修饰符别名

```html
<div id="app">
    预先定义了keycode 116（即F5）的别名为f5，因此在文字输入框中按下F5，会触发prompt方法
    <input type="text" v-on:keydown.f5="prompt()">
</div>

<script>
	
    Vue.config.keyCodes.f5 = 116;

    let app = new Vue({
        el: '#app',
        methods: {
            prompt: function() {
                alert('我是 F5！');
            }
        }
    });
</script>
```

## 样式绑定

### 对象：

```
1、 class//v-bind:class="{类名:is开头的属性}"
<ul class="box" v-bind:class="{textColor:isColor, textSize:isSize}">

data:{
        isColor:true,
        isSize:true，
}

2、style
  <div v-bind:style="{color:activeColor,fontSize:activeSize}">对象语法</div>

data:{
    	activeColor:"red",
        activeSize:"25px",
}
```

### 数组：

```
//
<ul class="box" :class="[类名class, 类名class]"></ul>

 data:{
        类名class:‘类名‘,
        类名class:‘类名‘
 }
```

## 分支结构

### v-if 使用场景

1- 多个元素 通过条件判断展示或者隐藏某个元素。或者多个元素

```
<div id="app">
        <!--  判断是否加载，如果为真，就加载，否则不加载-->
        <span v-if="flag">
           如果flag为true则显示,false不显示!
        </span>
</div>

<script>
    var vm = new Vue({
        el:"#app",
        data:{
            flag:true
        }
    })
</script>
```

2- 进行两个视图之间的切换

```
 <div v-if="type === 'A'">
       A
    </div>
  <!-- v-else-if紧跟在v-if或v-else-if之后   表示v-if条件不成立时执行-->
    <div v-else-if="type === 'B'">
       B
    </div>
    <div v-else-if="type === 'C'">
       C
    </div>
  <!-- v-else紧跟在v-if或v-else-if之后-->
    <div v-else>
       Not A/B/C
    </div>

<script>
    new Vue({
      el: '#app',
      data: {
        type: 'C'
      }
    })
</script>
```

### v-show 

- v-show本质就是标签display设置为none，控制隐藏
  - v-show只编译一次，后面其实就是控制css，而v-if不停的销毁和创建，故v-show性能更好一点。
- v-if是动态的向DOM树内添加或者删除DOM元素
  - v-if切换有一个局部编译/卸载的过程，切换过程中合适地销毁和重建内部的事件监听和子组件

## 循环结构(v-for)

- **key 的作用---->必须写**  
  - **key来给每个节点做一个唯一标识**
  - **key的作用主要是为了高效的更新虚拟DOM**

```html
<ul>
  <li v-for="（item, index） in items" :key="item.id">...	</li>
</ul>

//:key="item.id"  当没有item.id 时可以用index
```

- **不推荐**同时使用 `v-if` 和 `v-for`
- 当 `v-if` 与 `v-for` 一起使用时，`v-for` 具有比 `v-if` 更高的优先级。

```
 <!-- 循环结构-遍历数组  
	item 是我们自己定义的一个名字  代表数组里面的每一项  
	items对应的是 data中的数组-->
	
<li v-for="item in items（数组名）">
    {{ item.message }}
</li> 
或者
<li v-for="（item, index） in items（数组名）">
    {{ item.message }}
</li> 

data: {
    items（数组名）: [
      { message: 'Foo' },
      { message: 'Bar' }
    ]， 
}
```

```
 <!--  循环结构-遍历对象
		v 代表   对象的value
		k  代表对象的 键 
		i  代表索引	
	---> 
     
<div v-if='v==13' v-for='(v,k,i) in obj（对象名）'>{{v + '---' + k + '---' + i}}</div>

data: {
    items: [
      { message: 'Foo' },
      { message: 'Bar' }
    ]，
    obj（对象名）: {
        uname: 'zhangsan',
        age: 13,
        gender: 'female'
    }
 }
```

## 表单基本操作

- 获取单选框中的值
  - 通过v-model

```
  	<!-- 
		1、 两个单选框需要同时通过v-model 双向绑定 一个值 
        2、 每一个单选框必须要有value属性  且value 值不能一样 
		3、 当某一个单选框选中的时候 v-model  会将当前的 value值 改变 data 中的 数据

		gender 的值就是选中的值，我们只需要实时监控他的值就可以了
	-->
   <input type="radio" id="male" value="1" v-model='gender'>
   <label for="male">男</label>

   <input type="radio" id="female" value="2" v-model='gender'>
   <label for="female">女</label>

<script>
    new Vue({
         data: {
             // 默认会让当前的 value 值为 2 的单选框选中
                gender: 2,  
            },
    })

</script>
```

- 获取复选框中的值
  - 通过v-model
  - 和获取单选框中的值一样 
  - 复选框 `checkbox` 这种的组合时   data 中的 hobby 我们要定义成数组 否则无法实现多选

```
<!-- 
		1、 复选框需要同时通过v-model 双向绑定 一个值 
        2、 每一个复选框必须要有value属性  且value 值不能一样 
		3、 当某一个单选框选中的时候 v-model  会将当前的 value值 改变 data 中的 数据

		hobby 的值就是选中的值，我们只需要实时监控他的值就可以了
	-->

<div>
   <span>爱好：</span>
   <input type="checkbox" id="ball" value="1" v-model='hobby'>
   <label for="ball">篮球</label>
   <input type="checkbox" id="sing" value="2" v-model='hobby'>
   <label for="sing">唱歌</label>
   <input type="checkbox" id="code" value="3" v-model='hobby'>
   <label for="code">写代码</label>
 </div>
<script>
    new Vue({
         data: {
                // 默认会让当前的 value 值为 2 和 3 的复选框选中
                hobby: ['2', '3'],
            },
    })
</script>
```

- 获取下拉框和文本框中的值
  - 通过v-model

```
 <div>
      <span>职业：</span>
       <!--
			1、 需要给select  通过v-model 双向绑定 一个值 
            2、 每一个option  必须要有value属性  且value 值不能一样 
		    3、 当某一个option选中的时候 v-model  会将当前的 value值 改变 data 中的 数据
		     occupation 的值就是选中的值，我们只需要实时监控他的值就可以了
		-->
       <!-- multiple  多选 -->
      <select v-model='occupation' multiple>
          <option value="0">请选择职业...</option>
          <option value="1">教师</option>
          <option value="2">软件工程师</option>
          <option value="3">律师</option>
      </select>
         <!-- textarea 是 一个双标签   不需要绑定value 属性的  -->
        <textarea v-model='desc'></textarea>
  </div>
<script>
    new Vue({
         data: {
                // 默认会让当前的 value 值为 2 和 3 的下拉框选中
                 occupation: ['2', '3'],
             	 desc: 'nihao'
            },
    })
</script>
```

### 表单修饰符

- .number  转换为数值

  - 注意点：	
  - 当开始输入非数字的字符串时，因为Vue无法将字符串转换成数值
  - 所以属性值将实时更新成相同的字符串。即使后面输入数字，也将被视作字符串。

- .trim  自动过滤用户输入的首尾空白字符

  - 只能去掉首尾的 不能去除中间的空格

- .lazy   将input事件切换成change事件

  - .lazy 修饰符延迟了同步更新属性值的时机。即将原本绑定在 input 事件的同步逻辑转变为绑定在 change 事件上
- 在失去焦点 或者 按下回车键时才更新

```
1、.number    自动将用户的输入值转为数值类型
	<input v-model.number='age'>

2、.trim  自动过滤用户输入的首尾空白字符
	<input v-model.trim='msg'>
	
3、.lazy  在'change'时而非'input'时更新(不实时同步，最后同步)
	<input v-model.lazy='msg'>
```

注意：

​		v-model默认是input事件；

​		下拉选项多选:

- ```
  	<select v-model="数组形式" multiple="true">
  ```

## 自定义指令   directive

#### 注册全局指令

```html
<!-- 
  使用自定义的指令，只需在对用的元素中，加上'v-'的前缀形成类似于内部指令'v-if'，'v-text'的形式。 
-->
<input type="text" v-focus>
<script>
// 注意点： 
//   1、 在自定义指令中  如果以驼峰命名的方式定义 如  Vue.directive('focusA',function(){}) 
//   2、 在HTML中使用的时候 只能通过 v-focus-a 来使用 
    
// 注册一个全局自定义指令 v-focus
Vue.directive('focus', function (el) {
    		// 聚焦元素
    		el.focus();
 	}
});
 --------------------------------------
 新版
    // binding 为自定义的函数形参   通过自定义属性传递过来的值 存在 binding.value 里面
Vue.directive('focus', function (el, binding) {
    // 当绑定元素插入到 DOM 中。 其中 el为dom元素
    		el.style.backgroundColor = binding.value.color;
});
------------------------------------------
new Vue({
　　el:'#app'
});
</script>
```

#### 注册全局指令 带参数

```
 <input type="text" v-color='msg'>
 <script type="text/javascript">
    /*
      自定义指令-带参数
      bind - 只调用一次，在指令第一次绑定到元素上时候调用

    */
    Vue.directive('color', {
      // bind声明周期, 只调用一次，指令第一次绑定到元素时调用。在这里可以进行一次性的初始化设置
      // el 为当前自定义指令的DOM元素  
      // binding 为自定义的函数形参   通过自定义属性传递过来的值 存在 binding.value 里面
      bind: function(el, binding){
        // 根据指令的参数设置背景色
        // console.log(binding.value.color)
        el.style.backgroundColor = binding.value.color;
      }
    });
    var vm = new Vue({
      el: '#app',
      data: {
        msg: {
          color: 'blue'
        }
      }
    });
  </script>
```

#### 局部指令

- 局部指令，需要定义在  directives 的选项   用法和全局用法一样 
- 局部指令只能在当前组件里面使用
- 当全局指令和局部指令同名时以局部指令为准

```
使用自定义指令
<input type="text" v-color='msg'>  //动态绑定值
<input type="text" v-focus>  //绑定值

 <script type="text/javascript">
    /*
      自定义指令-局部指令
    */
    var vm = new Vue({
      el: '#app',
      data: {
        msg: {
          color: 'red'
        }
      },
   	  //局部指令，需要定义在  directives 的选项
      directives: {
      	//动态绑定值
      	//el 指绑定指令的原生dom对象
      	//bind 函数只调用 1 次：当指令第一次绑定到元素时调用，当 DOM 更新时 bind 函数不会被触发。 
      	 // binding 为自定义的函数形参   通过自定义属性传递过来的值 存在 binding.value 里面
        color: {
          bind(el, binding){            
            el.style.backgroundColor = binding.value.color;
          }，
          //update 函数会在每次 DOM 更新时被调用。示例代码如下
          update(el, binding){            
            el.style.backgroundColor = binding.value.color;
          }
        },
        
        如果 insert 和update 函数中的逻辑完全相同，则对象格式的自定义指令可以简写成函数格式：
        color(el, binding) {            
            el.style.backgroundColor = binding.value.color;
        }，
        
        //绑定值
        focus: {
          inserted(el) {
             el.focus();
          }
        }
      }
    });
  </script>
```

## 计算属性	computed

**一定要有return**

```
 <div id="app">
     <!--  
        当多次调用 reverseString  的时候 
        只要里面的 num 值不改变 他会把第一次计算的结果直接返回
		直到data 中的num值改变 计算属性才会重新发生计算
     -->
    <div>{{reverseString}}</div>
    <div>{{reverseString}}</div>
     <!-- 调用methods中的方法的时候  他每次会重新调用 -->
    <div>{{reverseMessage()}}</div>
    <div>{{reverseMessage()}}</div>
  </div>
  <script type="text/javascript">
    /*
      计算属性与方法的区别:计算属性是基于依赖进行缓存的，而方法不缓存
    */
    var vm = new Vue({
      el: '#app',
      data: {
        msg: 'Nihao',
        num: 100
      },
      methods: {
        reverseMessage: function(){
          console.log('methods')
          return this.msg.split('').reverse().join('');
        }
      },
      //computed  属性 定义 和 data 已经 methods 平级 
      computed: {
        //  reverseString   这个是我们自己定义的名字 
        reverseString: function(){
          console.log('computed')
          var total = 0;
          //  当data 中的 num 的值改变的时候  reverseString  会自动发生计算  
          for(var i=0;i<=this.num;i++){
            total += i;
          }
          // 这里一定要有return 否则 调用 reverseString 的 时候无法拿到结果    
          return total;
        }
      }
    });
  </script>
```

## 侦听器   watch

- 使用watch来响应数据的变化
- 一般用于异步或者开销较大的操作
- watch 中的属性 一定是data 中 已经存在的数据 
- **当需要监听一个对象的改变时，普通的watch方法无法监听到对象内部属性的改变，只有data中的数据才能够监听到变化，此时就需要deep属性对对象进行深度监听**
- immediate 的作用是：控制侦听器是否自动触发一次！默认值是 false；

```
 <div id="app">
        <div>
            <span>名：</span>
            <span>
        		<input type="text" v-model='firstName'>
      		</span>
        </div>
  </div>

  <script type="text/javascript">
        var vm = new Vue({
            el: '#app',
            data: {
                firstName: 'Jim',
                info: {
         			 username: 'admin',
          			address: {
            			city: '北京'
          			}
        		}
            },
             //watch  属性 定义 和 data 已经 methods 平级 
            watch: {
                //   注意：  这里firstName  对应着data 中的 firstName 
                //   当 firstName 值 改变的时候  会自动触发 watch
                //newval是新值； oldval是旧值
                firstName (newval, oldval) {
                    this.fullName = val + ' ' + this.lastName;
                     // immediate 选项的默认值是 false
          			// immediate 的作用是：控制侦听器是否自动触发一次！
          			immediate: true
                },
                //对象形式
            	info: {
          			handler(newVal) {
            			console.log(newVal)
         	 		},
          			// 开启深度监听，只要对象中任何一个属性变化了，都会触发“对象的侦听器”
          			deep: true
       			}
        		// 如果要侦听的是对象的子属性的变化，则必须包裹一层单引号
        		'info.username'(newVal) {
          			console.log(newVal)
        		}
           	}
        });
    </script>
```

## 过滤器	filter(vue3.0没有)

- Vue.js允许自定义过滤器，可被用于一些常见的文本格式化。

- 过滤器可以用在两个地方：双花括号插值和v-bind表达式。

- 过滤器应该被添加在JavaScript表达式的尾部，由“管道”符号指示

- 支持级联操作

- 过滤器不改变真正的`data`，而只是改变渲染的结果，并返回过滤后的版本

- 全局注册时是filter，没有s的。而局部过滤器是filters，是有s的

- 在过滤器函数中，**一定要有 return 值**

- 大多使用全局过滤器

- 如果全局过滤器和私有过滤器名字一致，此时按照“**就近原则**”，调用的是”私有过滤器“

  调用过滤器：

  ```
  1、<div>{{msg | upper}}</div>
  2、<div :abc='msg | upper'>测试数据</div>
  ```

```
<div id="app">
    <input type="text" v-model='msg'>
      <!-- upper 被定义为接收单个参数的过滤器函数，表达式  msg  的值将作为参数传入到函数中 -->
    <div>{{msg | upper}}</div>
    <!--  
      支持级联操作
      upper  被定义为接收单个参数的过滤器函数，表达式msg 的值将作为参数传入到函数中。
	  然后继续调用同样被定义为接收单个参数的过滤器 lower ，将upper 的结果传递到lower中
 	-->
    <div>{{msg | upper | lower}}</div>
    <div :abc='msg | upper'>测试数据</div>
  </div>

<script type="text/javascript">
   
   //  lower  为全局过滤器     
   Vue.filter('lower', function(val) {
      return val.charAt(0).toLowerCase() + val.slice(1);
    });
    
    var vm = new Vue({
      el: '#app',
      data: {
        msg: ''
      },
       //filters  属性 定义 和 data 已经 methods 平级 
       //  定义filters 中的过滤器为局部过滤器 
      filters: {
        //   upper  自定义的过滤器名字 
        //    upper 被定义为接收单个参数的过滤器函数，表达式  msg  的值将作为参数传入到函数中
        upper(val) {
        	//val 代表形参  这里指msg
         //  过滤器中一定要有返回值 这样外界使用过滤器的时候才能拿到结果
          return val.charAt(0).toUpperCase() + val.slice(1);
        }
      }
    });
  </script>
```

#### 过滤器中传递参数

```
 <div id="box">
        <!--
			filterA 被定义为接收三个参数的过滤器函数。
  			其中 message 的值作为第一个参数，
			普通字符串 'arg1' 作为第二个参数，表达式 arg2 的值作为第三个参数。
		-->
        {{ message | filterA('arg1', 'arg2') }}
    </div>
    <script>
        // 在过滤器中 第一个参数 对应的是  管道符前面的数据   n  此时对应 message
        // 第2个参数  a 对应 实参  arg1 字符串
        // 第3个参数  b 对应 实参  arg2 字符串
        Vue.filter('filterA',function(n,a,b){
            if(n<10){
                return n+a;
            }else{
                return n+b;
            }
        });
        
        new Vue({
            el:"#box",
            data:{
                message: "哈哈哈"
            }
        })

    </script>
```

## 生命周期

| 创建阶段                       |                                                              |
| ------------------------------ | ------------------------------------------------------------ |
| beforeCreate                   | 在实例初始化之后，数据观测和事件配置之前被调用 此时data 和 methods 以及页面的DOM结构都没有初始化   什么都做不了 |
| **created**(操作数据，方法)    | 在实例创建完成后被立即调用此时data 和 methods已经可以使用  但是页面还没有渲染出来(发起ajax请求数据) |
| beforeMount                    | 在挂载开始之前被调用   此时页面上还看不到真实数据 只是一个模板页面而已 |
| **mounted**（操作dom）         | el被新创建的vm.$el替换，并挂载到实例上去之后调用该钩子。  数据已经真实渲染到页面上  在这个钩子函数里面我们可以使用一些第三方的插件 |
|                                |                                                              |
| 运行阶段                       |                                                              |
| beforeUpdate                   | 数据更新时调用，发生在虚拟DOM打补丁之前。   页面上数据还是旧的 |
| **updated**（操作更新后的DOM） | 由于数据更改导致的虚拟DOM重新渲染和打补丁，在这之后会调用该钩子。 页面上数据已经替换成最新的 |
|                                |                                                              |
| 销毁阶段                       |                                                              |
| beforeDestroy                  | 实例销毁之前调用                                             |
| destroyed                      | 实例销毁后调用                                               |

1、2、3、4为挂载；5、6为更新；7、8为销毁。

## ref引用

ref 用来辅助开发者在不依赖于 jQuery 的情况下，获取 DOM 元素或组件的引用。

每个 vue 的组件实例上，都包含一个 $refs 对象，里面存储着对应的 DOM 元素或组件的引用。默认情况下，组件的 $refs 指向一个空对象。

### 引用 DOM 元素

![image-20211007103618144](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103618144.png)

###  引用组件实例

![image-20211007103627711](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103627711.png)

###  this.$nextTick(cb)方法

组件的 $nextTick(cb) 方法，会把 cb 回调推迟到下一个 DOM 更新周期之后执行。通俗的理解是：等组件的DOM 更新完成之后，再执行 cb 回调函数。从而能保证 cb 回调函数可以操作到最新的 DOM 元素

![image-20211007103639379](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103639379.png)

## 数组方法

### every

判断数组中的值是否全部符合条件

```
arr.every(item => item.state)   //判断状态是否都为true
```

### reduce

把每次结果累加起来

```
arr.reduce(（累加的结果， 当前循环项）=> (return ******), 初始值)
```

### 数组变异方法

会影响数组的原始数据的变化。

| `push()`    | 往数组最后面添加一个元素，成功返回当前数组的长度             |
| ----------- | ------------------------------------------------------------ |
| `pop()`     | 删除数组的最后一个元素，成功返回删除元素的值                 |
| `shift()`   | 删除数组的第一个元素，成功返回删除元素的值                   |
| `unshift()` | 往数组最前面添加一个元素，成功返回当前数组的长度             |
| `splice()`  | 有三个参数，第一个是想要删除的元素的下标（必选），第二个是想要删除的个数（必选），第三个是删除 后想要在原位置替换的值 |
| `sort()`    | sort()  使数组按照字符编码默认从小到大排序,成功返回排序后的数组 |
| `reverse()` | reverse()  将数组倒序，成功返回倒序后的数组                  |

### 替换数组

不会影响原始的数组数据，而是形成一个新的数组。

| filter | filter() 方法创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素。 |
| ------ | ------------------------------------------------------------ |
| concat | concat() 方法用于连接两个或多个数组。该方法不会改变现有的数组 |
| slice  | slice() 方法可从已有的数组中返回选定的元素。该方法并不会修改数组，而是返回一个子数组 |

## 动态数组响应式数据

- Vue.set(a,b,c)    让 触发视图重新更新一遍，数据动态起来
- a是要更改的数据 、   b是数据的第几项、   c是更改后的数据

## 组件

### Vue单文件组件

每个单文件组件的后缀名都是.vue

每一个Vue单文件组件都由三部分组成
					1).template组件组成的模板区域
					2).script组成的业务逻辑区域
					3).style样式区域

```
<template>

    组件代码区域

</template>

<script>
	export default {
  		props: ["msg", "user"],
  		data() {
    		return {
    			数据
    		};
  		},
  		methods: {
   			
  		},
	};
</script>

<style lang="less" scoped>    //scoped  样式私有
	//如果给当前组件的 style 节点添加了 scoped 属性，则当前组件的样式对其子组件是不生效的。如果想让某些样式对子组件生效，可以使用 /deep/ 深度选择器
    /deep/ .title {
    	color: blue;
    }
    
    样式代码区域

</style>
```

#### 配置.vue文件的加载器

```
1.安装vue组件的加载器
    npm install vue-loader vue-template-compiler -D
2.配置规则：更改webpack.config.js的module中的rules数组
  const VueLoaderPlugin = require("vue-loader/lib/plugin");
    const vuePlugin = new VueLoaderPlugin();
    module.exports = {
        ......
        plugins:[ htmlPlugin, vuePlugin  ],
        module : {
            rules:[
                ...//其他规则
                { 
                    test:/\.vue$/,
                    loader:"vue-loader",
 				 }
        	]
    	}
	}
```

#### 在webpack中使用vue

安装处理了vue单文件组件的加载器，想要让vue单文件组件能够使用，我们必须要安装vue。

```
1.安装Vue
    npm install vue -S
2.在index.js中引入vue：import Vue from "vue"
3.创建Vue实例对象并指定el，最后使用render函数渲染单文件组件
    const vm = new Vue({
        el:"#app",
        render:h=>h(App)
    })
    
---------------------    
    导入根组件：(在index.js的import Vue from "vue"下面)
    	import App from "./components/App.Vue"
```

### 组件注册

#### 全局注册

老版本

```
 //  如果使用驼峰式命名组件，那么在使用组件的时候，只能在字符串模板中用驼峰的方式使用组件，
 //  但是在普通的标签模板中，必须使用短横线的方式使用组件
 Vue.component('HelloWorld', {
 	  // 组件参数的data值必须是函数 
      // 同时这个函数要求返回一个对象  
      data: function(){				
        return {
          msg: 'HelloWorld'
        }
      },
      //  组件模板必须是单个根元素
      //  组件模板的内容可以是模板字符串
      template: '<div>{{msg}}</div>
      	//在字符串模板中可以使用驼峰的方式使用组件	
		 <HelloWorld></HelloWorld>
      '
  });
   
 <!-- 必须使用短横线的方式使用组件 -->
     <hello-world></hello-world>
  
```

新版本

```
在 vue 项目的 main.js 入口文件中，通过 Vue.component() 方法，可以注册全局组件。示

1、 导入需要被全局注册的那个组件
import Count from '@/components/Count.vue'

2、注册
参数1:字符串格式，表示组件的"注册名称”；参数2:需要被全局注册的那个组件
Vue.component('MyCount', Count)

3、在需使用的组件中标签使用
<template>
  <div class="left-container">
    <h3>Left 组件</h3>
    <hr />
    <MyCount></MyCount>
  </div>
</template>
```

#### 局部注册

老版本

```
  <div id="app">
      <my-component></my-component>
  </div>


<script>

    // 定义组件的模板
    //Child采用驼峰命名
    var Child = {
      data: function() {},
      template: '<div>A custom component!</div>'
    }
    
    new Vue({
      //局部注册组件  
      components: {
        // <my-component> 将只在父模板可用  一定要在实例上注册了才能在html文件中使用
        'my-component': Child
      }
    })
    
</script>
```

新版本

```
步骤1：在APP.vue根组件中使用 import 语法导入需要的组件
import Left from "@/components/Left.vue";

步骤2：使用 components 节点注册组件
export default {
  data() {
    return {
      flag: true,
    };
  },
  // 2. 注册组件
  components: {
    Left,
    Right,
    Test,
  },
};

步骤3：以标签形式使用刚才注册的组件
<div class="box">
      <!-- 渲染 Left 组件和 Right 组件 -->
      <!-- 3. 以标签形式，使用注册好的组件 -->
      <Left></Left>
      <Right></Right>
</div>
```

### Vue 调试工具

安装： 官网-->生态系统-->Devtools

​		复制--->安装依赖包（npm install）-->构建（npm run build）-->打开Chrome扩张页面-->选中开发者模式-->加载已减压的扩展，选择shell/chrome。

### Vue组件之间传值

#### 父组件向子组件传值

- 父组件发送的形式是以**属性**的形式绑定值到子组件身上。
- 然后子组件用属性props接收
- 在props中使用驼峰形式，模板中需要使用短横线的形式字符串形式的模板中没有这个限制
- props中的数据是只读的，不直接修改，有需要时把值转存到data中，例如： count = this.传输的值

```
 父组件
 ····································
 <div id="app">
    <div>{{pmsg}}</div>
     <!--1、menu-item在APP中嵌套着故 menu-item为子组件-->    
     <!-- 给子组件传入一个静态的值 -->
    <menu-item title='来自父组件的值'></menu-item>
    
    <!-- 2、 需要动态的数据的时候 需要属性绑定的形式设置 此时 ptitle  来自父组件data 中的数据 .传的值可以是数字、对象、数组等等
	-->
    <menu-item :title='ptitle' content='hello'></menu-item>
</div>

var vm = new Vue({
      el: '#app',
      data: {
        pmsg: '父组件中内容',
        ptitle: '动态绑定属性'
      }
})
------------------------------------------------------------------------------------------------------------------
子组件（menu-item）
······························
		// 3、 子组件用属性props接收父组件传递过来的数据  
		
      数组形式
      props: ['title', 'content'],
      
      对象形式
      props: {
      	init: {
      		//default  定义默认值
      		default: 0,
      		//type  定义属性的值类型 (如果传递的值不符合，则会在终端报错)// 通过数组形式，为当前属性定义多个可能的类型 type: [Number, String],
     		 type: Object,
      		// 通过 default 函数，返回 cover 属性的默认值
      		 default: function() {
      		 // 这个 return 的对象就是 cover 属性的默认值
       			 return { type: 0 }
      		 }
     		
      		type: Number,
      		// required 必填项校验
      		required: true,
      	}
      
template: 
	<div>{{msg + "--" + title + "--" +content}}</div>
```

#### 子组件向父组件传值

- 子组件用`$emit()`触发事件
- `$emit()`  第一个参数为 **自定义的事件**名称     第二个参数为需要传递的数据
- 父组件用v-on 监听子组件的事件

```
<div id="app">
    <div :style='{fontSize: fontSize + "px"}'>{{pmsg}}</div>
     <!-- 2 父组件用v-on 监听子组件的事件
		这里 enlarge-text  是从 $emit 中的第一个参数对应   handle 为对应的事件处理函数	
	-->	
    <menu-item :parr='parr' @enlarge-text='handle($event)'></menu-item>
 
    /*子组件向父组件传值-携带参数*/
    Vue.component('menu-item', {
      props: ['parr'],
      template: `
        <div>
          <ul>
            <li :key='index' v-for='(item,index) in parr'>{{item}}</li>
          </ul>
			###  1、子组件用$emit()触发事件
			### 第一个参数为 自定义的事件名称   第二个参数为需要传递的数据  
          <button @click='$emit("enlarge-text", 5)'>扩大父组件中字体大小</button>
        </div>
      `
    });
    
    var vm = new Vue({
      el: '#app',
      data: {
        pmsg: '父组件中内容',
        parr: ['apple','orange','banana'],
        fontSize: 10
      },
      methods: {
        handle: function(val){
          // 扩大字体大小
          this.fontSize += val;
        }
      }
    });
```

新版本

![image-20211007103707612](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103707612.png)

![image-20211007103715892](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103715892.png)

#### 兄弟之间的传递

- 兄弟之间传递数据需要借助于事件中心，通过事件中心传递数据   
  - 提供事件中心    var hub = new Vue()
- 触发事件：hub.$emit('事件名称'，'参数')
- 监听事件：接收数据方，通过mounted(){} 钩子中  触发hub.$on('事件名称'，'事件函数(箭头函数)')
- 销毁事件： hub.$off('事件名称')

新方法：

![image-20211007103730166](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103730166.png)

```
 <div id="app">
    <div>父组件</div>
    <div>
      <button @click='handle'>销毁事件</button>
    </div>
    <test-tom></test-tom>
    <test-jerry></test-jerry>
  </div>
  <script type="text/javascript" src="js/vue.js"></script>
  <script type="text/javascript">
    /*
      兄弟组件之间数据传递
    */
    //1、 提供事件中心
    var hub = new Vue();

    Vue.component('test-tom', {
      data: function(){
        return {
          num: 0
        }
      },
      template: `
        <div>
          <div>TOM:{{num}}</div>
          <div>
            <button @click='handle'>点击</button>
          </div>
        </div>
      `,
      methods: {
        handle: function(){
          //2、传递数据方，通过一个事件触发hub.$emit(方法名，传递的数据)   触发兄弟组件的事件
          hub.$emit('jerry-event', 2);
        }
      },
      mounted: function() {
       // 3、接收数据方，通过mounted(){} 钩子中  触发hub.$on(方法名
        hub.$on('tom-event', (val) => {
          this.num += val;
        });
      }
    });
    Vue.component('test-jerry', {
      data: function(){
        return {
          num: 0
        }
      },
      template: `
        <div>
          <div>JERRY:{{num}}</div>
          <div>
            <button @click='handle'>点击</button>
          </div>
        </div>
      `,
      methods: {
        handle: function(){
          //2、传递数据方，通过一个事件触发hub.$emit(方法名，传递的数据)   触发兄弟组件的事件
          hub.$emit('tom-event', 1);
        }
      },
      mounted: function() {
        // 3、接收数据方，通过mounted(){} 钩子中  触发hub.$on()方法名
        hub.$on('jerry-event', (val) => {
          this.num += val;
        });
      }
    });
    var vm = new Vue({
      el: '#app',
      data: {
        
      },
      methods: {
        handle: function(){
          //4、销毁事件 通过hub.$off()方法名销毁之后无法进行传递数据  
          hub.$off('tom-event');
          hub.$off('jerry-event');
        }
      }
    });
  </script>

```

### 动态组件

#### component

动态组件指的是动态切换组件的显示与隐藏。

vue 提供了一个内置的 <component> 组件，专门用来实现动态组件的渲染。示例代码如下：

![image-20211007103745305](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103745305.png)

#### keep-alive 保持状态

默认情况下，切换动态组件时无法保持组件的状态。此时可以使用 vue 内置的 <keep-alive> 组件保持动态组件的状态。示例代码如下：

![image-20211007103755980](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103755980.png)

#####  keep-alive 对应的生命周期函数

当组件被缓存时，会自动触发组件的 deactivated 生命周期函数。

当组件被激活时，会自动触发组件的 activated 生命周期函数。

![image-20211007103829912](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103829912.png)

##### keep-alive 的 include属性

include 属性用来指定：**只有名称匹配的组件会被缓存**。多个组件名之间使用英文的**逗号分隔**：

![image-20211007103838965](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211007103838965.png)

### 组件插槽

组件插槽：父组件向子组件传递内容

标签中嵌套的内容会替换掉slot  如果不传值 则使用 slot 中的默认值

#### 匿名插槽

```
父组件 
····································
    <alert-box>有bug发生</alert-box>
    <alert-box>有一个警告</alert-box>
    <alert-box></alert-box>
---------------------------------------------------------
---------------------------------------------------------
子组件 
····························
          <strong>ERROR:</strong>
		# 当组件渲染的时候，这个 <slot> 元素将会被替换为“组件标签中嵌套的内容”。
		# 插槽内可以包含任何模板代码，包括 HTML
          <slot>默认内容</slot>
```

#### 具名插槽

- 具有名字的插槽 
- 使用 <slot> 中的 "name" 属性绑定元素
- 默认插槽的名字为default
- 新版<template v-slot:header>
  - v-slot:header     可以简写为  #header

```
父组件
····························
    <!-- 2、 通过slot属性来指定, 这个slot的值必须和下面slot组件得name值对应上，如果没有匹配到 则放到匿名的插槽中   --
    <base-layout>//子组件
      <!-- 注意点：template临时的包裹标签最终不会渲染到页面上     -->  
      <template slot='header'>
        <p>标题信息1</p>
        <p>标题信息2</p>
      </template>
      <p>主要内容1</p>
      <p>主要内容2</p>
      <template slot='footer'>
        <p>底部信息信息1</p>
        <p>底部信息信息2</p>
      </template>
    </base-layout>
------------------------------------------------------------------------------------------------------------------ 
子组件
·······························
  ###	1、 使用 <slot> 中的 "name" 属性绑定元素 指定当前插槽的名字
  ###  注意点： 
  ###  具名插槽的渲染顺序，完全取决于模板，而不是取决于父组件中元素的顺序
            <slot name='header'></slot>
			
            <slot name='footer'></slot>
```

#### 作用域插槽

- 父组件对子组件加工处理
- 在封装组件的过程中，可以为预留的 <slot> 插槽绑定 props 数据，这种带有 props 数据的 <slot> 叫做“作用域插槽”。
- 既可以复用子组件的slot，又可以使slot内容不一致

新版

```
父组件
······································
<my-com>  // 子组件名
	<template #content="scope">  //content是插槽名 ，这里的scope可以解构{msg, user}
		<p> {{scope.msg}} </p>  //scope是一个对象
		<p> {{scope.user.name}} </p>
	</template>
</my-com>
------------------------------------------------------------------------------------------------------------------
子组件
··································
<slot name="content" msg="hello vue.js" :user="userinfo"></slot>
	
export default {
  // 首字母要大写
  name: 'Article',
  data() {
    return {
      // 用户的信息对象
      userinfo: {
        name: 'zs',
        age: 20
      }
    }
  }
}
```

老版

```
<div id="app">
    <!-- 
		1、当我们希望li 的样式由外部使用组件的地方定义，因为可能有多种地方要使用该组件，但样式希望不一样 这个时候我们需要使用作用域插槽--> 
    <fruit-list :list='list'>
       <!-- 2、 父组件中使用了<template>元素,而且包含scope="slotProps",slotProps在这里只是临时变量---> 	
      <template slot-scope='slotProps'>
        <strong v-if='slotProps.info.id==3' class="current">
            {{slotProps.info.name}}		         
         </strong>
        <span v-else>{{slotProps.info.name}}</span>
      </template>
    </fruit-list>
  </div>
  <script type="text/javascript" src="js/vue.js"></script>
  <script type="text/javascript">
    /*
      作用域插槽
    */
    Vue.component('fruit-list', {
      props: ['list'],
      template: `
        <div>
          <li :key='item.id' v-for='item in list'>
			###  3、 在子组件模板中,<slot>元素上有一个类似props传递数据给组件的写法msg="xxx",
			###   插槽可以提供一个默认内容，如果如果父组件没有为这个插槽提供了内容，会显示默认的内容。如果父组件为这个插槽提供了内容，则默认的内容会被替换掉
            <slot :info='item'>{{item.name}}</slot>
          </li>
        </div>
      `
    });
    var vm = new Vue({
      el: '#app',
      data: {
        list: [{
          id: 1,
          name: 'apple'
        },{
          id: 2,
          name: 'orange'
        },{
          id: 3,
          name: 'banana'
        }]
      }
    });
  </script>
</body>
</html>
```

## Vue Router

vue-router 的官方文档地址：https://router.vuejs.org/zh/

安装：

```
npm install vue-router@3.5.2 -S
```

### 基本使用步骤

1、在 src 源代码目录下，新建 router/router.js 路由模块,代码如下：

- ```
  1、导入Vue和VueRouter的包
  	import Vue from 'vue'
  	import VueRouter from 'vue-router'
  
  2、调用vue.use()函数，装成插件
  	Vue.use(VueRouter)
  	
  3、插件路由实例对象
  	const router = new VueRouter({})
  	
  4、向外分享路由实例对象
  	export default router
  ```

2、在 src/main.js 入口文件中，导入并挂载路由模块。示例代码如下

- ```
  1、导入路由模块
  	import router from './router/router'
  	
  2、将路由挂载到Vue实例中
  	new Vue({
    		router,
    		render: h => h(App)
  	}).$mount('#app')
  ```

3、添加路由链接（在app.vue中）

- ```
  <router-link to="/user">User</router-link>
  ```

4、添加路由填充位（路由占位符）

- ```
  <router-view></router-view>
  ```

5、配置路由规则并创建路由实例（在 router/router.js）

- ```js
  //导入需要的组件（放于顶部）
  import User from '@/components/User.vue'
  import Login from '@/components/Login.vue'
  
  const router = new VueRouter({
  	//routes是路由规则数组
      routes:[
          //每一个路由规则都是一个对象，对象中至少包含path和component两个属性
          //path表示  路由匹配的hash地址，component表示路由规则对应要展示的组件对象
          {path:"/user",component:User},
          {path:"/login",component:Login}
      ]
  })
  ```

### 路由重定向

可以通过路由重定向为页面设置默认展示的组件

```
var myRouter = new VueRouter({
    //routes是路由规则数组
    routes: [
        //path设置为/表示页面最初始的地址 / ,redirect表示要被重定向的新地址，设置为一个路由即可
        { path:"/",redirect:"/user"},
        { path: "/user", component: User },
        { path: "/login", component: Login }
    ]
})
```

### 嵌套路由

```
//父组件
 //Login组件中的模板代码里面包含了子级路由链接以及子级路由的占位符
 <router-link to="/login/account">账号密码登录	 </router-link>
 <router-link to="/login/phone">扫码登录</router-link>
 
 <!-- 子路由组件将会在router-view中显示 -->
 <router-view></router-view>
//------------------------------------------------------------------------------------------------------
//在router/router.js中
	//导入需要的组件（放于顶部）
import User from '@/components/account.vue'
import Login from '@/components/phone.vue'
    
   var myRouter = new VueRouter({
        //routes是路由规则数组
        routes: [
            { 
                path: "/login", 
                component: Login,
                //通过children属性为/login添加子路由规则
                children:[
                    { path: "account", component: account },
                    { path: "phone", component: phone },
                ]
            }
        ]
    })
```

### 默认子路由

1、children的数组中，某个路由规则的path值为空值时，则这条规则叫做”默认子路由“；

2、路由重定向；

### 动态路由匹配

1、基本用法（不推荐）

- ```
  规则：
  var myRouter = new VueRouter({
      //routes是路由规则数组
      routes: [
          //通过/:参数名  的形式传递参数 
          { path: "/user/:id", component: User },
  })
  
  
  组件：可以通过 this.$route.params 对象访问到动态匹配的参数值，this可以省略
  var User = { template:"<div>用户：{{$route.params.id}}</div>"}
  ```

2、props传参

- ```
  规则：
  var myRouter = new VueRouter({
      //routes是路由规则数组
      routes: [
          //通过/:参数名  的形式传递参数 
          //如果props设置为true，route.params将会被设置为组件属性
          { path: "/user/:id", component: User,props:true },
  })
  
  
  组件：
  var User = { 
      props:["id"],//接收
      template:"<div>用户：{{id}}</div>"
  }
  ----------------------------------------------------------
  props为对象时：直接将对象的数据传递给组件进行使用
  				var User = { 
      				props:["username","pwd"],
      				template:"<div>用户：{{username}}---{{pwd}}</div>"
      			}
      			
      			var myRouter = new VueRouter({
     		 			//routes是路由规则数组
      				routes: [
          				//通过/:参数名  的形式传递参数 
          				//如果props设置为对象，则传递的是对象中的数据给组件
          				{ path: "/user/:id", component:User,props:{username:"jack",pwd:123} },
  				})
  		----------------------------------------------------------		
  props为函数形式：获取传递的参数值还想要获取传递的对象数据
  		var User = { 
      				 props:["username","pwd","id"],
      				 template:"<div>用户：{{id}} -> {{username}}---{{pwd}}</div>"
      			}
      			
      	var myRouter = new VueRouter({
     		 	//routes是路由规则数组
      		routes: [
          		//通过/:参数名  的形式传递参数 
          		//如果props设置为对象，则传递的是对象中的数据给组件
          		{ path: "/user/:id", component:User,props:(route)=>{
              		return{username:"jack",pwd:123,id:route.params.id}
              	} 
         		 ],
  		})
  ```

### 命名路由

```
var myRouter = new VueRouter({
    //routes是路由规则数组
    routes: [
        //通过name属性为路由添加一个别名
        { path: "/user/:id", component: User, name:"user"},
})
//添加了别名之后，可以使用别名进行跳转
<router-link to="/user">User</router-link>
<router-link :to="{ name:'user' , params: {id:123} }">User</router-link>
```

### 编程式导航

#### 1、声明式导航：

​	通过点击链接的方式实现的导航

#### 2、编程式导航：

​	调用js的api方法实现导航

​	在写行内式时，this一定要省略

```js
const User = {
	props: [xxx],
	template: `<button @click='goRe'>跳转</button>`,
	methods: {
		goRe() {
			this.$router.push("/hash地址");跳转到指定 hash 地址，并增加一条历史记录
----------------------------------------------------
			或者
			this.$router.go( n );//n为数字,正为前进。实现导航历史前进、后退
			简化：
				① $router.back()
					⚫ 在历史记录中，后退到上一个页面
				② $router.forward()
					⚫ 在历史记录中，前进到下一个页面
----------------------------------------------------
			或者
			this.$router..replace("/hash地址");跳转到指定的 hash 地址，并替换掉当前的历史记录
		}
	}
}
```

$router.push（）方法的参数规则：

- ('/home')    // hash地址；
- ({path: '/home'})			//对象；
- ({name: '/user', params: {}})   //命名路由
- ({path: '/register', query: {uname: 'list'}})  //带查询参数   ： /register?uname=list

### 导航守卫

导航守卫可以控制路由的访问权限。

每次发生路由的导航跳转时，都会触发全局前置守卫。因此，在全局前置守卫中，程序员可以对每个路由进行访问权限的控制：

```
router.beforeEach((to, from, next) => {
  // to 表示将要访问的路由的信息对象
  // from 表示将要离开的路由的信息对象
  // next() 函数表示放行的意思
  if (pathArr.indexOf(to.path) !== -1) {
  	//获取token值
    const token = localStorage.getItem('token')
    //判断是否有token值，有则通过，没有则调到登录页面
    if (token) {
      next()
    } else {
      next('/login')
    }
  } else {
    next()
  }
})
```

**next 函数的 3 种调用方式**：

1. 当前用户拥有后台主页的访问权限，直接放行：next()
2. 当前用户没有后台主页的访问权限，强制其跳转到登录页面：next('/login')
3. 当前用户没有后台主页的访问权限，不允许跳转到后台主页：next(false)

## 前端工程化（模块化）

浏览器端的模块化
        		1).AMD(Asynchronous Module Definition,异步模块定义)
        				代表产品为：Require.js
       		 2).CMD(Common Module Definition,通用模块定义)
        				代表产品为：Sea.js

---------------------------------------------------------------------

服务器端的模块化
       	 服务器端的模块化规范是使用CommonJS规范：
        		1).使用require引入其他模块或者包
        		2).使用exports或者module.exports导出模块成员
        		3).一个文件就是一个模块，都拥有独立的作用域

---------------------------------------------------------------------

ES6模块化
        	ES6模块化规范中定义：
           	 1).每一个js文件都是独立的模块
          	  2).导入模块成员使用import关键字
           	 3).暴露模块成员使用export关键字

---------------------------------------------------------------------

#### NodeJS中安装babel

​	1、输入命令：npm install --save-dev @babel/core @babel/cli @babel/preset-env @babel/node；

​	2、再次输入命令安装：npm install --save @babel/polyfill

​	3、在项目目录中创建babel.config.js文件。

	4、编辑js文件中的代码如下：
	    const presets = [
	        ["@babel/env",{
	            targets:{
	                edge:"17",
	                firefox:"60",
	                chrome:"67",
	                safari:"11.1"
	            }
	        }]
	    ]

​	5、暴露module.exports = { presets }

​	6、 在项目目录中创建index.js文件作为入口文件

​	7、打开终端，输入命令：npx babel-node ./index.js

#### ES6模块化基本语法

1、设置默认导入/导出

​				导出： export default {}；//一个模块只能用一次

​				导入： import  接收名称  from  "模块标识符"；

​			//如果在一个模块中没有向外暴露成员，其他模块引入该模块时将会得到一个空对象 

2、设置按需导入/导出

​				导出： export let myName = "jack";

​				导入： import { myName } from "模块化文件";

3、直接导入

​				 import "模块化文件";

## Vue脚手架

Vue脚手架可以快速生成Vue项目基础的架构。

官网：https://cli.vuejs.org/zh/

### 安装

```
3.x版本的Vue脚手架：
    npm install -g @vue/cli
    
    检查： vue -V
```

### 基于3.x版本的脚手架创建Vue项目

```
1).使用命令创建Vue项目(了解)
        命令：vue create 项目名称
        1、选择Manually select features(选择特性以创建项目)
        2、勾选特性可以用空格进行勾选。
        3、选择vue版本
        4、css预处理器选择：less
        5、第三方插件安装位置选择：in dedicated confug files
        6、是否保存为模板：n/y
        
        ESLint选择：ESLint + Standard config
        何时进行ESLint语法校验：Lint on save
        
2).基于ui界面创建Vue项目(常用)
        命令：vue ui
        在自动打开的创建项目网页中配置项目信息。
3).基于2.x的旧模板，创建Vue项目(了解)
        npm install -g @vue/cli-init
        vue init webpack my-project
```

### Vue脚手架生成的项目结构

```
node_modules:依赖包目录
public：静态资源目录
src：源码目录
src/assets:静态资源文件，例如：css 样式表、图片资源
src/components：组件目录
src/views:视图组件目录
src/App.vue:根组件
src/main.js:入口js
src/router.js:路由js
babel.config.js:babel配置文件
--------------------------------
postcss.config.js:配置前缀文件
.gitignore: 忽略文件
.prettierrc: vscode配置文件
			{
				"semi": false,  //移除分号
				"singleQuote":true    //把双引号改为单引号
			}
--------------------------------
.eslintrc.js:eslintrc语法配置文件
```

### Vue脚手架的自定义配置

```
 1.通过 package.json 进行配置 [不推荐使用]
        "vue":{
            "devServer":{
                "port":"9990",
                "open":true
            }
        }
 2.通过单独的配置文件进行配置，创建vue.config.js
        module.exports = {
            devServer:{
                port:8888,
                open:true
            }
        }
        
        --------------------------
        先npm run serve 再去配置，停止后再打开
```

## Vuex

Vuex是实现组件全局状态（数据）管理的一种机制，可以方便的实现组件之间的数据共享。

### 基本使用

```
1、手动安装
	a.安装vuex依赖包   npm install vuex --save
	b.导入vuex包   
			import Vuex from 'Vuex'
			Vue.use(Vuex)
	c.创建store对象
			const store = new Vuex.Store({
				//state中存放的是全局共享的数据
				state: { count: 0 }
			})

2、图形化界面安装
	a.输入命令：vue ui
	b.设置手动配置项目
```

### 属性 

#### 1、State

提供唯一的公共数据源，所有共享的数据都要统一放到Store中的State中存储。

```
在store.js中
在State对象中可以添加我们要共享的数据，如：count:0
-------------------------------------------------
1、this.$store.state.count

2、先按需导入mapState函数：import { mapState } from 'vuex'
   再将数据映射为计算属性：computed:{ ...mapState(['count']) }
   
   --------
   页面中采用差值表达式： {{count}}
```

#### 2、Mutation

用于修改变更$store中的数据

不能编写异步的代码

```
在store.js中，与state同级
----------------------------------
1、this.$store.commit('函数'，参数)
  		mutations: {
    		函数(state，step){
      			//第一个形参永远都是state也就是$state对象
      			//第二个形参是调用add时传递的参数
          		state.count+=step;
    		}
  		}
 
2、先按需导入mapMutations函数：import { mapState,mapMutations } from 'vuex'
   再映射为组件的methods函数：methods:{
  								...mapMutations(['函数'])，
  								//当点击按钮时触发Sub函数
  								 Add(){
          							//调用sub函数完成对数据的操作
          							this.函数(参数);
      							 }
						   }
```

#### 3、Action

在mutations中不能编写异步的代码，会导致vue调试器的显示出错。在vuex中我们可以使用Action来执行异步操作。

不能直接修改state中的值。

```
1、通过间接触发mutations
	mutations: {
    		函数(state，step){
      			//第一个形参永远都是state也就是$state对象
      			//第二个形参是调用add时传递的参数
          		state.count+=step;
    		}
  	}，
  	actions: {
  		函数(context,step){     //step是参数
    		setTimeout(()=>{
      			context.commit('函数',step);
    		},2000)
 		 }
  	}
  	//调用
  		methods:{
  			//这里的函数是点击事件中的<button @click="函数2">...+1</button>
  			
  			函数2(){   
   		 		this.$store.dispatch('函数',参数)
  			}
		}

2、先按需导入mapActions函数：import { mapState,mapMutations,mapActions } from 'vuex'
   再映射为组件的methods函数：methods:{														...mapMutations(['函数'])，
  								//当点击按钮时触发Sub函数
  								 Add(){
          							//调用sub函数完成对数据的操作
          							this.函数(参数);
      							 }，
      							 //获得mapActions映射的										 addAsync函数
      							 ...mapActions(['函数']),
      							 asyncSub(){
          							this.函数(参数);
      							 }
						    }
```

#### 4、Getter

Getter用于对Store中的数据进行加工处理形成新的数据。

```
在store.js中，与state同级
----------------------------------
getters:{
    //添加了一个showNum的属性
    函数 : state =>{
      return '最新的count值为：'+state.count;
    }
}

1、{{$store.getters.函数}}或者this.$store.getters.函数

2、先按需导入mapGetters函数：import { mapGetters } from 'vuex'
   再将数据映射为计算属性：computed:{ ...mapGetters(['函数']) }
```

#### 5、modules

放置子模块

```
modules: {
	user: { state:{ token: '123'}},
	setting: { statt: {name: 'vue'}}
}
先通过getters改变再在组件中引用
getters: {
	token: state => state.user.token,
	name: state => state.setting.name
}
再通过getters引用
computed: { ...mapGetters}
```

------

------

# React



### 官网

1. 英文官网:[ https://reactjs.org/](https://reactjs.org/)

2. 中文官网: https://react.docschina.org/

### React脚手架配置代理(发送网络请求)

#### axios

##### 前提

1、安转axios

```
npm install axios
```

2、引入文件

```
import axios from 'axios'
```



##### 方法一

> 在package.json中追加如下配置

```json
"proxy":"http://localhost:5000"
```

说明：

1. 优点：配置简单，前端请求资源时可以不加任何前缀。
2. 缺点：不能配置多个代理。
3. 工作方式：上述方式配置代理，当请求了3000不存在的资源时，那么该请求会转发给5000 （优先匹配前端资源）



##### 方法二

1. 第一步：创建代理配置文件

   ```
   在src下创建配置文件：src/setupProxy.js
   ```

2. 编写setupProxy.js配置具体代理规则：

   ```js
   const proxy = require('http-proxy-middleware')
   
   module.exports = function(app) {
     app.use(
       proxy('/api1', {  //api1是需要转发的请求(所有带有/api1前缀的请求都会转发给5000)
         target: 'http://localhost:5000', //配置转发目标地址(能返回数据的服务器地址)
         changeOrigin: true, //控制服务器接收到的请求头中host字段的值
         /*
         	changeOrigin设置为true时，服务器收到的请求头中的host为：localhost:5000
         	changeOrigin设置为false时，服务器收到的请求头中的host为：localhost:3000
         	changeOrigin默认值为false，但我们一般将changeOrigin值设为true
         */
         pathRewrite: {'^/api1': ''} //去除请求前缀，保证交给后台服务器的是正常请求地址(必须配置)
       }),
       proxy('/api2', { 
         target: 'http://localhost:5001',
         changeOrigin: true,
         pathRewrite: {'^/api2': ''}
       })
     )
   }
   ```

说明：

1. 优点：可以配置多个代理，可以灵活的控制请求是否走代理。
2. 缺点：配置繁琐，**前端请求资源时必须加前缀。**

例子：

```
axios.get(`/api1/search/users?q=${keyWord}`).then(
            response => {
                //请求成功后通知App更新状态
                this.props.updateAppState({isLoading:false,users:response.data.items})
            },
            error => {
                //请求失败后通知App更新状态
                this.props.updateAppState({isLoading:false,err:error.message})
            }
        )
```

#### fetch

```
在src下创建配置文件：src/setupProxy.js
编写setupProxy.js配置具体代理规则：

const proxy = require('http-proxy-middleware')

module.exports = function(app) {
  app.use(
    proxy('/api1', {  //api1是需要转发的请求(所有带有/api1前缀的请求都会转发给5000)
      target: 'http://localhost:5000', //配置转发目标地址(能返回数据的服务器地址)
      changeOrigin: true, //控制服务器接收到的请求头中host字段的值
      /*
      	changeOrigin设置为true时，服务器收到的请求头中的host为：localhost:5000
      	changeOrigin设置为false时，服务器收到的请求头中的host为：localhost:3000
      	changeOrigin默认值为false，但我们一般将changeOrigin值设为true
      */
      pathRewrite: {'^/api1': ''} //去除请求前缀，保证交给后台服务器的是正常请求地址(必须配置)
    }),
    proxy('/api2', { 
      target: 'http://localhost:5001',
      changeOrigin: true,
      pathRewrite: {'^/api2': ''}
    })
  )
}
```

例子：

```
	try {
			const response= await fetch(`/api1/search/users2?q=${keyWord}`)
			const data = await response.json()
			console.log(data);
			PubSub.publish('atguigu',{isLoading:false,users:data.items})
		} catch (error) {
			console.log('请求出错',error);
			PubSub.publish('atguigu',{isLoading:false,err:error.message})
		}
```



------

### React-router 

##### 路由的基本使用

​		1.明确好界面中的导航区、展示区

​		2.导航区的a标签改为Link标签  	

```
 <Link to="/xxxxx">Demo</Link>
```

​		3.展示区写Route标签进行路径的匹配

```
<Route path='/xxxx' component={Demo}/>
```

​		4.<App>的最外侧包裹了一个<BrowserRouter>或<HashRouter>

##### 封装NavLink

```
新建index.jsx文件
import React, { Component } from 'react'
import {NavLink} from 'react-router-dom'

export default class MyNavLink extends Component {
	render() {
		// console.log(this.props);
		return (
			<NavLink activeClassName="atguigu" className="list-group-item" {...this.props}/>
		)
	}
}
```

```
引入文件
import MyNavLink from './components/MyNavLink'

原来的Link改为下面的形式
<MyNavLink to="/about">About</MyNavLink>
<MyNavLink to="/home">Home</MyNavLink>
```

##### 路由组件与一般组件

​	  1.写法不同：

​            一般组件：<Demo/>

​            路由组件：<Route path="/demo" component={Demo}/>

​      2.存放位置不同：

​            一般组件：components

​            路由组件：pages

​      3.接收到的props不同：

​            一般组件：写组件标签时传递了什么，就能收到什么

​            路由组件：接收到三个固定的属性

​                      history:

​                            go: ƒ go(n)

​                            goBack: ƒ goBack()

​                            goForward: ƒ goForward()

​                            push: ƒ push(path, state)

​                            replace: ƒ replace(path, state)

​                      location:

​                            pathname: "/about"

​                            search: ""

​                            state: undefined

​                      match:

​                            params: {}

​                            path: "/about"

​                            url: "/about"

##### 解决多级路径刷新页面样式丢失的问题

​		1.public/index.html 中 引入样式时不写 ./ 写 / （常用）

​        2.public/index.html 中 引入样式时不写 ./ 写 %PUBLIC_URL% （常用）

​        3.使用HashRouter

##### 路由的严格匹配与模糊匹配

​		1.默认使用的是模糊匹配（简单记：【输入的路径】必须包含要【匹配的路径】，且顺序要一致）

​        2.开启严格匹配：<Route exact={true} path="/about" component={About}/>

​        3.严格匹配不要随便开启，需要再开，有些时候开启会导致无法继续匹配二级路由

##### Redirect、Switch的使用  

​	Redirect：

​		1.一般写在所有路由注册的最下方，当所有路由都无法匹配时，跳转到Redirect指定的路由

​        2.具体编码：

​	Switch：

​		渲染与该地址匹配的第一个子节点 `<Route>` 或者 `<Redirect>`

```
			<Switch>

​              <Route path="/about" component={About}/>

​              <Route path="/home" component={Home}/>

​              <Redirect to="/about"/>

​            </Switch>
```

##### 向路由组件传递参数

​		1.params参数

​              路由链接(携带参数)：<Link to='/demo/test/${xx.id}/${xx.age}'}>详情</Link>

​              注册路由(声明接收)：<Route path="/demo/test/:name/:age" component={Test}/>

​              接收参数：this.props.match.params

```
传递
state = {
		messageArr:[
			{id:'01',title:'消息1'},
			{id:'02',title:'消息2'},
			{id:'03',title:'消息3'},
		]
	}
	
<Link to={`/home/message/detail/${msgObj.id}/${msgObj.title}`}>{msgObj.title}</Link>

<Route path="/home/message/detail/:id/:title" component={Detail}/>

接收
const {id,title} = this.props.match.params
```

​        2.search参数

​              路由链接(携带参数)：<Link to={`/home/message/detail/?id=${msgObj.id}&title=${msgObj.title}`}}>详情</Link>

​              注册路由(无需声明，正常注册即可)：<Route path="/demo/test" component={Test}/>

​              接收参数：const {search} = this.props.location

​								 const {id,title} = qs.parse(search.slice(1))

​              备注：获取到的search是urlencoded编码字符串，需要借助querystring解析

```
传递
state = {
		messageArr:[
			{id:'01',title:'消息1'},
			{id:'02',title:'消息2'},
			{id:'03',title:'消息3'},
		]
	}
	
<Link to={`/home/message/detail/?id=${msgObj.id}&title=${msgObj.title}`}>{msgObj.title}</Link>

{/* search参数无需声明接收，正常注册路由即可 */}
<Route path="/home/message/detail" component={Detail}/>

接收
const {search} = this.props.location
const {id,title} = qs.parse(search.slice(1))
```

​        3.state参数

​              路由链接(携带参数)：<Link to={{pathname:'/demo/test',state:{name:'tom',age:18}}}>详情</Link>

​              注册路由(无需声明，正常注册即可)：<Route path="/demo/test" component={Test}/>

​              接收参数：const {id,title} = this.props.location.state || {}

​              备注：刷新也可以保留住参数

```
传递
state = {
		messageArr:[
			{id:'01',title:'消息1'},
			{id:'02',title:'消息2'},
			{id:'03',title:'消息3'},
		]
	}
	
<Link to={ {pathname:'/home/message/detail',state:{id:msgObj.id,title:msgObj.title} } }>{msgObj.title}</Link>

{/* state参数无需声明接收，正常注册路由即可 */}
<Route path="/home/message/detail" component={Detail}/>

接收
const {id,title} = this.props.location.state || {}

```

##### 编程式路由导航

借助this.prosp.history对象上的API对操作路由跳转、前进、后退

​              -this.prosp.history.push()

​              -this.prosp.history.replace()

​              -this.prosp.history.goBack()

​              -this.prosp.history.goForward()

​              -this.prosp.history.go()

**以上跳转携带什么类型的（params）参数，则向路由组件传递什么类型的（params）参数 ，路由声明接收什么类型的参数 ，都要一一对应（search,state类型的正常路由即可）**

例子：

```
//replace跳转+携带params参数
this.props.history.replace或者push(`/home/message/detail/${id}/${title}`)

			携带params参数
			(`/home/message/detail/${id}/${title}`)
			携带search参数
			(`/home/message/detail?id=${id}&title=${title}`)
			携带state参数
			(`/home/message/detail`,{id,title})

回退			
this.props.history.goBack()
前进
this.props.history.goForward()

数字为正，为前进；为负为回退；数字为几步
this.props.history.go(-2)
```

##### withRouter

作用：1、可以加工一般组件，让一般组件具备路由组件所特有的API

​			2、返回值是一个新组件

例子： 

```
import {withRouter} from 'react-router-dom'

class Header extends Component{}

export default withRouter(Header)
```



##### BrowserRouter与HashRouter的区别

**常用：BrowserRouter**

​	1.底层原理不一样：

​            BrowserRouter使用的是H5的history API，不兼容IE9及以下版本。

​            HashRouter使用的是URL的哈希值。

​      2.path表现形式不一样

​            BrowserRouter的路径中没有#,例如：localhost:3000/demo/test

​            HashRouter的路径包含#,例如：localhost:3000/#/demo/test

​      3.刷新后对路由state参数的影响

​            (1).BrowserRouter没有任何影响，因为state保存在history对象中。

​            (2).HashRouter刷新后会导致路由state参数的丢失！！！

​      4.备注：HashRouter可以用于解决一些路径错误相关的问题。

```
index.jsx  入口文件

//引入react核心库
import React from 'react'
//引入ReactDOM
import ReactDOM from 'react-dom'
//
import {BrowserRouter} from 'react-router-dom'
//引入App
import App from './App'

ReactDOM.render(
	<BrowserRouter>
		<App/>
	</BrowserRouter>,
	document.getElementById('root')
)
```



------

### 传递参数

##### 父子之间

​    1.【父组件】给【子组件】传递数据：通过props传递

```
父：
//初始化状态
	state = {todos:[
		{id:'001',name:'吃饭',done:true},
		{id:'002',name:'睡觉',done:true},
		{id:'003',name:'打代码',done:false},
		{id:'004',name:'逛街',done:false}
	]}
	
render() {
		const {todos} = this.state
		return (
			<div className="todo-container">
				<div className="todo-wrap">
					<Header addTodo={this.addTodo}/>
					<List todos={todos} />
					<Footer todos={todos}/>
				</div>
			</div>
		)
	}
	
子：List
const {todos} = this.props
```

​    2.【子组件】给【父组件】传递数据：通过props传递，要求父提前给子传递一个函数

```
父：
//初始化状态
	state = {todos:[
		{id:'001',name:'吃饭',done:true},
		{id:'002',name:'睡觉',done:true},
		{id:'003',name:'打代码',done:false},
		{id:'004',name:'逛街',done:false}
	]}
	
	父提前给子传递一个函数
//updateTodo用于更新一个todo对象
	updateTodo = (id,done)=>{
		//获取状态中的todos
		const {todos} = this.state
		//匹配处理数据
		const newTodos = todos.map((todoObj)=>{
			if(todoObj.id === id) return {...todoObj,done}
			else return todoObj
		})
		this.setState({todos:newTodos})
	}
	
render() {
		const {todos} = this.state
		return (
			<div className="todo-container">
				<div className="todo-wrap">
					<Header addTodo={this.addTodo}/>
					<List todos={todos} updateTodo={this.updateTodo} deleteTodo={this.deleteTodo}/>
					<Footer todos={todos} checkAllTodo={this.checkAllTodo} clearAllDone={this.clearAllDone}/>
				</div>
			</div>
		)
	}
	
子：List
const {todos,updateTodo,deleteTodo} = this.props

```

##### 兄弟之间

​	消息订阅与发布机制

​          1.先订阅，再发布（理解：有一种隔空对话的感觉）

​          2.适用于任意组件间通信

​          3.要在组件的componentWillUnmount中取消订阅

  

```
List 订阅
state = { //初始化状态
		users:[], //users初始值为数组
		isFirst:true, //是否为第一次打开页面
		isLoading:false,//标识是否处于加载中
		err:'',//存储请求相关的错误信息
	} 

	componentDidMount(){
		this.token = PubSub.subscribe('atguigu',(_,stateObj)=>{
			this.setState(stateObj)
		})
	}

	componentWillUnmount(){
		PubSub.unsubscribe(this.token)
	}

Search 发布
//发送请求前通知List更新状态
		PubSub.publish('atguigu',{isFirst:false,isLoading:true})
```

------

### React UI组件库

##### ant-design(国内蚂蚁金服)       简称antd

1、官网: https://ant.design/index-cn

2、Github: https://github.com/ant-design/ant-design/



安装： npm install antd

按需引入：按钮

​			import { Button} from 'antd';

有些组件需要单独引入：例如：icon小图标

​			import {WechatOutlined,WeiboOutlined,SearchOutlined} from '@ant-design/icons'



antd的按需引入+自定主题

```
1.安装依赖：yarn add react-app-rewired customize-cra babel-plugin-import less less-loader
2.修改package.json
					....
						"scripts": {
							"start": "react-app-rewired start",
							"build": "react-app-rewired build",
							"test": "react-app-rewired test",
							"eject": "react-scripts eject"
						},
					....
3.根目录下创建config-overrides.js
					//配置具体的修改规则
					const { override, fixBabelImports,addLessLoader} = require('customize-cra');
					module.exports = override(
						fixBabelImports('import', {
							libraryName: 'antd',
							libraryDirectory: 'es',
							style: true,
						}),
						addLessLoader({
							lessOptions:{
								javascriptEnabled: true,
								modifyVars: { '@primary-color': 'green' },
							}
						}),
					);
4.备注：不用在组件里亲自引入样式了，即：import 'antd/dist/antd.css'应该删掉
```



##### element ui



------

### redux

##### 学习文档

1、英文文档: https://redux.js.org/

2、中文文档: http://www.redux.org.cn/

3、Github: https://github.com/reactjs/redux

##### redux是什么

1、redux是一个专门用于做***\*状态管理\****的JS库(不是react插件库)。

2、 它可以用在react, angular, vue等项目中, 但基本与react配合使用。

3、 作用: 集中式管理react应用中多个组件***\*共享\****的状态。

#####  什么情况下需要使用redux

1、某个组件的状态，需要让其他组件可以随时拿到（共享）。

2、 一个组件需要改变另一个组件的状态（通信）。

3、总体原则：能不用就不用, 如果不用比较吃力才考虑使用。

##### redux的三个核心概念

1、action

​      1.1 动作的对象

​      1.2 包含2个属性

​			type：标识属性, 值为字符串, 唯一, 必要属性

​			ldata：数据属性, 值类型任意, 可选属性

​	   1.3 例子：{ type: 'ADD_STUDENT',data:{name: 'tom',age:18} }

2、reducer

​		1.1 用于初始化状态、加工状态。

​        1.2 加工时，根据旧的state和action， 产生新的state的纯函数

3、storer

​		3.1 将state、action、reducer联系在一起的对象

​		3.2 如何得到此对象?

​				1) import {createStore} from 'redux'

​				2) import reducer from './reducers'

​				3) const store = createStore(reducer)

​		3.3 此对象的功能?

​				1) getState(): 得到state

​				2) dispatch(action): 分发action, 触发reducer调用, 产生新的state

​				3) subscribe(listener): 注册监听, 当产生了新的state时, 自动调用

#####  redux的核心API

1、createstore()

​	作用：创建包含指定reducer的store对象

```
import {createStore, applyMiddleware} from 'redux'
export default createStore(reducers,composeWithDevTools(applyMiddleware(thunk)))
```

2、store对象

​	 作用: redux库最核心的管理对象

​	 核心方法:

​	 			store.getState()    得到state

​	 			store.dispatch(action)   分发action

```
store.dispatch({type:'increment',data:value*1})
```

​				 store.subscribe(listener)  

```
import store from './redux/store'
//调用render
store.subscribe(()=>{	ReactDOM.render(<App/>,document.getElementById('root'))
})
```

3、applyMiddleware()

​	作用：应用上基于redux的中间件(插件库)

```
import {createStore, applyMiddleware} from 'redux'
export default createStore(reducers,composeWithDevTools(applyMiddleware(thunk)))
```

4、combineReducers()

​	作用：合并多个reducer函数

```
import {combineReducers} from 'redux'
//引入为Count组件服务的reducer
import counts from './Count'
//引入为Count组件服务的reducer
import persons from './Person'

export default combineReducers({
    counts,
    persons
})
```

##### redux异步编程

1、使用异步中间件

npm install --save redux-thunk

```
//引入redux-thunk，用于支持异步action
import thunk from 'redux-thunk'
export default createStore(reducers,composeWithDevTools(applyMiddleware(thunk)))
```

##### 基于redux的案例（redux_test中的src _redux完整版）

![image-20210726173212572](C:\Users\LEO\AppData\Roaming\Typora\typora-user-images\image-20210726173212572.png)

**index.js入口文件**

```
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import store from './redux/store'

ReactDOM.render( <App />,document.getElementById('root'))
store.subscribe(()=>{
    ReactDOM.render(<App/>,document.getElementById('root'))
})
```



**APP.js**

```
import React, { Component } from 'react'
import Count from "./Component/Count";

export default class App extends Component{
  render() {
    return (
        <div>
          <Count/>
        </div>
    )
  }
}
```



**component组件**

```
import React, {Component} from 'react';
//引入store，用于获取redux中保存状态
import store from '../redux/store'
import {createIncrementAction, createDecrementAction} from '../redux/action'

class Count extends Component {
    increment = () => {
        const {value} = this.selectNum
        store.dispatch(createIncrementAction(value*1))
    }
    decrement = () => {
        const {value} = this.selectNum
        store.dispatch(createDecrementAction(value*1))
    }
    incrementIfOdd = () => {
        const {value} = this.selectNum
        const count = store.getState()
        if(count % 2 !== 0) {
            store.dispatch(createIncrementAction(value*1))
        }
    }
    incrementAsync = () => {
        const {value} = this.selectNum
       /* setTimeout(() => {
            store.dispatch(createIncrementAction(value*1))
        },500)*/
        store.dispatch(createIncrementAction(value*1,500))
    }
    render() {
        return (
            <div>
                <h1>当前求和为：{store.getState()}</h1>
                <select ref={c => this.selectNum = c}>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                </select>
                <button onClick={this.increment}>+</button>
                <button onClick={this.decrement}>-</button>
                <button onClick={this.incrementIfOdd}>当前求和为奇数再加</button>
                <button onClick={this.incrementAsync}>异步加</button>
            </div>
        );
    }
}

export default Count;
```



**store.js**

```
import {createStore, applyMiddleware} from 'redux'
import Reducer from "./reducer"
//引入redux-thunk，用于支持异步action
import thunk from 'redux-thunk'
export default createStore(Reducer,applyMiddleware(thunk))
```



**constant.js**

```
export const INCREMENT = 'increment'
export const DECREMENT = 'decrement'
```



**action.js**

```
import {INCREMENT,DECREMENT} from './constant'
export const createIncrementAction = data => ({type:INCREMENT,data:data})
export const createDecrementAction = data => ({type:DECREMENT,data})
export const  createIncrementAsyncAction = (data,time) => {
    return(dispatch) => {
        setTimeout(() => {
            dispatch(createIncrementAction(data))
        }, time)
    }
}
```





**reducer.js**

```
import {INCREMENT,DECREMENT} from './constant'
//初始化状态
const initState = 0
export default function Reducer (preState=initState, action) {
    const {type, data} = action
    switch (type) {
        case INCREMENT:
            return preState + data
        case DECREMENT:
            return preState - data
        default:
            return preState
    }
}
```



------

### react-redux

##### 分类

1、UI组件

​		只负责 UI 的呈现，不带有任何业务逻辑

​		通过props接收数据(一般数据和函数)

​		不使用任何 Redux 的 API

​		一般保存在components文件夹下

2、容器组件

​		责管理数据和业务逻辑，不负责UI的呈现

​		使用 Redux 的 API

​		一般保存在containers文件夹下

##### 相关API

1、Provider：让所有组件都可以得到state数据

```
import {Provider} from 'react-redux'
import store from './redux/store'

ReactDOM.render(
    <Provider store={store}>
        <App />
    </Provider>,
    document.getElementById('root')
```

2、 connect：用于包装 UI 组件生成容器组件

```
//引入connect用于连接UI组件与redux
import {connect} from 'react-redux'
//引入Count的UI组件
import CountUI from '../../components/Count/index'

//使用connect()()创建并暴露一个Count的容器组件
export default connect(mapStateToProps,mapDispatchToProps)(CountUI)
```

3、mapStateToprops：将外部的数据（即state对象）转换为UI组件的标签属性

```
/* 
	1.mapStateToProps函数返回的是一个对象；
	2.返回的对象中的key就作为传递给UI组件props的key,value就作为传递给UI组件props的value
	3.mapStateToProps用于传递状态
*/
function mapStateToProps(state){
	return {count:state}
}
```

4、mapDispatchToProps：将分发action的函数转换为UI组件的标签属性

```
/* 
	1.mapDispatchToProps函数返回的是一个对象；
	2.返回的对象中的key就作为传递给UI组件props的key,value就作为传递给UI组件props的value
	3.mapDispatchToProps用于传递操作状态的方法
*/
function mapDispatchToProps(dispatch){
	return {
		jia:number => dispatch(createIncrementAction(number)),
		jian:number => dispatch(createDecrementAction(number)),
		jiaAsync:(number,time) => dispatch(createIncrementAsyncAction(number,time)),
	}
}
```

##### 调试工具

1、安装chrome浏览器插件

![image-20210726174322006](C:\Users\LEO\AppData\Roaming\Typora\typora-user-images\image-20210726174322006.png)

2、下载工具依赖包

```
npm install --save-dev redux-devtools-extension
```

3、在store.js中引入

```
//引入redux-devtools-extension
import {composeWithDevTools} from 'redux-devtools-extension'

//暴露store 
export default createStore(allReducer,composeWithDevTools(applyMiddleware(thunk)))
```

##### 基于redux的案例（redux_test中的src ）

![image-20210726174805432](C:\Users\LEO\AppData\Roaming\Typora\typora-user-images\image-20210726174805432.png)

**index.js入口文件**

```
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import {Provider} from 'react-redux'
import store from './redux/store'

ReactDOM.render(
    <Provider store={store}>
        <App />
    </Provider>,
    document.getElementById('root')
)

```



**APP.js文件**

```
import React, { Component } from 'react'
import Count from './Containers/Count'
import Person from './Containers/Person'

export default class App extends Component{
  render() {
    return (
        <div>
          <Count/>
          <hr/>
          <Person/>
        </div>
    )
  }
}
```



***Containers中的容器组件***

```
import React, {Component} from 'react';
/*// 引入Count UI组件
import CountUI from '../Component/Count'*/
//引入action
import {
    increment,
    decrement,
    incrementAsync
} from '../redux/actions/Count'
//引入connect用于连接UI组件与redux
import {connect} from 'react-redux'


//定义UI组件
class Count extends Component {
    increment = () => {
        const {value} = this.selectNum
        this.props.increment(value*1)
    }
    decrement = () => {
        const {value} = this.selectNum
        this.props.decrement(value*1)
    }
    incrementIfOdd = () => {
        const {value} = this.selectNum
        if(this.props.count % 2 !== 0) {
            this.props.increment(value*1)
        }
    }
    incrementAsync = () => {
        const {value} = this.selectNum
        /* setTimeout(() => {
             store.dispatch(createIncrementAction(value*1))
         },500)*/
        this.props.incrementAsync(value*1,500)
    }
    render() {
        return (
            <div>
                <h2>我是Count组件,下方组件总人数为:{this.props.personCount}</h2>
                <h1>当前求和为：{this.props.count}</h1>
                <select ref={c => this.selectNum = c}>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                </select>
                <button onClick={this.increment}>+</button>
                <button onClick={this.decrement}>-</button>
                <button onClick={this.incrementIfOdd}>当前求和为奇数再加</button>
                <button onClick={this.incrementAsync}>异步加</button>
            </div>
        );
    }
}

/*// mapStateToProps用于传递状态
const mapStateToProps = (state) => {
    return {count:state}
}
// mapDispatchToProps用于传递操作状态的方法
const mapDispatchToProps = (dispatch) => {
    return {
        jia:number => dispatch(createIncrementAction(number)),
        jian:number => dispatch(createDecrementAction(number)),
        jiaAsync:(number,time) => dispatch(createIncrementAsyncAction(number,time)),
    }
}*/

//使用connect()()创建并暴露一个Count的容器组件
export default connect(
   /* mapStateToProps,
    mapDispatchToProps*/
   state => ({
       count:state.counts,
       personCount: state.persons.length
   }),
    {
        increment,
        decrement,
        incrementAsync
    }
)(Count)
```



**store.js文件**

```
import {createStore, applyMiddleware} from 'redux'

//引入redux-thunk，用于支持异步action
import thunk from 'redux-thunk'
//引入汇总之后的reducer
import reducers from './reducers/index'
//引入redux-devtools-extension
import {composeWithDevTools} from 'redux-devtools-extension'

export default createStore(reducers,composeWithDevTools(applyMiddleware(thunk)))
```



**constant.js文件**

```
export const INCREMENT = 'increment'
export const DECREMENT = 'decrement'
export const ADDPERSON = 'addPerson'
```



**action.js文件**

```
import {INCREMENT,DECREMENT} from '../constant'
export const increment = data => ({type:INCREMENT,data})
export const decrement = data => ({type:DECREMENT,data})
export const  incrementAsync = (data,time) => {
    return(dispatch) => {
        setTimeout(() => {
            dispatch(increment(data))
        }, time)
    }
}
```



**reducers中的组件**

```
import {INCREMENT,DECREMENT} from '../constant'
//初始化状态
const initState = 0
export default function Count (preState=initState, action) {
    const {type, data} = action
    switch (type) {
        case INCREMENT:
            return preState + data
        case DECREMENT:
            return preState - data
        default:
            return preState
    }
}
```



**reducers中的组件合并**

```
/* 
	该文件用于汇总所有的reducer为一个总的reducer
*/
//引入combineReducers，用于汇总多个reducer
import {combineReducers} from 'redux'
//引入为Count组件服务的reducer
import count from './count'
//引入为Person组件服务的reducer
import persons from './person'

//汇总所有的reducer变为一个总的reducer
export default  combineReducers({
	count,
	persons
})

```

##### 打包

npm run build

运行：npm install serve -g

​            serve





------

# webpack

------

实际项目中不需要自己配置webpack，使用CLI一键生成带有webpack的项目

### 导入

```
import msg from '../../msg'

可以写成 
//@代表src源代码目录
import msg from '@/msg.js'

需在webpack.config.js中配置 
module.exports = {
     resolve: {
     	alias: {
     		'@': path.join(__dirname, './src')
     	}
     }  
}
```



## 基本使用

1、 创建项目，并打开项目所在目录的终端，输入命令：npm init -y；生成package.jsoon

2、新建src源代码目录

3、新建src-->index.html首页和src-->index.js脚本文件

4、初始化首页基本结构

5、打开项目目录终端，输入命令: npm install jQuery -S安装jQuery

6、导入jQuery  打开index.js文件，编写代码导入jQuery并实现功能：	

```
 										 import $ from "jquery";
 										 
   										 $(function(){
       											 $("li:odd").css("background","cyan");
       											 $("li:even").css("background","pink");
    										})
```

注意：此时项目运行会有错误，因为import $ from "jquery";这句代码属于ES6的新语法代码，在浏览器中可能会存在兼容性问题，所以我们需要webpack来帮助我们解决这个问题。

## 安装、配置webpack

1、打开项目目录终端，输入命令: 

```
npm install webpack@5.42.1 webpack-cli@4.7.2 -D

​//-D  本地安装（只在开发阶段用的工具） -S  开发阶段和发布阶段都用到   -g全局安装      先全局安装再本地安装
//@代表指定版本
```

2、然后在项目根目录中，创建一个 webpack.config.js 的配置文件用来配置webpack

```
 module.exports = {
        mode:"development"//可以设置为development(开发模式)，production(发布模式)
 }
```

3、修改项目中的package.json文件添加运行脚本dev，如下：

```
 "scripts":{
        "dev":"webpack"
  }
```

4、运行dev命令进行项目打包，并在页面中引入项目打包生成的js文件，打开项目目录终端，输入命令:

```
npm run dev
```

**注意：**

​	等待webpack打包完毕之后，找到默认的dist路径中生成的main.js文件，将其引入到html页面中。 浏览页面查看效果。

## 配置webpack的打包入口/出口（大部分情况不需要）

默认     src/index.js       作为默认的打包入口js文件
默认     dist/main.js      作为默认的打包输出js文件

修改：通过改变 webpack.config.js 来设置入口/出口的js文件

```
const path = require("path");
    module.exports = {
        mode:"development",
        //设置入口文件路径
        entry: path.join(__dirname,"./src/xx.js"),
        //设置出口文件
        output:{
            //设置路径
            path:path.join(__dirname,"./dist"),
            //设置文件名
            filename:"res.js"
        }
	}
```

## 配置webpack的自动打包

1、安装自动打包功能的包

```
 npm install webpack-dev-server@3.11.2 -D
```

2、修改package.json中的dev指令如下：

```
 "scripts":{
       "dev":"webpack server"
  }
```

3、在index.html中将引入的js文件路径更改为：（可以不用自己写）

```
<script src="/bundle.js"></script>
```

4、运行npm run dev，进行打包

5、生成**预览页面**后打开网址查看效果：http://localhost:8080

**注意：**

​		webpack-dev-server自动打包的输出文件，默认放到了服务器的根目录中.

### 配置webpack的自动打包参数）（自动打开页面）

package.json文件，修改dev命令：

```
// 开发服务器 devServer：用来自动化，不用每次修改后都重新输入webpack打包一遍（自动编译，自动打开浏览器，自动刷新浏览器）
  // 特点：只会在内存中编译打包，不会有任何输出（不会像之前那样在外面看到打包输出的build包，而是在内存中，关闭后会自动删除）
  // 启动devServer指令为：npx webpack-dev-server
  devServer: {
    // 端口号
    port: 3000,
    // 自动打开浏览器
    open: true,
    //ip地址
    host 127.0.0.1,
    
    //暂时用不到
    // 项目构建后路径
    contentBase: resolve(__dirname, 'build'),
    // 启动gzip压缩
    compress: true,
  }
```

## 生成一个预览页面

1、安装默认预览功能的包

```
 npm install html-webpack-plugin@5.3.2 -D
```

2、修改webpack.config.js文件，如下：

```
//导入包
            const HtmlWebpackPlugin = require("html-webpack-plugin");
            //创建对象
            const htmlPlugin = new HtmlWebpackPlugin({
                //设置生成预览页面的模板文件
                template:"./src/index.html",
                //设置生成的预览页面名称
                filename:"./index.html"
            })
```

3、继续修改webpack.config.js文件，添加plugins信息：

```
module.exports = {
                ......
                plugins:[ htmlPlugin ]
}
```

## 加载器（loader）

通过loader打包非js模块：**默认情况下，webpack只能打包js文件**，如果想要打包非js文件，需要调用loader加载器才能打包。

  loader加载器包含：
            1).less-loader
            2).sass-loader
            3).url-loader:打包处理css中与url路径有关的文件
            4).babel-loader:处理高级js语法的加载器
            5).postcss-loader
            6).css-loader,style-loader

**注意**：指定多个loader时的顺序是固定的，而调用loader的顺序是从后向前进行调用。

### 1、打包css文件

```
 1).安装包
        npm install style-loader@3.0.0 css-loader@5.2.6 -D
 2).配置规则：更改webpack.config.js的module中的rules数组
    module.exports = {
        ......
        plugins:[ htmlPlugin ],
        module : {
            rules:[
                {
                    //test设置需要匹配的文件类型，支持正则//use表示该文件类型需要调用的loader
                    test: /\.css$/,use:['style-loader','css-loader']
                }
            ]
        }
    }
```

### 2、打包less文件

```
1).安装包
        npm install less-loader@10.0.1 less@4.1.1 -D
2).配置规则：更改webpack.config.js的module中的rules数组
    module.exports = {
        ......
        plugins:[ htmlPlugin ],
        module : {
            rules:[
                {
                    //test设置需要匹配的文件类型，支持正则//use表示该文件类型需要调用的loader
                    test: /\.css$/,use:['style-loader','css-loader']
                },
                {
                    test: /\.less$/,use:['style-loader','css-loader','less-loader']
                }
            ]
        }
    }
```

### 3、打包scss文件(暂时不用)

```
1).安装包
        npm install sass-loader node-sass -D
2).配置规则：更改webpack.config.js的module中的rules数组
    module.exports = {
        ......
        plugins:[ htmlPlugin ],
        module : {
            rules:[
                {
                    //test设置需要匹配的文件类型，支持正则
                    test:/\.css$/,
                    //use表示该文件类型需要调用的loader
                    use:['style-loader','css-loader']
                },
                {
                    test:/\.less$/,
                    use:['style-loader','css-loader','less-loader']
                },
                {
                    test:/\.scss$/,
                    use:['style-loader','css-loader','sass-loader']
                }
            ]
        }
    }

    补充：安装sass-loader失败时，大部分情况是因为网络原因，详情参考：
    https://segmentfault.com/a/1190000010984731?utm_source=tag-newest

```

### 4、配置post-css自动添加css的兼容性前缀(暂时不用)

```
1).安装包
    npm install postcss-loader autoprefixer -D
2).在项目根目录创建并配置postcss.config.js文件
const autoprefixer = require("autoprefixer");
module.exports = {
    plugins:[ autoprefixer ]
}
3).配置规则：更改webpack.config.js的module中的rules数组
module.exports = {
    ......
    plugins:[ htmlPlugin ],
    module : {
        rules:[
            {
                //test设置需要匹配的文件类型，支持正则
                test:/\.css$/,
                //use表示该文件类型需要调用的loader
                use:['style-loader','css-loader','postcss-loader']
            },
            {
                test:/\.less$/,
                use:['style-loader','css-loader','less-loader']
            },
            {
                test:/\.scss$/,
                use:['style-loader','css-loader','sass-loader']
            }
        ]
    }
}
```

### 5、打包样式表中的图片以及字体文件

```
1).安装包
    npm install url-loader@4.1. file-loader@6.2.0 -D
2).配置规则：更改webpack.config.js的module中的rules数组
module.exports = {
    ......
    plugins:[ htmlPlugin ],
    module : {
        rules:[
            {
                //test设置需要匹配的文件类型，支持正则
                test:/\.css$/,
                //use表示该文件类型需要调用的loader
                use:['style-loader','css-loader']
            },
            {
                test:/\.less$/,
                use:['style-loader','css-loader','less-loader']
            },
            {
                test:/\.scss$/,
                use:['style-loader','css-loader','sass-loader']
            },
            {
            	//limit用来设置字节数，只有小于limit值的图片，才会转换
                //为base64图片
                //outputPath=images为图片路径 
                test: /\.jpg|png|gif|bmp|ttf|eot|svg|woff|woff2$/,
                use:"url-loader?limit=1694&outputPath=images"
            }
        ]
    }
}
```

### 6、打包js文件中的高级语法

```
1.安装babel转换器
    npm install babel-loader@8.2.2 @babel/core@7.14.6 @babel/runtime@7.14.5 -D

2.配置规则：更改webpack.config.js的module中的rules数组
module.exports = {
    ......
    plugins:[ htmlPlugin ],
    module : {
        rules:[
            {
                //test设置需要匹配的文件类型，支持正则
                test:/\.css$/,
                //use表示该文件类型需要调用的loader
                use:['style-loader','css-loader']
            },
            {
                test:/\.less$/,
                use:['style-loader','css-loader','less-loader']
            },
            {
                test:/\.scss$/,
                use:['style-loader','css-loader','sass-loader']
            },
            {
                test:/\.jpg|png|gif|bmp|ttf|eot|svg|woff|woff2$/,
                //limit用来设置字节数，只有小于limit值的图片，才会转换
                //为base64图片
                use:"url-loader?limit=16940"
            },
            {
            	//exclude为排除项，意思是不要处理node_modules中的js文件
                test: /\.js$/, use:"babel-loader", exclude:/node_modules/
            }
        ]
    }
}

3.在项目根目录创建并配置babel.config.js文件
    module.exports = {
    	plugins:[ ["@babel/plugin-proposal-decorators", {legacy: true}]]
    }
    
    
------------------------------------------------------------------------------------------------- -- -------  ---------------------------------------
 (暂时不用)
 2.安装babel语法插件包
    npm install @babel/preset-env @babel/plugin-transform-runtime @babel/plugin-proposal-class-properties -D
3.在项目根目录创建并配置babel.config.js文件
    module.exports = {
        presets:["@babel/preset-env"],
        plugins:[ "@babel/plugin-transform-runtime", "@babel/plugin-proposal-class-properties" ]
    }
```

## 打包发布前配置自动清除dist目录

```
1、安装
	npm install --save-dev webpack-backup-output-plugin
	
	//老版本
	npm install --save-dev clear-wepback-plugin
	
2、在webpack.config.js中配置
	var WebpackBackupOutputPlugin = require('webpack-backup-output-plugin');
	
	module.exports = {
    ......
    plugins:[ htmlPlugin, new WebpackBackupOutputPlugin({ /* options */ })],
```

## 使用webpack打包发布项目

在项目上线之前，我们需要将整个项目打包并发布。

```
1.配置package.json的scripts增加
    "scripts":{
        "dev":"webpack server",  //开发阶段运行（生成文件放到内存中）
        "build":"webpack --mode produaction"   //用于打包命令  开发阶段运行
    }
    
    --------------------
    npm run build进行打包
    --------------------
```

### 把 JavaScript 文件统一生成到 js 目录中

在 webpack.config.js 配置文件的 output 节点中，进行如下的配置：

![image-20211009171921654](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211009171921654.png)

### **把图片文件统一生成到 image 目录中**

修改 webpack.config.js 中的 url-loader 配置项，新增 outputPath 选项即可指定图片文件的输出路径：

![image-20211009171953963](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211009171953963.png)

### **自动清理 dist 目录下的旧文件**

为了在每次打包发布时自动清理掉 dist 目录中的旧文件，可以安装并配置 clean-webpack-plugin 插件：

![image-20211009172020943](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211009172020943.png)



------

## 开发模式下配置SourceMap

是一个信息文件，里面存储着位置信息。有了他。出错的时候直显示原始代码，而不是转换获后的代码，能够极大的方便后期的调试。

**只定位行号不暴露源码**(推荐)

```
在webpack.config.js 中添加配置
module.exports = {	
		//在开发调试阶段 
       	devtool: 'nosources-sources-map',
	}
```

***发布阶段时要注释掉***

```
在webpack.config.js 中添加配置
module.exports = {	
		//在开发调试阶段 
       	devtool: 'eval-source-map',
	}
```

------

# Element-UI

------

Element-UI:一套基于2.0的桌面端组件库
	    官网地址：http://element-cn.eleme.io/#/zh-CN

```
1、基于命令行方式手动安装
A.安装：
    npm install element-ui -S
B.导入使用：
	//导入组件库
    import ElementUI from "element-ui";
    //导入相关样式
    import "element-ui/lib/theme-chalk/index.css";
    //配置Vue插件
    Vue.use(ElementUI)
    
2、基于图形化界面自动安装
A.打开图形化见界面    vue ui
B.配置Element-UI:在插件中安装，搜索vue-cli-plugin-element
 --------
 配置插件，实现按需导入（import on demand）
 --------
C.配置Axios：在依赖中安装,搜索axios(运行依赖)
```

------

# 打包

------

```
在艮目录下新建--》vue.config.js文件添加一下的规则module.exports = {  publicPath: './',}npm run build 进行打包
```

------

# 同、异步任务

① 同步任务（synchronous） 

​	⚫ 又叫做非耗时任务，指的是在主线程上排队执行的那些任务

​	⚫ 只有前一个任务执行完毕，才能执行后一个任务

​    ⚫new promise是一个 同步任务

② 异步任务（asynchronous） 

​	⚫ 又叫做耗时任务，异步任务由 JavaScript 委托给宿主环境进行执行

​	⚫ 当异步任务执行完成后，会通知 JavaScript 主线程执行异步任务的回调函数



**同步任务和异步任务的执行过程**

- ① 同步任务由 JavaScript 主线程次序执行

  ② 异步任务委托给宿主环境执行

  ③ 已完成的异步任务对应的回调函数，会被

  加入到任务队列中等待执行

  ④ JavaScript 主线程的执行栈被清空后，会

  读取任务队列中的回调函数，次序执行

  ⑤ JavaScript 主线程不断重复上面的第 4 步

JavaScript 主线程从“任务队列”中读取异步

任务的回调函数，放到执行栈中依次执行。这

个过程是循环不断的，所以整个的这种运行机

制又称为 EventLoop（事件循环）。



## **宏任务和微任务**

① 宏任务（macrotask） 

​	⚫ 异步 Ajax 请求、

​	⚫ setTimeout、setInterval、 

​	⚫ 文件操作

​	⚫ 其它宏任务

② 微任务（microtask） 

​	⚫ Promise.then、.catch 和 .finally

​	⚫ process.nextTick

​	⚫ 其它微任务



**宏任务和微任务的执行顺序**

![image-20211009164304237](C:\Users\Mario-Leo\AppData\Roaming\Typora\typora-user-images\image-20211009164304237.png)



------

# eslint规则(函数空格)

```
eslint规则

rules: {
    'no-console': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
    'no-debugger': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
    //'space-before-function-paren': ['error', 'never'],
    'space-before-function-paren': ['error', {
        'anonymous': 'always',
        'named': 'never',
        'asyncArrow': 'always'
    }],
    'vue/script-indent': ['error', 2, {  // script标签缩进设置
      'baseIndent': 1,
      'switchCase': 0,
      'ignores': []
    }]
  },
  overrides: [
    {
      "files": ["*.vue"],
      "rules": {
        "indent": "off",
      }
    }
  ],
```

------

# Vant主题订制

------

1、为了能够覆盖默认的 less 变量，一定要把引入Vant组件库的css后缀名改为 .less

2、在跟目录下新建--》vue.config.js文件

- ```
  // 这个文件是 vue-cli 创建出来的项目的配置文件// 在 vue.config.js 这个配置文件中，可以对整个项目的打包、构建进行全局性的配置// webpack 在进行打包的时候，底层用到了 node.js// 因此,在 vue.config.js 配置文件中，可以导入并使用 node.js 中的核心模块const path = require('path')const themePath = path.join(__dirname, './src/theme.less')module.exports = {  publicPath: './',  css: {    loaderOptions: {      less: {        modifyVars: {          // 或者可以通过 less 文件覆盖（文件路径为绝对路径）          //  ../    ./    theme.less          // 从盘符开始的路径，叫做绝对路径   C:\\Users\liulongbin\\theme.less          hack: `true; @import "${themePath}";`        }      }    }  }}
  ```

3、在src目录下新建--》xxx.less文件

- ```
  // 在 theme.less 文件中，覆盖 Vant 官方的 less 变量值1、定义变量@blue: #007bff;// 覆盖 Navbar 的 less 样式@nav-bar-background-color: @blue;@nav-bar-title-text-color: #fff;
  ```

------

# 项目上线

------

步骤一：通过node创建服务器

​		1、在项目文件（vue_shop）同级创建一个新文件夹vue_shop_server存放node服务器；

​		2、使用终端打开vue_shop_server文件夹，输入命令 npm init -y；

​		3、初始化包之后，输入命令 npm i express -S  ，安装express框架；

​		4、打开项目文件（vue_shop）目录，复制dist文件夹，粘贴到vue_shop_server中；

​		5、在vue_shop_server文件夹中创建app.js文件,编写代码如下：

- ```
  //引入express框架
  const express = require('express')
  //创建服务器
  const app = express()
  //静态资源处理
  app.use(express.static('./dist'))
  //监听端口
  app.listen(80,()=>{
      console.log("server running at http://127.0.0.1")
  })
  ```



步骤二：开启gzip压缩

​		1、打开vue_shop_server文件夹的终端，输入命令：npm i compression -D；

​		2、打开app.js,编写代码：

- ```
  const express = require('express')
  
  const compression = require('compression')
  
  const app = express()
  //一定要写到静态资源托管之前
  app.use(compression())
  app.use(express.static('./dist'))
  
  app.listen(80,()=>{
      console.log("server running at http://127.0.0.1")
  })
  ```



步骤三：配置https服务

​		*配置https服务一般是后台进行处理，前端开发人员了解即可*。

​		首先，需要申请SSL证书，进入https://freessl.cn官网，在后台导入证书，打开今天资料/		素材，复制素材中的两个文件到vue_shop_server中。
​				打开app.js文件，编写代码导入证书，并开启https服务

- ```
  const express = require('express')
  const compression = require('compression')
  //引入文件
  const https = require('https')
  const fs = require('fs')
  
  const app = express()
  
  //创建配置对象设置公钥和私钥
  const options = {
      cert:fs.readFileSync('./full_chain.pem'),
      key:fs.readFileSync('./private.key')
  }
  
  app.use(compression())
  app.use(express.static('./dist'))
  
  // app.listen(80,()=>{
  //     console.log("server running at http://127.0.0.1")
  // })
  
  //启动https服务
  https.createServer(options,app).listen(443)
  ```

  ​	注意：因为我们使用的证书有问题，所以无法正常使用https服务

步骤四：使用pm2管理应用	

​		1、打开电脑的终端，输入命令：npm i pm2 -g  安装
​				2、使用pm2启动项目，在项目终端中输入命令：pm2 start app.js --name 自定义名称
​				3、查看项目列表命令：pm2 ls
​						重启项目：pm2 restart 自定义名称
​						停止项目：pm2 stop 自定义名称
​						删除项目：pm2 delete 自定义名称

------

# 项目优化策略

------

#### 1、通过 nprogress 添加进度条效果

方法一：

- ```
  npm install --save nprogress 
  ```

方法二：在Vue项目中，通过 “ 运行依赖 ” 安装  nprogress

- ```
  步骤：在入口文件main.js中写入
  
  //导入进度条插件
  import NProgress from 'nprogress'
  //导入进度条样式
  import 'nprogress/nprogress.css'
  .....
  //请求在到达服务器之前，先会调用use中的这个回调函数来添加请求头信息
  axios.interceptors.request.use(config => {
    //当进入request拦截器，表示发送了请求，我们就开启进度条
    NProgress.start()
    //为请求头对象，添加token验证的Authorization字段
    config.headers.Authorization = window.sessionStorage.getItem("token")
    //必须返回config
    return config
  })
  //在response拦截器中，隐藏进度条
  axios.interceptors.response.use(config =>{
    //当进入response拦截器，表示请求已经结束，我们就结束进度条
    NProgress.done()
    return config
  })
  ```

------

#### 2、移除console指令

###### 	2.1 开发阶段和发布阶段都移除

注意：解决完serve中问题后再运行build命令

- ```
  步骤：
  1、在项目中安装“开发依赖”：babel-plugin-transform-remove-console
  2、打开项目根目录下的babel.config.js，编辑代码如下：
  
  module.exports = {
    "presets": [
      "@vue/app"
    ],
    "plugins": [
      [
        "component",
        {
          "libraryName": "element-ui",
          "styleLibraryName": "theme-chalk"
        }
      ],
      //添加的内容
      'transform-remove-console'
    ]
  }
  ```

###### 2.2 只移除发布阶段

- ```
  步骤：
  1、在项目中安装“开发依赖”：babel-plugin-transform-remove-console
  2、打开项目根目录下的babel.config.js，编辑代码如下：
  
  //项目发布阶段需要用到的babel插件
  const productPlugins = []
  
  //判断是开发还是发布阶段
  if(process.env.NODE_ENV === 'production'){
    //发布阶段
    productPlugins.push("transform-remove-console")
  }
  
  module.exports = {
    "presets": [
      "@vue/app"
    ],
    "plugins": [
      [
        "component",
        {
          "libraryName": "element-ui",
          "styleLibraryName": "theme-chalk"
        }
      ],
      ...productPlugins
    ]
  }
  ```

------

#### 3、生成打包报告

方法一：命令行形式生成打包报告

- ```
  vue-cli-service build --report
  ```

方法二（**推荐**）：在vue ui 控制面板的控制台生成打包报告

- ```
  点击“任务”=>“build”=>“运行”
  运行完毕之后点击右侧“分析”，“控制台”面板查看报告
  ```

------

#### 4、修改webpack的默认配置

默认情况下，vue-cli 3.0生成的项目，隐藏了webpack配置项，如果我们需要配置webpack
需要通过vue.config.js来配置。

###### 4.1为开发模式和发布模式指定不同的入口文件

1、开发模式入口文件：main-dev.js；

2、发布模式入口文件：main-prod.js；

在项目根目录中创建vue.config.js文件：

- ```
  module.exports = {
      chainWebpack:config=>{
          //发布模式
          config.when(process.env.NODE_ENV === 'production',config=>{
              //entry找到默认的打包入口，调用clear则是删除默认的打包入口
              //add添加新的打包入口
              config.entry('app').clear().add('./src/main-prod.js')
          })
          //开发模式
          config.when(process.env.NODE_ENV === 'development',config=>{
              config.entry('app').clear().add('./src/main-dev.js')
          })
      }
  }
  ```

  补充：
  	chainWebpack可以通过链式编程的形式，修改webpack配置
  	configureWebpack可以通过操作对象的形式，修改webpack配置

------

#### 5、通过externals加载外部CDN

默认情况下，依赖项的所有第三方包都会被打包到js/chunk-vendors.******.js文件中，导致该js文件过大，那么我们可以通过externals排除这些包，使它们不被打包到js/chunk-vendors.******.js文件中。

步骤1：

​		在vue.config.js，文件使用externals设置排除项

```
module.exports = {
    chainWebpack:config=>{
        //发布模式
        config.when(process.env.NODE_ENV === 'production',config=>{
            //entry找到默认的打包入口，调用clear则是删除默认的打包入口
            //add添加新的打包入口
            config.entry('app').clear().add('./src/main-prod.js')

            //使用externals设置排除项
            config.set('externals',{
                vue:'Vue',
                'vue-router':'VueRouter',
                axios:'axios',
                lodash:'_',
                echarts:'echarts',
                nprogress:'NProgress',
                'vue-quill-editor':'VueQuillEditor'
            })
        })
        //开发模式
        config.when(process.env.NODE_ENV === 'development',config=>{
            config.entry('app').clear().add('./src/main-dev.js')
        })
    }
}
```

步骤2：

设置好排除之后，为了使我们可以使用vue，axios等内容，我们需要加载外部CDN的形式解决引入依赖项。
		打开开发入口文件main-prod.js,<u>删除掉默认</u>的引入样式文件代码

```
// 导入vue-quill-editor的样式
// import 'quill/dist/quill.core.css'
// import 'quill/dist/quill.snow.css'
// import 'quill/dist/quill.bubble.css'

// 导入进度条样式
// import 'nprogress/nprogress.css'
```

[**<u>重点：步骤2和步骤3的上传与添加要一致</u>**]()

步骤3：

打开public/index.html头部添加外部cdn引入css文件代码

​		**例子：**

```
<!-- 富文本编辑器 的样式表文件 -->
    <link rel="stylesheet" href="https://cdn.staticfile.org/quill/1.3.4/quill.core.min.css" />
    <link rel="stylesheet" href="https://cdn.staticfile.org/quill/1.3.4/quill.snow.min.css" />
    <link rel="stylesheet" href="https://cdn.staticfile.org/quill/1.3.4/quill.bubble.min.css" />
    
<!-- nprogress 的样式表文件 -->
    <link rel="stylesheet" href="https://cdn.staticfile.org/nprogress/0.2.0/nprogress.min.css" />
```

步骤4：

打开public/index.html头部添加外部cdn引入对应js文件代码

​		**例子：**对应vur ui 控制面板的运行依赖

```
<script src="https://cdn.staticfile.org/vue/2.5.22/vue.min.js"></script>
    <script src="https://cdn.staticfile.org/vue-router/3.0.1/vue-router.min.js"></script>
    <script src="https://cdn.staticfile.org/axios/0.18.0/axios.min.js"></script>
    <script src="https://cdn.staticfile.org/lodash.js/4.17.11/lodash.min.js"></script>
    <script src="https://cdn.staticfile.org/echarts/4.1.0/echarts.min.js"></script>
    <script src="https://cdn.staticfile.org/nprogress/0.2.0/nprogress.min.js"></script>
<!-- 富文本编辑器的 js 文件 -->
    <script src="https://cdn.staticfile.org/quill/1.3.4/quill.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vue-quill-editor@3.0.4/dist/vue-quill-editor.js"></script>
```

------

#### 6、通过CDN优化Element UI的打包

步骤1：

​		在main-prod.js中，注释掉element-ui按需加载的代码

步骤2：

​		在public/index.html头部通过cdn加载element-ui的对应js和css样式文件代码

------

#### 7、自定制首页内容

开发环境的首页和发布环境的首页展示内容的形式有所不同，如开发环境中使用的是import加载第三方包，而发布环境则是使用CDN，那么首页也需根据环境不同来进行不同的实现，我们可以通过插件的方式来定制首页内容。

步骤1：

​		打开vue.config.js，编写代码如下：

```
module.exports = {
    chainWebpack:config=>{
        config.when(process.env.NODE_ENV === 'production',config=>{
            ......
            
            //使用插件
            config.plugin('html').tap(args=>{
                //添加参数isProd
                args[0].isProd = true
                return args
            })
            
        })

        config.when(process.env.NODE_ENV === 'development',config=>{
            config.entry('app').clear().add('./src/main-dev.js')

            //使用插件
            config.plugin('html').tap(args=>{
                //添加参数isProd
                args[0].isProd = false
                return args
            })
            
        })
    }
}
```

步骤2：

​		然后在public/index.html头部中使用插件判断是否为发布环境并定制首页内容

```
标题：
<title><%= htmlWebpackPlugin.options.isProd ? '' : 'dev - ' %>电商后台管理系统</title>

CDN外部资源：
<% if(htmlWebpackPlugin.options.isProd){ %>
    <!-- nprogress 的样式表文件 -->
    <link rel="stylesheet" href="https://cdn.staticfile.org/nprogress/0.2.0/nprogress.min.css" />
    ........
    <!-- element-ui 的 js 文件 -->
    <script src="https://cdn.staticfile.org/element-ui/2.8.2/router.js"></script>
    <% } %>
```

------

#### 8、路由懒加载

当路由被访问时才加载对应的路由文件，就是路由懒加载。

路由懒加载实现步骤：

​	步骤1：

​			安装 @babel/plugin-syntax-dynamic-import，打开vue控制台，点击依赖->安装依赖- >**开发依赖**->搜索@babel/plugin-syntax-dynamic-import，点击安装。

​	步骤2：

​			在babel.config.js中声明该插件，打开babel.config.js

```
//项目发布阶段需要用到的babel插件
const productPlugins = []

//判断是开发还是发布阶段
if(process.env.NODE_ENV === 'production'){
  //发布阶段
  productPlugins.push("transform-remove-console")
}

module.exports = {
  "presets": [
    "@vue/app"
  ],
  "plugins": [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "theme-chalk"
      }
    ],
    ...productPlugins,
    
    //配置路由懒加载插件
    "@babel/plugin-syntax-dynamic-import"
    
  ]
}
```

步骤3：

​		将路由更改为按需加载的形式，打开router.js，更改引入组件代码如下

```
import Vue from 'vue'
import Router from 'vue-router'
以上的两个不变

// import Login from './components/Login.vue'  改为下面的形式
// /* webpackChunkName:"login_home_welcome" */  名字相同的打包到一个文件中
const Login = () => import(/* webpackChunkName:"login_home_welcome" */ '../components/Login.vue')
```

------

# 微信小程序

------

****
