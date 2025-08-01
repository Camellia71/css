## 1.css-1

#### 1.css简介

##### 1.初步认识

HTML-结构

css-样式

##### 2.css语法规范

写在head标签中；由选择器和声明构成；属性+属性值叫做键值对。

```css
p {
    color:red;
    font-size:10px;
}
```

-选择器是用于指定CSS样式的HTML标签，花括号内是对该对象设置的具体样式

-属性和属性值以“键值对”的形式出现

-属性是对指定的对象设置的样式属性，例如字体大小、文本颜色等

-属性和属性值之间用英文“:”分开

-多个“键值对”之间用英文“;”进行区分

##### 3.css代码风格

###### 1.格式样式书写

紧凑格式

```css
h3 {color:red;font-size:20px;}
```

展开格式(优先)

```css
h3 {
   color:red;
   font-size:20px;
}
```

###### 2.样式大小写

优先小写

###### 3.空格

属性值后面，冒号前面，保留一个空格；

选择器和大括号之间保留一个空格；

#### 2.css基础选择器

##### 1.css选择器的作用

是选择标签用的

##### 2.选择器分类

包括基础选择器（标签选择器、类选择器、id 选择器和通配符选择器）和复合选择器

##### 3.标签选择器

标签选择器（元素选择器）是指用HTML 标签名称作为选择器，按标签名称分类，为页面中某一类标签指定统一的CSS 样式。

```css
p {
     color: darkgreen;
   }
```

##### 4.类选择器（开发最常用）

```html
<head>
.类名{
   属性1：属性值1
    color :...;
    width :...px;
    height :...px;
    background-color :...;
   ...
}
</head>
<body>
    <ul>
       <li class="类名">1</li>
       <li>2</li>
    </ul>
</body>     
```

-结构需要用class属性来调用 class 类的意思；

-类选择器使用“.”（英文点号）进行标识，后面紧跟类名（自定义，我们自己命名的）。

-可以理解为给这个标签起了一个名字，来表示。

-长名称或词组可以使用中横线来为选择器命名。

-不要使用纯数字、中文等命名，尽量使用英文字母来表示。

多类名：(一个标签有多个名字)

```html
<div class="red front1">多类名</div>
```

-在标签class 属性中写多个类名

-多个类名中间必须用空格分开

-这个div标签就可以分别具有这些类名的样式

##### 5.id选择器

```html
#id名 {
    属性1 ：属性值1；
    ...
}
<div id="id名">xixixi</div>
```

注意：id 属性只能在每个HTML 文档中出现一次。

id选择器和类选择器的区别:

-类选择器（class）好比人的名字，一个人可以有多个名字，同时一个名字也可以被多个人使用。

-id选择器好比人的身份证号码，全中国是唯一的，不得重复。

-id 选择器和类选择器最大的不同在于使用次数上。

-类选择器在修改样式中用的最多，id 选择器一般用于页面唯一性的元素上，经常和JavaScript 搭配使用。

##### 6.通配符选择器

在CSS 中，通配符选择器使用“*”定义，它表示选取页面中所有元素（标签）。

```html
* {
属性1 ：属性值1；
...
}
```

特殊情况才使用，后面讲解使用场景(以下是清除所有的元素标签的内外边距,后期讲)

```html
* {
    margin: 0;
    padding: 0;
}
```

#### 3.css字体属性

CSS Fonts (字体)属性用于定义字体系列、大小、粗细、和文字样式（如斜体）。

##### 3.1字体系列

-各种字体之间必须使用英文状态下的逗号隔开

-一般情况下,如果有空格隔开的多个单词组成的字体,加引号

```html
<style>
        h2 {
            font-family: '微软雅黑';
        }
        p {
            font-family: 'Microsoft YaHei' ;
        }
    </style>
```

可以直接给body指定字体

```html
body {
    font-family: 'Microsoft YaHei',tahoma,arial,'Hiragino Sans GB';
    }
```

##### 3.2字体大小

```html
<style>
    p {
        font-size:20px;
    }
</style>
```

标题标签比较特殊，需要单独指定文字大小；可以直接给body指定文字大小；

##### 3.3字体粗细

```html
<style>
    .bold {
        font-weight=:bold(bolder,lighter,normal,100-900的数字);
    }
</style>
<body>    
    <p class="bold">
        xixi
    </p>
</body>
```

400=normal;700=bold;

实际开发时，我们更喜欢用数字表示粗细

##### 3.4文字样式

```html
<style>
    p{
        font-style:normal;
    }
</style>
```

normal       默认值，标准字体样式

italic            斜体

注意：平时我们很少给文字加斜体，反而要给斜体标签（em，i）改为不倾斜字体。

##### 3.5复合属性

```html
body {
     font: font-style font-weight font-size/line-height font-family;
    }
```

顺序不能变；size和family必须有

#### 4.css文本属性

CSS Fonts (字体)属性用于定义字体系列、大小、粗细、和文字样式（如斜体）。

##### 4.1文本颜色

```html
div {
   color :red;
}
```

表示

预定义的颜色值           red,green等

十六进制                       #FF0000，#FF6600等                          **开发中最常用**

RGB代码                        rgb(255,0,0)或rgb(100%,0%,0%)

##### 4.2对齐文本

其实是用于盒子内的水平对齐；

```html
div {
    text-align:center;
}
```

left左对齐为默认值，还有center居中对齐，right右对齐；

##### 4.3装饰文本

text-decoration 属性规定添加到文本的修饰。可以给文本添加下划线、删除线、上划线等。

```html
div {
    text-decoration：underline；
}
```

none                            默认，没有装饰线

underline                    下划线

overline                       上划线

line-through               删除线

##### 4.4文本缩进

text-indent 属性用来指定文本的第一行的缩进，通常是将段落的首行缩进。

通过设置该属性，所有元素的第一行都可以缩进一个给定的长度，甚至该长度可以是负值。

```html
div {
    text-indent: 10px;
}
```

em是一个相对单位，就是当前元素（font-size) 1 个文字的大小, 如果当前元素没有设置大小，则会按照父元素的1 个文字大小。

