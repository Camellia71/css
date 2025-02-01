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

#### 5.css三大特性

CSS 有三个非常重要的三个特性：层叠性、继承性、优先级。

##### 5.1层叠性

相同选择器给设置相同的样式，此时一个样式就会覆盖（层叠）另一个冲突的样式。层叠性主要解决样式冲突的问题

层叠性原则：

样式冲突，遵循的原则是就近原则，哪个样式离结构近，就执行哪个样式

样式不冲突，不会层叠

![image-20250126160222558](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250126160222558.png)

##### 5.2继承性

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

##### 5.3优先级

![image-20250127232354483](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250127232354483.png)

继承的权重是0，如果该元素没有直接选中，不管父元素权重多高，子元素得到的权重都是0。

权重叠加：如果是复合选择器，则会有权重叠加，需要计算权重。<u>权重会叠加但是不会有进位</u>

**！important>style="">ID选择器>类选择器，伪类选择器>元素选择器**

#### 6.css盒子模型

页面布局要学习三大核心, 盒子模型, 浮动和定位. 学习好盒子模型能非常好的帮助我们布局页面.

##### 6.1盒子模型组成

CSS 盒子模型本质上是一个盒子，封装周围的HTML 元素，它包括：边框、外边距、内边距、和实际内容



![image-20250128233808951](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250128233808951.png)

border：边框

content：内容

padding：内边距 （边框与内容）

margin：外边距 （边框与边框）

##### 6.2边框

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

##### 6.3表格的细线边框

border-collapse 属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框。

```html
border-collapse :collapse
```

collapse是合并单元格的边框；

##### 6.4边框会影响盒子的实际大小

1.测量盒子大小的时候,不量边框.

2.如果测量的时候包含了边框,则需要width/height 减去边框宽度

##### 6.5内边框

padding属性用于设置内边距，即边框与内容之间的距离。

盒子大小会随之改变；如果盒子没有width属性，则不会撑开盒子（比如与浏览器页面大小一致）

![image-20250130221625726](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250130221625726.png)

![image-20250130222756486](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250130222756486.png)

顺时针旋转，没有的就复刻对面的

##### 6.6外边距

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

##### 6.7外边距合并

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

##### 6.8清除内外边距

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

#### 7.ps基本操作

因为网页美工大部分效果图都是利用PS（Photoshop）来做的，所以以后我们大部分切图工作都是在PS里面完成。

文件->打开：可以打开我们要测量的图片

Ctrl+R：可以打开标尺，或者视图->标尺

右击标尺，把里面的单位改为像素

Ctrl+ 加号(+)可以放大视图，Ctrl+ 减号(-)可以缩小视图

按住空格键，鼠标可以变成小手，拖动PS 视图

用选区拖动 可以测量大小

Ctrl+ D可以取消选区，或者在旁边空白处点击一下也可以取消选区

![image-20250131235936437](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20250131235936437.png)