```html
p{
    text-indent: 2em;
}
```

##### 4.5行间距

```html
p {
    line-height: 26px;
}
```

#### 5.css的引入方式

##### 5.1css的三种样式表

1.行内样式表（行内式）

2.内部样式表（嵌入式）

3.外部样式表（链接式）

##### 5.2内部样式表

内部样式表（内嵌样式表）是写到html页面内部. 

是将所有的CSS 代码抽取出来，单独放到一个<style> 标签中。

```html
<style>
    div{
        color: red;
        font-size: 12px;
    }
</style>
```

-<style> 标签理论上可以放在HTML文档的任何地方，但一般会放在文档的<head>标签中

-通过此种方式，可以方便控制当前整个页面中的元素样式设置

-代码结构清晰，但是并没有实现结构与样式完全分离

-使用内部样式表设定CSS，通常也被称为嵌入式引入，这种方式是我们练习时常用的方式

##### 5.3行内样式表

行内样式表（内联样式表）是在元素标签内部的style 属性中设定CSS 样式。适合于修改简单样式.

```html
<div style="color: red; font-size: 12px;">青春不常在，抓紧谈恋爱</div>
```

-style其实就是标签的属性

-在双引号中间，写法要符合CSS 规范

-可以控制当前的标签设置样式

-由于书写繁琐，并且没有体现出结构与样式相分离的思想，所以不推荐大量使用，只有对当前元素添加简单样式的时候，可以考虑使用

##### 5.4外部样式表

-新建一个后缀名为.css 的样式文件，把所有CSS 代码都放入此文件中。

-在HTML 页面head标签中，使用<link> 标签引入这个文件。

```html
<link rel="stylesheet" href="css 文件路径">
```

属性

rel         定义当前文档与被链接文档的关系，在这里需要指定为stylesheet，表示被链接的文件是一个样	      式表文件

href       定义所链接样式表文件的URL，可以是相对路径，也可以是绝对路径

-使用外部样式表设定CSS，通常也被称为外链式或链接式引入，这种方式是开发中常用的方式



## 2.css-2

#### 1.Emmet语法

##### 1.1快速生成HTML语法

1.生成标签直接输入标签名按tab键即可比如 div然后tab 键，就可以生成<div></div>

2.如果想要生成多个相同标签 加上* 就可以了比如div*3就可以快速生成3个div

3.如果有父子级关系的标签，可以用>比如ul> li就可以了

4.如果有兄弟关系的标签，用 + 就可以了比如div+p

5.如果生成带有类名或者id名字的， 直接写 .demo 或者 #twotab 键就可以了

6.如果生成的div 类名是有顺序的，可以用自增符号 $

7.如果想要在生成的标签内部写内容可以用 { } 表示

##### 1.2快速生成css语法

1.比如w200按tab 可以生成 width: 200px;

2.比如lh26px按tab 可以生成 line-height: 26px;

##### 1.3快速格式化代码

Vscode 快速格式化代码:shift+alt+f

也可以设置当我们保存页面的时候自动格式化代码:

1）文件------.>【首选项】---------->【设置】；

2）搜索emmet.include;

3）在settings.json下的【工作区设置】中添加以下语句：

"editor.formatOnType": true

"editor.formatOnSave": true

#### 2.css的复合选择器

##### 2.1介绍

在CSS 中，可以根据选择器的类型把选择器分为基础选择器和复合选择器，复合选择器是建立在基础选择器之上，对基本选择器进行组合形成的。

-复合选择器可以更准确、更高效的选择目标元素（标签）

-复合选择器是由两个或多个基础选择器，通过不同的方式组合而成的

-常用的复合选择器包括：后代选择器、子选择器、并集选择器、伪类选择器等等

##### 2.2后代选择器

```html
元素1 元素2 {样式声明}
```

上述语法表示选择元素1 里面的所有元素2 (后代元素)。

```html
<style>
    ol li {
        color : red;
    }
</style>
```

-元素1 和元素2 中间用空格隔开

-元素1 是父级，元素2 是子级，最终选择的是元素2

-元素2 可以是儿子，也可以是孙子等，只要是元素1 的后代即可

-元素1 和元素2 可以是任意基础选择器

```html
    <style>
        ol li a {
            color : red;
        }
    </style>
<body>
    <ol>
        <li><a href="#">xixi</a></li>
    </ol>
</body>
或者
<style>
      .nav li a {
            color: green;
        }
</style>
```

##### 2.3子选择器

子元素选择器（子选择器）只能选择作为某元素的最近一级子元素。简单理解就是选亲儿子元素

```html
元素1 > 元素2 { 样式声明}
```

上述语法表示选择元素1 里面的所有直接后代(子元素) 元素2。

```
div > p {样式声明}     /*选择div里面所有最近一级p标签元素*/
```

-元素1 和元素2 中间用大于号隔开

-元素1 是父级，元素2 是子级，最终选择的是元素2

-元素2 必须是亲儿子，其孙子、重孙之类都不归他管. 你也可以叫他亲儿子选择器

##### 2.4并集选择器

并集选择器可以选择多组标签, 同时为他们定义相同的样式，通常用于集体声明

并集选择器是各选择器通过英文逗号（,）连接而成，任何形式的选择器都可以作为并集选择器的一部分。

```html
元素1,
元素2 {样式声明}
```

上述语法表示选择元素1 和元素2

```html
ul,
div，
.pig li{样式声明}        /*选择u1,div和pig中的li标签元素*/
```

-元素1 和元素2 中间用逗号隔开

-逗号可以理解为和的意思

-并集选择器通常用于集体声明

##### 2.5伪类选择器

伪类选择器用于向某些选择器添加特殊的效果，比如给链接添加特殊效果，或选择第1个，第n个元素。

伪类选择器书写最大的特点是用冒号（:）表示，比如:hover 、:first-child 

有链接伪类、结构伪类等.

##### 2.6链接伪类选择器

```html
a:link                  /*选择所有未被访问的链接*/
a:visited               /*选择所有已被访问的链接*/
a:hover                 /*选择鼠标指针位于其上的链接*/
a:active                /*选择活动链接（鼠标按下未弹起的链接）*/
```

链接伪类选择器注意事项:

为了确保生效，请按照LVHA的循顺序声明:link－:visited－:hover－:active。

记忆法：LOve HAte yuanze

因为a 链接在浏览器中具有默认样式，所以我们实际工作中都需要给链接单独指定样式。

```html
/* a是标签选择器所有的链接*/
a {
color: gray;
}
/* :hover是链接伪类选择器鼠标经过*/
a:hover {
color: red;
/*鼠标经过的时候，由原来的灰色变成了红色*/
}
```

##### 2.7focus伪类选择器

focus 伪类选择器用于选取获得焦点的表单元素，焦点就是光标；

一般情况<input> 类表单元素才能获取，因此这个选择器也主要针对于表单元素来说。

```html
input:focus {
	background-color:yellow;
}
```

#### 3.css元素显示模式

##### 3.1什么是元素显示模式

元素显示模式就是元素（标签）以什么方式进行显示，比如<div>自己占一行，比如一行可以放多个<span>。

HTML元素一般分为块元素和行内元素两种类型。

##### 3.2块元素

块级元素的特点：

①比较霸道，自己独占一行。

②高度，宽度、外边距以及内边距都可以控制。

③宽度默认是容器（父级宽度）的100%。

④是一个容器及盒子，里面可以放行内或者块级元素。

注意：

-**文字类的元素内不能使用块级元素**

-<p>标签主要用于存放文字，因此<p>里面不能放块级元素，特别是不能放<div>

-同理，<h1>~<h6>等都是文字类块级标签，里面也不能放其他块级元素

##### 3.3行内元素/内联元素

行内元素的特点：

①相邻行内元素在一行上，一行可以显示多个。

②高、宽直接设置是无效的。

③默认宽度就是它本身内容的宽度。

④行内元素只能容纳文本或其他行内元素。

注意：

-链接里面不能再放链接

-特殊情况链接<a> 里面可以放块级元素，但是给<a> 转换一下块级模式最安全

##### 3.4行内块元素

在行内元素中有几个特殊的标签——<img />、<input />、<td>，它们同时具有块元素和行内元素的特点。有些资料称它们为行内块元素。

行内块元素的特点：

①和相邻行内元素（行内块）在一行上，但是他们之间会有空白缝隙。一行可以显示多个（行内元素特点）。

②默认宽度就是它本身内容的宽度（行内元素特点）。

③高度，行高、外边距以及内边距都可以控制（块级元素特点）。

##### 3.5元素显示模式转换

特殊情况下，我们需要元素模式的转换，简单理解: 一个模式的元素需要另外一种模式的特性比如想要增加链接<a> 的触发范围。

```html
<style>
    a {
        width :100px;
        height :100px;
        background-color :red;
        display :block;
    }
</style>
```

-转换为块元素：display:block;

-转换为行内元素：display:inline;

-转换为行内块：display: inline-block;

##### 3.6单行文字垂直居中

解决方法：

让文字的行高等于盒子的高度

![image-20250125213616948](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250125213616948.png)

#### 4.css背景

##### 4.1背景颜色

background-color属性定义了元素的背景颜色。

```html
<style>
    div {
        background-color :颜色/transparent；
    }
</style>
```

一般情况下元素背景颜色默认值是transparent（透明），我们也可以手动指定背景颜色为透明色。

##### 4.2背景图片

背景图片可以添加背景颜色，图片会压住颜色；

```html
<style>
    div {
        background-image :none/url(地址);
    }
</style>
```

none                        无背景图（默认）

url                            使用绝对或相对路径指定背景图像

##### 4.3背景平铺

如果需要在HTML 页面上对背景图像进行平铺，可以使用background-repeat 属性。

```html
background-repeat: repeat | no-repeat | repeat-x | repeat-y
```

![image-20250125221505486](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250125221505486.png)

##### 4.4背景方位

利用background-position 属性可以改变图片在背景中的位置。

```html
background-position: x y;
```

参数代表的意思是：x 坐标和y 坐标。可以使用方位名词或者精确单位

![image-20250125222549213](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250125222549213.png)

![image-20250125230249780](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250125230249780.png)

1.参数是方位名词

如果指定的两个值都是方位名词，则两个值前后顺序无关，比如lefttop和topleft效果一致

如果只指定了一个方位名词，另一个值省略，则第二个值默认居中对齐

2.参数是精确单位

如果参数值是精确坐标，那么第一个肯定是x 坐标，第二个一定是y坐标

如果只指定一个数值，那该数值一定是x坐标，另一个默认垂直居中

3.参数是混合单位

如果指定的两个值是精确单位和方位名词混合使用，则第一个值是x坐标，第二个值是y坐标

##### 4.5背景固定

background-attachment 属性设置背景图像是否固定或者随着页面的其余部分滚动。

background-attachment 后期可以制作视差滚动的效果。

```html
background-attachment : scroll | fixed
```

![image-20250126084726981](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250126084726981.png)

##### 4.6复合写法

background: 背景颜色背景图片地址背景平铺背景图像滚动背景图片位置;

```html
background: transparent url(image.jpg) repeat-y fixed top ;
```

##### 3.7背景颜色半透明

```html
background: rgba(0, 0, 0, 0.3);
```

最后一个参数是alpha 透明度，取值范围在0~1之间

我们习惯把0.3 的0 省略掉，写为background: rgba(0, 0, 0, .3);

注意：背景半透明是指盒子背景半透明，盒子里面的内容不受影响

## 3.css-3

#### 1.css三大特性

CSS 有三个非常重要的三个特性：层叠性、继承性、优先级。

##### 1.1层叠性

相同选择器给设置相同的样式，此时一个样式就会覆盖（层叠）另一个冲突的样式。层叠性主要解决样式冲突的问题

层叠性原则：

样式冲突，遵循的原则是就近原则，哪个样式离结构近，就执行哪个样式

样式不冲突，不会层叠

![image-20250126160222558](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250126160222558.png)

##### 1.2继承性

![image-20250126210656838](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250126210656838.png)

恰当地使用继承可以简化代码，降低CSS样式的复杂性

子元素可以继承父元素的样式（text-，font-，line-这些元素开头的可以继承，以及color属性）

行高的继承性

```html
body {font:12px/1.5 Microsoft YaHei；}
```

行高可以跟单位也可以不跟单位

如果子元素没有设置行高，则会继承父元素的行高为1.5

此时子元素的行高是：当前子元素的文字大小* 1.5

body 行高1.5这样写法最大的优势就是里面子元素可以根据自己文字大小自动调整行高

##### 1.3优先级

![image-20250127232354483](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250127232354483.png)

继承的权重是0，如果该元素没有直接选中，不管父元素权重多高，子元素得到的权重都是0。

权重叠加：如果是复合选择器，则会有权重叠加，需要计算权重。<u>权重会叠加但是不会有进位</u>

**！important>style="">ID选择器>类选择器，伪类选择器>元素选择器**

#### 2.css盒子模型

页面布局要学习三大核心, 盒子模型, 浮动和定位. 学习好盒子模型能非常好的帮助我们布局页面.

##### 2.1盒子模型组成

CSS 盒子模型本质上是一个盒子，封装周围的HTML 元素，它包括：边框、外边距、内边距、和实际内容



![image-20250128233808951](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250128233808951.png)

border：边框

content：内容

padding：内边距 （边框与内容）

margin：外边距 （边框与边框）

##### 2.2边框

```html
border : border-width ||border-style ||border-color
```

![image-20250128235516541](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250128235516541.png)

border-style:

![image-20250128235416425](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250128235416425.png)

边框样式border-style 可以设置如下值：

none：没有边框即忽略所有边框的宽度（默认值）

solid：边框为单实线(最为常用的)

dashed：边框为虚线

dotted：边框为点线

复合写法：

```html
border: 20px solid red;
没有顺序
```

只写边框的一部分：

```html
border-top :20px solid red
border-bottom :
border-left :
border-right :
```

##### 2.3表格的细线边框

border-collapse 属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框。

```html
border-collapse :collapse
```

collapse是合并单元格的边框；

##### 2.4边框会影响盒子的实际大小

1.测量盒子大小的时候,不量边框.

2.如果测量的时候包含了边框,则需要width/height 减去边框宽度

##### 2.5内边框

padding属性用于设置内边距，即边框与内容之间的距离。

盒子大小会随之改变；如果盒子没有width属性，则不会撑开盒子（比如与浏览器页面大小一致）

![image-20250130221625726](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250130221625726.png)

![image-20250130222756486](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250130222756486.png)

顺时针旋转，没有的就复刻对面的

##### 2.6外边距

margin属性用于设置外边距，即控制盒子和盒子之间的距离。

![image-20250130233125046](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250130233125046.png)

简写方式与padding完全一致

外边距可以让块级盒子水平居中，但是必须满足两个条件：

①盒子必须指定了宽度（width）。

②盒子左右的外边距都设置为auto 。

```html
.header { width:960px; margin:0 auto;}
```

常见的写法，以下三种都可以：

margin-left: auto;margin-right: auto;

margin: auto;

margin: 0 auto;

注意：

以上方法是让块级元素水平居中，行内元素或者行内块元素水平居中给其父元素添加text-align:center 即可。

##### 2.7外边距合并

使用margin定义块元素的垂直外边距时，可能会出现外边距的合并。

主要有两种情况:

1.相邻块元素垂直外边距的合并

当上下相邻的两个块元素（兄弟关系）相遇时，如果上面的元素有下外边距margin-bottom，下面的元素有上外边距margin-top，则他们之间的垂直间距不是margin-bottom 与margin-top 之和。取两个值中的较大者这种现象被称为相邻块元素垂直外边距的合并。

![image-20250131234311761](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250131234311761.png)

2.嵌套块元素垂直外边距的塌陷

对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会塌陷较大的外边距值。

![image-20250131234426333](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250131234426333.png)

解决方案：

①可以为父元素定义上边框。

②可以为父元素定义上内边距。

③可以为父元素添加overflow:hidden。

还有其他方法，比如浮动、固定，绝对定位的盒子不会有塌陷问题，后面咱们再总结。

##### 2.8清除内外边距

网页元素很多都带有默认的内外边距，而且不同浏览器默认的也不一致。因此我们在布局前，首先要清除下网页元素的内外边距。

```html
* {
padding:0;
/*清除内边距*/
margin:0;
/*清除外边距*/
}
```

注意：行内元素为了照顾兼容性，尽量只设置左右内外边距，不要设置上下内外边距。但是转换为块级和行内块元素就可以了

#### 3.css3新增

##### 3.1圆角边框

border-radius 属性用于设置元素的外边框圆角。

```html
border-radius:length;
```

参数值可以为数值或百分比的形式

如果是正方形，想要设置为一个圆，把数值修改为高度或者宽度的一半即可，或者直接写为50%

该属性是一个简写属性，可以跟四个值，分别代表左上角、右上角、右下角、左下角

分开写：border-top-left-radius、border-top-right-radius、border-bottom-right-radius 和border-bottom-left-radius

如果只有两个数值，那分别为主对角线和副对角线；

##### 3.2盒子阴影

CSS3 中新增了盒子阴影，我们可以使用box-shadow属性为盒子添加阴影。

```html
box-shadow:h-shadow v-shadow blur(虚实) spread color inset;
```

```html
box-shadow: 10px 10px 10px 10px rgba(0,0,0, .3);
```

![image-20250202000128877](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250202000128877.png)-默认的是**外阴影(outset)**, 但是不可以写这个单词,否则造成阴影无效

-盒子阴影不占用空间，不会影响其他盒子排列。

##### 3.3文字阴影

在CSS3 中，我们可以使用text-shadow 属性将阴影应用于文本。

```html
text-shadow: h-shadow v-shadow blur color;
```

![image-20250202001454893](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250202001454893.png)

#### 4.ps基本操作

因为网页美工大部分效果图都是利用PS（Photoshop）来做的，所以以后我们大部分切图工作都是在PS里面完成。

文件->打开：可以打开我们要测量的图片

Ctrl+R：可以打开标尺，或者视图->标尺

右击标尺，把里面的单位改为像素

Ctrl+ 加号(+)可以放大视图，Ctrl+ 减号(-)可以缩小视图

按住空格键，鼠标可以变成小手，拖动PS 视图

用选区拖动 可以测量大小

Ctrl+ D可以取消选区，或者在旁边空白处点击一下也可以取消选区

![image-20250131235936437](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250131235936437.png)

## 4.css-4

#### 1.浮动

##### 1.1 传统网页布局的三种方式

网页布局的本质——用CSS 来摆放盒子。把盒子摆放到相应位置.

CSS 提供了三种传统布局方式(简单说,就是盒子如何进行排列顺序)：普通流（标准流），浮动，定位

这三种布局方式都是用来摆放盒子的，盒子摆放到合适位置，布局自然就完成了。

**注意**：实际开发中，一个页面基本都包含了这三种布局方式（后面移动端学习新的布局方式）。

##### 1.2 标准流（普通流/文档流）

所谓的标准流: 就是标签按照规定好默认方式排列.

--块级元素会独占一行，从上向下顺序排列。

常用元素：div、hr、p、h1~h6、ul、ol、dl、form、table

--行内元素会按照顺序，从左到右顺序排列，碰到父元素边缘则自动换行。

常用元素：span、a、i、em等

以上都是标准流布局，我们前面学习的就是标准流，标准流是最基本的布局方式。

##### 1.3浮动简单介绍

浮动最典型的应用：可以让多个块级元素一行内排列显示。

**网页布局第一准则**：多个块级元素纵向排列找标准流，多个块级元素横向排列找浮动。

##### 1.4浮动格式

float属性用于创建浮动框，将其移动到一边，直到左边缘或右边缘触及包含块或另一个浮动框的边缘。

```html
选择器 { float :属性值; }
```

![image-20250202003950289](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250202003950289.png)

##### 1.5浮动特性

1.浮动元素会脱离标准流(脱标)

--脱离标准普通流的控制（浮）移动到指定位置（动）, （俗称脱标）

--浮动的盒子不再保留原先的位置

2.浮动的元素会一行内显示并且元素顶部对齐

![image-20250203011609637](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250203011609637.png)

-- 如果多个盒子都设置了浮动，则它们会按照属性值一行内显示并且顶端对齐排列。

--浮动的元素是互相贴靠在一起的（不会有缝隙），如果父级宽度装不下这些浮动的盒子，多出的盒子会另起一行对齐。

3.浮动的元素会具有行内块元素的特性.

--任何元素都可以浮动。不管原先是什么模式的元素，添加浮动之后具有行内块元素相似的特性。

如果块级盒子没有设置宽度，默认宽度和父级一样宽，但是**添加浮动后，它的大小根据内容来决定**

浮动的盒子中间是没有缝隙的，是紧挨着一起的

行内元素同理

##### 1.6搭配

为了约束浮动元素位置, 我们网页布局一般采取的策略是:

先用标准流的父元素排列上下位置, 之后内部子元素采取浮动排列左右位置. 符合网页布局第一准则.

![image-20250204004611282](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250204004611282.png)

#### 2.常见网页布局

##### 2.1常见布局

![image-20250204235712655](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250204235712655.png)

![image-20250204235731677](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250204235731677.png)

##### 2.2注意点

--浮动和标准流的父盒子搭配。

先用标准流的父元素排列上下位置, 之后内部子元素采取浮动排列左右位置

--一个元素浮动了，理论上其余的兄弟元素也要浮动。

一个盒子里面有多个子盒子，如果其中一个盒子浮动了，那么其他兄弟也应该浮动，以防止引起问题。浮动的盒子只会影响浮动盒子后面的标准流,不会影响前面的标准流.

#### 3.清除浮动

##### 3.1清除浮动本质

![image-20250205230234623](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250205230234623.png)

-清除浮动的本质是清除浮动元素造成的影响

-如果父盒子本身有高度，则不需要清除浮动

-清除浮动之后，父级就会根据浮动的子盒子自动检测高度。父级有了高度，就不会影响下面的标准流了

##### 3.2清除浮动

```html
选择器 {clear: 属性值; }
```

![image-20250205164149859](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250205164149859.png)

我们实际工作中，几乎只用clear: both;

清除浮动的策略是: **闭合浮动**.

##### 3.3清除浮动方法

1.额外标签法也称为隔墙法，是W3C推荐的做法。

额外标签法会在浮动元素末尾添加一个空的标签。例如<div style="clear:both"></div>，或者其他标签（如 br/ 等）。

注意：要求这个新的空标签必须是**块级**元素。

2.父级添加overflow属性

可以给父级添加overflow属性，将其属性值设置为hidden、auto或scroll。

3.父级添加after伪元素

:after 方式是额外标签法的升级版。也是给父元素添加

```html
.clearfix:after
{
    content: "";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}
.clearfix {
	/* IE6、7专有 */
	*zoom: 1;
}
```

4.父级添加双伪元素

```html
.clearfix:before,.clearfix:after
{
	content:"";
	display:table;
}
.clearfix:after
{
	clear:both;
}
.clearfix
{
	*zoom:1;
}
```

##### 3.4总结

为什么需要清除浮动？

①父级没高度。

②子盒子浮动了。

③影响下面布局了，我们就应该清除浮动了。

![image-20250205233617452](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250205233617452.png)

## 5.css-5

#### 1.PS切图

##### 1.1常见的图片格式

--jpg图像格式：JPEG（.JPG）对色彩的信息保留较好，高清，颜色较多，我们产品类的图片经常用jpg格式的

--gif图像格式：GIF格式最多只能储存256色，所以通常用来显示简单图形及字体，但是可以保存透明背景和动画效果, 实际经常用于一些图片小动画效果.

--png图像格式是一种新兴的网络图形格式，结合了GIF和JPEG的优点，具有存储形式丰富的特点，能够保持透明背景. 如果想要切成背景透明的图片,请选择png格式.

--PSD图像格式PSD格式是Photoshop的专用格式，里面可以存放图层、通道、遮罩等多种设计稿. 对我们前端人员来说,最大的优点,我们可以直接从上面复制文字,获得图片,还可以测量大小和距离.

##### 1.2图层切图

最简单的切图方式：

右击图层->快速导出为PNG。

但是很多情况下,我们需要合并图层再导出:

1.选中需要的图层:图层菜单->合并图层(ctrl+e)

2.右击->快速导出为PNG

##### 1.3切片切图

--利用切片工具手动划出

--文件菜单—导出—存储为web设备所用格式—选择我们要的图片格式—存储（切片改为选中的切片）

#### 2学成在线案例

##### 2.1案例准备工作

采取结构与样式相分离思想：

1. 创建study 目录文件夹(用于存放我们这个页面的相关内容)。
2. 用vscode打开study目录文件夹.
3. study目录内新建images 文件夹，用于保存图片。
4. 新建首页文件index.html（以后我们的网站首页统一规定为index.html)。
5. 新建style.css 样式文件。我们本次采用外链样式表。
6. 将样式引入到我们的HTML页面文件中。
7. 样式表写入清除内外边距的样式，来检测样式表是否引入成功。

##### 2.2CSS 属性书写顺序

1. 布局定位属性：display / position / float / clear / visibility / overflow（建议display 第一个写，毕竟关系到模式）
2. 自身属性：width / height / margin / padding / border / background
3. 文本属性：color / font / text-decoration / text-align / vertical-align / white-space / break-word
4. 其他属性（CSS3）：content / cursor / border-radius / box-shadow / text-shadow / background:linear-gradient

```html
.jdc {
    display: block;
    position: relative;
    float: left;
    width: 100px;
    height: 100px;
    margin: 0 10px;
    padding: 20px 0;
    font-family: Arial, 'Helvetica Neue', Helvetica, sans-serif;
    color: #333;
    background: rgba(0,0,0,.5);
    border-radius: 10px;
}
```

##### 2.3页面布局整体思路

为了提高网页制作的效率，布局时通常有以下的整体思路：

1.必须确定页面的版心（可视区），我们测量可得知。

2.分析页面中的行模块，以及每个行模块中的列模块。其实页面布局第一准则.

3.一行中的列模块经常浮动布局, 先确定每个列的大小,之后确定列的位置. 页面布局第二准则

4.制作HTML结构。我们还是遵循，先有结构，后有样式的原则。结构永远最重要.

5.所以,先理清楚布局结构,再写代码尤为重要. 这需要我们多写多积累.

## 6.css-6

#### 1.定位

##### 1.1简单介绍

1.浮动可以让多个块级盒子一行没有缝隙排列显示，经常用于横向排列盒子。

2.定位则是可以让盒子自由的在某个盒子内移动位置或者固定屏幕中某个位置，并且可以压住其他盒子。

##### 1.2定位组成

定位：将盒子定在某一个位置，所以定位也是在摆放盒子，按照定位的方式移动盒子。

定位= 定位模式+ 边偏移。

--定位模式决定元素的定位方式，它通过CSS 的position属性来设置，其值可以分为四个：

![image-20250206202316984](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250206202316984.png)

--边偏移就是定位的盒子移动到最终位置。有top、bottom、left 和right4 个属性。

![image-20250206202358014](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250206202358014.png)

##### 1.3 静态定位static

静态定位是元素的默认定位方式，无定位的意思。

```html
选择器 {position: static; }
```

##### 1.4相对定位relative

相对定位是元素在移动位置的时候，是相对于它原来的位置来说的。

```html
选择器 {position: relative; }
```

相对定位的**特点**：

1.它是相对于自己原来的位置来移动的（移动位置的时候参照点是自己原来的位置）。

2.原来在标准流的位置继续占有，后面的盒子仍然以标准流的方式对待它。因此，相对定位并没有脱标。它最典型的应用是给绝对定位当爹的。

##### 1.5绝对定位absolute

绝对定位是元素在移动位置的时候，是相对于它祖先元素来说的

```html
选择器 {position: absolute; }
```

绝对定位的特点：

1.如果没有祖先元素或者祖先元素没有定位，则以浏览器为准定位（Document 文档）。

2.如果祖先元素有定位（相对、绝对、固定定位），则以**最近一级的有定位祖先元素**为参考点移动位置。

3.绝对定位不再占有原先的位置，比浮动还要高。（脱标）

##### 1.6子绝父相

①子级绝对定位，不会占有位置，可以放到父盒子里面的任何一个地方，不会影响其他的兄弟盒子。

②父盒子需要加定位限制子盒子在父盒子内显示。

③父盒子布局时，需要占有位置，因此父亲只能是相对定位。

这就是子绝父相的由来，所以相对定位经常用来作为绝对定位的父级。

总结：因为父级需要占有位置，因此是相对定位，子盒子不需要占有位置，则是绝对定位；当然，子绝父相不是永远不变的，如果父元素不需要占有位置，子绝父绝也会遇到。

##### 1.7固定定位

固定定位是元素固定于浏览器可视区的位置。

主要使用场景：可以在浏览器页面滚动时元素的位置不会改变。

```html
选择器 {position: fixed; }
```

固定定位的特点：

1.以浏览器的可视窗口为参照点移动元素。

跟父元素没有任何关系

不随滚动条滚动。

2.固定定位不在占有原先的位置。

固定定位也是脱标的，其实固定定位也可以看做是一种特殊的绝对定位。

**固定定位小技巧： 固定在版心右侧位置。**

1.让固定定位的盒子left: 50%. 走到浏览器可视区（也可以看做版心）的一半位置。

2.让固定定位的盒子margin-left: 版心宽度的一半距离。多走版心宽度的一半位置就可以让固定定位的盒子贴着版心右侧对齐了。

##### 1.8 粘性定位sticky

粘性定位可以被认为是相对定位和固定定位的混合。

```html
选择器 {position: sticky; top: 10px; }
当距离上边缘为10px时不再随滚动而变化
```

粘性定位的特点：

1.以浏览器的可视窗口为参照点移动元素（固定定位特点）

2.粘性定位占有原先的位置（相对定位特点）

3.必须添加top 、left、right、bottom 其中一个才有效跟页面滚动搭配使用。

兼容性较差，IE 不支持。

##### 1.9总结

![image-20250207222209227](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250207222209227.png)

##### 1.10定位叠放次序

在使用定位布局时，可能会出现盒子重叠的情况。此时，可以使用z-index来控制盒子的前后次序(z轴)

```html
选择器 {z-index: 1; }
```

数值可以是正整数、负整数或0, 默认是auto，数值越大，盒子越靠上

如果属性值相同，则按照书写顺序，后来居上

数字后面不能加单位

只有定位的盒子才有z-index 属性

##### 1.11定位的拓展

###### -1绝对定位的盒子居中

加了绝对定位的盒子不能通过margin:0 auto 水平居中，但是可以通过以下计算方法实现水平和垂直居中。

①left: 50%;：让盒子的左侧移动到父级元素的水平中心位置。

②margin-left: -100px;：让盒子向左移动自身宽度的一半。

###### -2定位特殊特性

绝对定位和固定定位也和浮动类似。

1.行内元素添加绝对或者固定定位，可以直接设置高度和宽度。

2.块级元素添加绝对或者固定定位，如果不给宽度或者高度，默认大小是内容的大小。

###### -3脱标的盒子不会触发外边距塌陷

浮动元素、绝对定位(固定定位）元素的都不会触发外边距合并的问题。

###### -4绝对定位（固定定位）会完全压住盒子

浮动元素不同，只会压住它下面标准流的盒子，但是不会压住下面标准流盒子里面的文字（图片）但是绝对定位（固定定位）会压住下面标准流所有的内容。

浮动之所以不会压住文字，因为浮动产生的目的最初是为了做文字环绕效果的。文字会围绕浮动元素

#### 2.网页布局总结

通过盒子模型，清楚知道大部分html标签是一个盒子。

通过CSS浮动、定位可以让每个盒子排列成为网页。

一个完整的网页，是标准流、浮动、定位一起完成布局的，每个都有自己的专门用法。

1.标准流

可以让盒子上下排列或者左右排列，垂直的块级盒子显示就用标准流布局。

2.浮动

可以让多个块级元素一行显示或者左右对齐盒子，多个块级盒子水平显示就用浮动布局。

3.定位

定位最大的特点是有层叠的概念，就是可以让多个盒子前后叠压来显示。如果元素自由在某个盒子内移动就用定位布局。

#### 3.元素的显示与隐藏(重要)

本质：让一个元素在页面中隐藏或者显示出来。

##### 3.1display 属性

display 属性用于设置一个元素应如何显示。

display: none；->隐藏对象

display：block；->除了转换为块级元素之外，同时还有显示元素的意思

display 隐藏元素后，不再占有原来的位置。

后面应用及其广泛，搭配JS 可以做很多的网页特效。

##### 3.2visibility 可见性

visibility属性用于指定一个元素应可见还是隐藏。

visibility：visible ;元素可视

visibility：hidden; 元素隐藏

visibility 隐藏元素后，继续占有原来的位置。

如果隐藏元素想要原来位置，就用visibility：hidden

如果隐藏元素不想要原来位置，就用display：none (用处更多重点）

##### 3.3overflow 溢出

overflow属性指定了如果内容溢出一个元素的框（超过其指定高度及宽度）时，会发生什么。

![image-20250208181730118](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250208181730118.png)

一般情况下，我们都不想让溢出的内容显示出来，因为溢出的部分会影响布局。

但是如果有定位的盒子，请慎用overflow:hidden 因为它会隐藏多余的部分。

##### 3.4总结

1.display 显示隐藏元素但是不保留位置

2.visibility 显示隐藏元素 但是保留原来的位置

3.overflow 溢出显示隐藏 但是只是对于溢出的部分处理

## 7.css-7

#### 1精灵图

##### 1.1为什么需要精灵图

因此，为了有效地减少服务器接收和发送请求的次数，提高页面的加载速度，出现了CSS精灵技术（也称CSS Sprites、CSS雪碧）。

核心原理：将网页中的一些小背景图像整合到一张大图中，这样服务器只需要一次请求就可以了。

##### 1.2精灵图使用

使用精灵图核心：

1.精灵技术主要针对于背景图片使用。就是把多个小背景图片整合到一张大图片中。

2.这个大图片也称为sprites 精灵图 或者雪碧图

3.移动背景图片位置，此时可以使用background-position 。

4.移动的距离就是这个目标图片的x和y坐标。注意网页中的坐标有所不同

5.因为一般情况下都是往上往左移动，所以数值是负值。

6.使用精灵图的时候需要精确测量，每个小背景图片的大小和位置。

#### 2.字体图标

##### 2.1字体图标的产生

字体图标使用场景： 主要用于显示网页中通用、常用的一些小图标。

此时，有一种技术的出现很好的解决了以上问题，就是字体图标iconfont。

字体图标可以为前端工程师提供一种方便高效的图标使用方式，展示的是图标，本质属于字体。

##### 2.2字体图标的优点

轻量级：一个图标字体要比一系列的图像要小。一旦字体加载了，图标就会马上渲染出来，减少了服务器请求

灵活性：本质其实是文字，可以很随意的改变颜色、产生阴影、透明效果、旋转等

兼容性：几乎支持所有的浏览器，请放心使用

注意：字体图标不能替代精灵技术，只是对工作中图标部分技术的提升和优化。

总结：

1.如果遇到一些结构和样式比较简单的小图标，就用字体图标。

![image-20250209210003788](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209210003788.png)

2.如果遇到一些结构和样式复杂一点的小图片，就用精灵图。

##### 2.3字体图标的下载

—icomoon字库[http://icomoon.io](http://icomoon.io)推荐指数★★★★★IcoMoon成立于2011年，推出了第一个自定义图标字体生成器，它允许用户选择所需要的图标，使它们成一字型。该字库内容种类繁多，非常全面，唯一的遗憾是国外服务器，打开网速较慢。

—阿里iconfont字库http://www.iconfont.cn/推荐指数★★★★★这个是阿里妈妈M2UX的一个iconfont字体图标字库，包含了淘宝图标库和阿里妈妈图标库。可以使用AI制作图标上传生成。

##### 2.4字体图标的引入

*下载完毕之后，注意原先的文件不要删，后面会用。*

1. 把下载包里面的fonts文件夹放入页面根目录下![image-20250209213047756](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209213047756.png)

2.在CSS 样式中全局声明字体：简单理解把这些字体文件通过css引入到我们页面中。一定注意字体文件路径的问题。

```html
@font-face {
        font-family: 'icomoon';
        src:
        url('fonts/icomoon.eot?7kkyc2');
        src:url('fonts/icomoon.eot?7kkyc2#iefix') format('embedded-opentype'),
        url('fonts/icomoon.ttf?7kkyc2') format('truetype'),
        url('fonts/icomoon.woff?7kkyc2') format('woff'),
        url('fonts/icomoon.svg?7kkyc2#icomoon') format('svg');
        font-weight: normal;
        font-style: normal;
}

```

3. html 标签内添加小图标。

   ![image-20250209213219662](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209213219662.png)

4.给标签定义字体。

```html
span {
	font-family: "icomoon";
}
```

![image-20250209213314474](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209213314474.png)

##### 2.5字体图标的追加

如果工作中，原来的字体图标不够用了，我们需要添加新的字体图标到原来的字体文件中。把压缩包里面的selection.json 从新上传，然后选中自己想要新的图标，从新下载压缩包，并替换原来的文件即可。

![image-20250209224116569](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209224116569.png)

#### 3.css三角

网页中常见一些三角形，使用CSS 直接画出来就可以，不必做成图片或者字体图标。

```html
div {
    width: 0;
    height: 0;
    line-height: 0;
    font-size: 0;
    border: 50px solid transparent;
    border-left-color: pink;
}
```

#### 4.css用户界面样式

##### 4.1鼠标样式cursor

```html
li {cursor: pointer; }
```

设置或检索在对象上移动的鼠标指针采用何种系统预定义的光标形状。

![image-20250209233340154](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209233340154.png)

##### 4.2轮廓线outline

给表单添加outline: 0;或者 outline: none; 样式之后，就可以去掉默认的蓝色边框。

```html
input {outline: none; }
```

##### 4.3防止拖拽文本域resize

实际开发中，我们文本域右下角是不可以拖拽的。

```html
textarea{ resize: none;}
```

#### 5.vertical-align 属性应用

CSS 的vertical-align 属性使用场景：经常用于设置图片或者表单(行内块元素）和文字垂直对齐。

官方解释：用于设置一个元素的垂直对齐方式，但是它只针对于行内元素或者行内块元素有效。

```html
vertical-align : baseline | top | middle | bottom
```

![image-20250209234727357](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209234727357.png)

![image-20250209234755205](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250209234755205.png)

##### 5.1图片、表单和文字对齐

图片、表单都属于行内块元素，默认的vertical-align 是基线对齐。

此时可以给图片、表单这些行内块元素的vertical-align属性设置为middle就可以让文字和图片垂直居中对齐了。

##### 5.2解决图片底部默认空白缝隙问题

bug：图片底侧会有一个空白缝隙，原因是行内块元素会和文字的基线对齐。

主要解决方法有两种：

1.给图片添加vertical-align:middle | top| bottom等。（提倡使用的）

2.把图片转换为块级元素 display: block;

#### 6.溢出的文字省略号显示

##### 6.1单行文本溢出显示省略号

```html
/*1.先强制一行内显示文本*/
white-space: nowrap;
（默认normal自动换行）
/*2.超出的部分隐藏*/
overflow: hidden;
/*3.文字用省略号替代超出的部分*/
text-overflow: ellipsis;
```

##### 6.2多行文本溢出显示省略号

多行文本溢出显示省略号，有较大兼容性问题，适合于webKit浏览器或移动端（移动端大部分是webkit内核）

```html
overflow:hidden;
text-overflow:ellipsis;
/*弹性伸缩盒子模型显示*/
display:-webkit-box;
/*限制在一个块元素显示的文本的行数*/
-webkit-line-clamp:2;
/*设置或检索伸缩盒对象的子元素的排列方式*/
-webkit-box-orient:vertical;
```

*更推荐让后台人员来做这个效果，因为后台人员可以设置显示多少个字，操作更简单。*

#### 7.常见布局技巧

##### 7.1margin负值运用

![image-20250210181005571](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250210181005571.png)

1.让每个盒子margin往左侧移动-1px正好压住相邻盒子边框

2.鼠标经过某个盒子的时候，提高当前盒子的层级即可（如果没有定位，则加相对定位（保留位置），如果有定位，则加z-index）

##### 7.2文字围绕浮动元素

巧妙运用浮动元素不会压住文字的特性

##### 7.3行内块巧妙运用

![image-20250210181149160](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250210181149160.png)

页码在页面中间显示:

1.把这些链接盒子转换为行内块，之后给父级指定text-align:center;

2.利用行内块元素中间有缝隙，并且给父级添加text-align:center;行内块元素会水平会居中

##### 7.4CSS 三角强化

小三角用<i> </i>

![image-20250210192118701](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250210192118701.png)

```html
width: 0;
height: 0;
border-color: transparent red transparent transparent;
border-style: solid;
border-width: 22px 8px 0 0;
```

#### 8.CSS 初始化

简单理解：CSS初始化是指重设浏览器的样式。(也称为CSS reset）

每个网页都必须首先进行CSS初始化。

这里我们以京东CSS初始化代码为例。

Unicode编码字体：

把中文字体的名称用相应的Unicode编码来代替，这样就可以有效的避免浏览器解释CSS代码时候出现乱码的问题。

比如：

黑体\9ED1\4F53

宋体\5B8B\4F53

微软雅黑\5FAE\8F6F\96C5\9ED1


