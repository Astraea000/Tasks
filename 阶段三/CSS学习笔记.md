# 关于CSS的学习

前言：有关CSS的部分我将从css是什么与写在哪，css语法，文字样式，背景与边框，盒子模型，简单布局，常见选择器，导航栏八个方面展开学习。

## 一、css是什么与写在哪里

css是什么：css是给HTML化妆的，HTML提供骨架，css提供皮肤

css写在哪里：可以写在HTML里面，可以写在单独文件，也可以写在标签里面

## 二 、css语法

选择器 {  

​    属性:   值;

 }

很简单的三部分，选择器=要改谁，属性=要改什么，值=改成什么样

注意：CSS注释以 **/\*** 开始, 以 ***/** 结束，这个和HTML有所不同

## 三、文字样式

1. 文本颜色

   颜色是css最常见的指定

   - 十六进制值 - 如: **＃FF0000**
   - 一个RGB值 - 如: **RGB(255,0,0)**
   - 颜色的名称 - 如: **red**

   一个网页的背景颜色是指在主体内的选择：

   `body {color:red;} `

   `h1 {color:#00ff00;} `

   `h2 {color:rgb(255,0,0);}`

2. 文本的对齐方式

   文本排列属性是用来设置文本的水平对齐方式。

   文本可居中或对齐到左或右,两端对齐.

   当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。

   `h1 {text-align:center;} `

   `p.date {text-align:right;} `

   `p.main {text-align:justify;}`

3. 文本修饰

   text-decoration 属性用来设置或删除文本的装饰。

   从设计的角度看 text-decoration属性主要是用来删除链接的下划线：

   `a {text-decoration:none;}`

   也可以这样装饰文字：

   `h1 {text-decoration:overline;}` 

   `h2 {text-decoration:line-through;}` 

   `h3 {text-decoration:underline;}`

4. 文本转换

   文本转换属性是用来指定在一个文本中的大写和小写字母。

   可用于所有字句变成大写或小写字母，或每个单词的首字母大写。

   `p.uppercase {text-transform:uppercase;}` 

   `p.lowercase {text-transform:lowercase;}` 

   `p.capitalize {text-transform:capitalize;}`

5. 文本缩进

   文本缩进属性是用来指定文本的第一行的缩进。

   `p {text-indent:50px;}`

| 属性                | 描述                     |
| :------------------ | :----------------------- |
| `<color>`           | 设置文本颜色             |
| `<direction>`       | 设置文本方向。           |
| `<letter-spacing>`  | 设置字符间距             |
| `<line-height>`     | 设置行高                 |
| `<text-align>`      | 对齐元素中的文本         |
| `<text-decoration>` | 向文本添加修饰           |
| `<text-indent>`     | 缩进元素中文本的首行     |
| `<text-shadow>`     | 设置文本阴影             |
| `<text-tranform>`   | 控制元素中的字母         |
| `<unicode-bidi>`    | 设置或返回文本是否被重写 |
| `<vertical-align>`  | 设置元素的垂直对齐       |
| `<white-space>`     | 设置元素中空白的处理方式 |
| `<word-spacing>`    | 设置字间距               |

6. 字型

   在CSS中，有两种类型的字体系列名称：

   - **通用字体系列** - 拥有相似外观的字体系统组合（如 "Serif" 或 "Monospace"）
   - **特定字体系列** - 一个特定的字体系列（如 "Times" 或 "Courier"）

   

   font-family 属性设置文本的字体系列。

   font-family 属性应该设置几个字体名称作为一种"后备"机制，如果浏览器不支持第一种字体，他将尝试下一种字体。

   **注意**: 如果字体系列的名称超过一个字，它必须用引号，如Font Family："宋体"。

   多个字体系列是用一个逗号分隔指明：

   `p{font-family:"Times New Roman", Times, serif;}`

   字体样式：

   主要是用于指定斜体文字的字体样式属性。

   这个属性有三个值：

   - 正常 - 正常显示文本
   - 斜体 - 以斜体字显示的文字
   - 倾斜的文字 - 文字向一边倾斜（和斜体非常类似，但不太支持）

   `p.normal {font-style:normal;}`
   `p.italic {font-style:italic;}`
   `p.oblique {font-style:oblique;}`

   字体大小：

   font-size 属性设置文本的大小。

   能否管理文字的大小，在网页设计中是非常重要的。但是，你不能通过调整字体大小使段落看上去像标题，或者使标题看上去像段落。

   请务必使用正确的HTML标签，就`<h1> - <h6>`表示标题和`<p>`表示段落：

   字体大小的值可以是绝对或相对的大小。

   绝对大小：

   - 设置一个指定大小的文本
   - 不允许用户在所有浏览器中改变文本大小
   - 确定了输出的物理尺寸时绝对大小很有用

   相对大小：

   - 相对于周围的元素来设置大小
   - 允许用户在浏览器中改变文字大小

   设置文字的大小与像素，让您完全控制文字大小：

   `h1 {font-size:40px;}`
   `h2 {font-size:30px;}`
   `p {font-size:14px;}

   

   或者用em来设置字体大小：

   为了避免Internet Explorer 中无法调整文本的问题，许多开发者使用 em 单位代替像素。

   em的尺寸单位由W3C建议。

   1em和当前字体大小相等。在浏览器中默认的文字大小是16px。

   因此，1em的默认大小是16px。可以通过下面这个公式将像素转换为em：**px/16=em**

   `h1 {font-size:2.5em;} /* 40px/16=2.5em */
   h2 {font-size:1.875em;} /* 30px/16=1.875em */
   p {font-size:0.875em;} /* 14px/16=0.875em */`

   在上面的例子，em的文字大小是与前面的例子中像素一样。不过，如果使用 em 单位，则可以在所有浏览器中调整文本大小。

   最后也可以使用百分比和em的组合：

   在所有浏览器的解决方案中，设置 `<body>`元素的默认字体大小的是百分比：

   `body {font-size:100%;}`
   `h1 {font-size:2.5em;}`
   `h2 {font-size:1.875em;}`
   `p {font-size:0.875em;}`

| Property         | 描述                                 |
| :--------------- | :----------------------------------- |
| `<font>`         | 在一个声明中设置所有的字体属性       |
| `<font-famaily>` | 指定文本的字体系列                   |
| `<font-size>`    | 指定文本的字体大小                   |
| `<font-style>`   | 指定文本的字体样式                   |
| `<font-variant>` | 以小型大写字体或者正常字体显示文本。 |
| `<font-weight>`  | 指定字体的粗细。                     |

## 四、背景与边框

1. 背景

   CSS 背景属性用于定义HTML元素的背景。

   CSS 属性定义背景效果:

   - background-color
   - background-image
   - background-repeat
   - background-attachment
   - background-position

   background-color 属性定义了元素的背景颜色.

   页面的背景颜色使用在body的选择器中:

   `body {background-color:#b0c4de;}`

   CSS中，颜色值通常以以下方式定义:

   - 十六进制 - 如："#ff0000"
   - RGB - 如："rgb(255,0,0)"
   - 颜色名称 - 如："red"

   以下实例中, h1, p, 和 div 元素拥有不同的背景颜色:

   `h1 {background-color:#6495ed;}`
   `p {background-color:#e0ffff;}`
   `div {background-color:#b0c4de;}`

   background-image 属性描述了元素的背景图像.

   默认情况下，背景图像进行平铺重复显示，以覆盖整个元素实体.

   页面背景图片设置实例:

   `body {background-image:url('paper.gif');}`

   默认情况下 background-image 属性会在页面的水平或者垂直方向平铺。

   一些图像如果在水平方向与垂直方向平铺，这样看起来很不协调，如下所示: 

   `body`
   `{`
   `background-image:url('gradient2.png');`
   `}`

   如果图像只在水平方向平铺 (repeat-x), 页面背景会更好些:

   `body`
   `{`
   `background-image:url('gradient2.png');`
   `background-repeat:repeat-x;`
   `}`

   如果你不想让图像平铺，你可以使用 background-repeat 属性:

   `body`
   `{`
   `background-image:url('img_tree.png');`
   `background-repeat:no-repeat;`
   `}`

   以上实例中，背景图像与文本显示在同一个位置，为了让页面排版更加合理，不影响文本的阅读，我们可以改变图像的位置。

   可以利用 background-position 属性改变图像在背景中的位置:

   `body`
   `{`
   `background-image:url('img_tree.png');`
   `background-repeat:no-repeat;`
   `background-position:right top;`
   `}`

   在以上实例中我们可以看到页面的背景颜色通过了很多的属性来控制。

   为了简化这些属性的代码，我们可以将这些属性合并在同一个属性中.

   背景颜色的简写属性为 "background":

   `body {background:#ffffff url('img_tree.png') no-repeat right top;}`

   当使用简写属性时，属性值的顺序为：:

   - background-color
   - background-image
   - background-repeat
   - background-attachment
   - background-position

   以上属性无需全部使用，你可以按照页面的实际需要使用

2. 边框

   CSS 边框（Border）是用于定义元素边框样式的属性。

   边框可以应用于任何 HTML 元素，用于增强视觉效果、分隔内容或突出显示元素。

   CSS 边框属性主要包括边框宽度、边框样式、边框颜色以及简写属性。

   边框样式属性指定要显示什么样的边界。

   **border-style** 属性用于指定要显示的边框类型。

   允许的值如下：

   - dotted：定义点状边框。
   - dashed：定义虚线边框。
   - solid：定义实线边框。
   - double：定义双线边框。
   - groove：定义三维沟槽边框。效果取决于 border-color 的值。
   - ridge：定义三维脊状边框。效果取决于 border-color 的值。
   - inset：定义三维嵌入边框。效果取决于 border-color 的值。
   - outset：定义三维突出边框。效果取决于 border-color 的值。
   - none：定义无边框。
   - hidden：定义隐藏边框。

   为边框指定宽度有两种方法：可以指定长度值，比如 2px 或 0.1em(单位为 px, pt, cm, em 等)，或者使用 3 个关键字之一，它们分别是 thick 、medium（默认值） 和 thin。

   **注意：**CSS 没有定义 3 个关键字的具体宽度，所以一个用户可能把 thick 、medium 和 thin 分别设置为等于 5px、3px 和 2px，而另一个用户则分别设置为 3px、2px 和 1px。

   `p.one {`    

   `border-style:solid;`    

   `border-width:5px;` 

   `}` 

   `p.two` 

   `{`    

   `border-style:solid;`    

   `border-width:medium;` 

   `}`

   border-color属性用于设置边框的颜色。可以设置的颜色：

   - name - 指定颜色的名称，如 "red"
   - RGB - 指定 RGB 值, 如 "rgb(255,0,0)"
   - Hex - 指定16进制值, 如 "#ff0000"

   您还可以设置边框的颜色为"transparent"。

   **注意：** border-color单独使用是不起作用的，必须得先使用border-style来设置边框样式。

   `p.one` 

   `{`    

   `border-style:solid;`    

   `border-color:red;` 

   `} p.two` 

   `{`    

   `border-style:solid;`    

   `border-color:#98bf21;` 

   `}`

   上面的例子也可以设置一个单一属性：

   `border-style:dotted solid;`

   border-style属性可以有1-4个值：

   - border-style:dotted solid double dashed;
     - 上边框是 dotted
     - 右边框是 solid
     - 底边框是 double
     - 左边框是 dashed
   - border-style:dotted solid double;
     - 上边框是 dotted
     - 左、右边框是 solid
     - 底边框是 double
   - border-style:dotted solid;
     - 上、底边框是 dotted
     - 右、左边框是 solid
   - border-style:dotted;
     - 四面边框是 dotted

   上面的例子用了border-style。然而，它也可以和border-width 、 border-color一起使用。

   上面的例子用了很多属性来设置边框。

   你也可以在一个属性中设置边框。

   你可以在"border"属性中设置：

   - border-width
   - border-style (required)
   - border-color

   例如：

   `border:5px solid red;`

   | 属性                                                         | 描述                                                         |
   | :----------------------------------------------------------- | :----------------------------------------------------------- |
   | [border](https://www.runoob.com/cssref/pr-border.html)       | 简写属性，用于把针对四个边的属性设置在一个声明。             |
   | [border-style](https://www.runoob.com/cssref/pr-border-style.html) | 用于设置元素所有边框的样式，或者单独地为各边设置边框样式。   |
   | [border-width](https://www.runoob.com/cssref/pr-border-width.html) | 简写属性，用于为元素的所有边框设置宽度，或者单独地为各边边框设置宽度。 |
   | [border-color](https://www.runoob.com/cssref/pr-border-color.html) | 简写属性，设置元素的所有边框中可见部分的颜色，或为 4 个边分别设置颜色。 |
   | [border-bottom](https://www.runoob.com/cssref/pr-border-bottom.html) | 简写属性，用于把下边框的所有属性设置到一个声明中。           |
   | [border-bottom-color](https://www.runoob.com/cssref/pr-border-bottom-color.html) | 设置元素的下边框的颜色。                                     |
   | [border-bottom-style](https://www.runoob.com/cssref/pr-border-bottom-style.html) | 设置元素的下边框的样式。                                     |
   | [border-bottom-width](https://www.runoob.com/cssref/pr-border-bottom-width.html) | 设置元素的下边框的宽度。                                     |
   | [border-left](https://www.runoob.com/cssref/pr-border-left.html) | 简写属性，用于把左边框的所有属性设置到一个声明中。           |
   | [border-left-color](https://www.runoob.com/cssref/pr-border-left-color.html) | 设置元素的左边框的颜色。                                     |
   | [border-left-style](https://www.runoob.com/cssref/pr-border-left-style.html) | 设置元素的左边框的样式。                                     |
   | [border-left-width](https://www.runoob.com/cssref/pr-border-left-width.html) | 设置元素的左边框的宽度。                                     |
   | [border-right](https://www.runoob.com/cssref/pr-border-right.html) | 简写属性，用于把右边框的所有属性设置到一个声明中。           |
   | [border-right-color](https://www.runoob.com/cssref/pr-border-right-color.html) | 设置元素的右边框的颜色。                                     |
   | [border-right-style](https://www.runoob.com/cssref/pr-border-right-style.html) | 设置元素的右边框的样式。                                     |
   | [border-right-width](https://www.runoob.com/cssref/pr-border-right-width.html) | 设置元素的右边框的宽度。                                     |
   | [border-top](https://www.runoob.com/cssref/pr-border-top.html) | 简写属性，用于把上边框的所有属性设置到一个声明中。           |
   | [border-top-color](https://www.runoob.com/cssref/pr-border-top-color.html) | 设置元素的上边框的颜色。                                     |
   | [border-top-style](https://www.runoob.com/cssref/pr-border-top-style.html) | 设置元素的上边框的样式。                                     |
   | [border-top-width](https://www.runoob.com/cssref/pr-border-top-width.html) | 设置元素的上边框的宽度。                                     |
   | [border-radius](https://www.runoob.com/cssref/css3-pr-border-radius.html) | 设置圆角的边框。                                             |

## 五、盒子模型

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。

盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。

下面的图片说明了盒子模型(Box Model)：

![CSS box-model](https://www.runoob.com/images/box-model.gif)

不同部分的说明：

- **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
- **Border(边框)** - 围绕在内边距和内容外的边框。
- **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
- **Content(内容)** - 盒子的内容，显示文本和图像。

当您指定一个 CSS 元素的宽度和高度属性时，你只是设置内容区域的宽度和高度。要知道，完整大小的元素，你还必须添加内边距，边框和外边距。

下面的例子中的元素的总宽度为 450px：

`div {`    

`width: 300px;`    

`border: 25px solid green;`    

`padding: 25px;`    

`margin: 25px;` 

`}`

让我们自己算算：
300px (宽)
\+ 50px (左 + 右填充)
\+ 50px (左 + 右边框)
\+ 50px (左 + 右边距)
= 450px

试想一下，你只有 250 像素的空间。让我们设置总宽度为 250 像素的元素:

`div {`    

`width: 220px;`    

`padding: 10px;`    

`border: 5px solid gray;`   

 `margin: 0;` 

 `}`

最终元素的总宽度计算公式是这样的：

总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距

元素的总高度最终计算公式是这样的：

总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

## 六、关于盒子模型的简单布局

1. 外边距

   CSS margin(外边距)属性定义元素周围的空间。

   margin 清除周围的（外边框）元素区域。margin 没有背景颜色，是完全透明的。

   margin 可以单独改变元素的上，下，左，右边距，也可以一次改变所有的属性。

   ![img](https://www.runoob.com/wp-content/uploads/2013/08/VlwVi.png)

   | 值       | 说明                                        |
   | :------- | :------------------------------------------ |
   | auto     | 设置浏览器边距。 这样做的结果会依赖于浏览器 |
   | *length* | 定义一个固定的margin（使用像素，pt，em等）  |
   | *%*      | 定义一个使用百分比的边距                    |

   在CSS中，它可以指定不同的侧面不同的边距：

   `margin-top:100px; margin-bottom:100px; margin-right:50px; margin-left:50px;`

   为了缩短代码，有可能使用一个属性中margin指定的所有边距属性。这就是所谓的简写属性。

   所有边距属性的简写属性是 **margin** :

   `margin:100px 50px;`

   margin属性可以有一到四个值。

   - margin:25px 50px 75px 100px;
     - 上边距为25px
     - 右边距为50px
     - 下边距为75px
     - 左边距为100px
   - margin:25px 50px 75px;
     - 上边距为25px
     - 左右边距为50px
     - 下边距为75px
   - margin:25px 50px;
     - 上下边距为25px
     - 左右边距为50px
   - margin:25px;
     - 所有的4个边距都是25px

2. 边框

   详情请看上面的边框内容

3. 填充

   CSS padding（填充）是一个简写属性，定义元素边框与元素内容之间的空间，即上下左右的内边距。

   当元素的 padding（填充）内边距被清除时，所释放的区域将会受到元素背景颜色的填充。

   单独使用 padding 属性可以改变上下左右的填充。

   | 值       | 说明                                |
   | :------- | :---------------------------------- |
   | *length* | 定义一个固定的填充(像素, pt, em,等) |
   | *%*      | 使用百分比值定义一个填充            |

   在CSS中，它可以指定不同的侧面不同的填充：

   `padding-top:25px;`
   `padding-bottom:25px;`
   `padding-right:50px;`
   `padding-left:50px;`

   - 上内边距是 25px
   - 右内边距是 50px
   - 下内边距是 25px
   - 左内边距是 50px

   为了缩短代码，它可以在一个属性中指定所有的填充属性。

   这就是所谓的简写属性。所有的填充属性的简写属性是 **padding** :

   `padding:25px 50px;`

   Padding属性，可以有一到四个值。

    **padding:25px 50px 75px 100px;**

   - 上填充为25px
   - 右填充为50px
   - 下填充为75px
   - 左填充为100px

    **padding:25px 50px 75px;**

   - 上填充为25px
   - 左右填充为50px
   - 下填充为75px

    **padding:25px 50px;**

   - 上下填充为25px
   - 左右填充为50px

    **padding:25px;**

   - 所有的填充都是25px

   | 属性                                                         | 说明                                       |
   | :----------------------------------------------------------- | :----------------------------------------- |
   | [padding](https://www.runoob.com/cssref/pr-padding.html)     | 使用简写属性设置在一个声明中的所有填充属性 |
   | [padding-bottom](https://www.runoob.com/cssref/pr-padding-bottom.html) | 设置元素的底部填充                         |
   | [padding-left](https://www.runoob.com/cssref/pr-padding-left.html) | 设置元素的左部填充                         |
   | [padding-right](https://www.runoob.com/cssref/pr-padding-right.html) | 设置元素的右部填充                         |
   | [padding-top](https://www.runoob.com/cssref/pr-padding-top.html) | 设置元素的顶部填充                         |

4. 内容

   即文字与图像。

## 七、常见选择器

如果你要在HTML元素中设置CSS样式，你需要在元素中设置"id" 和 "class"选择器。

1. id选择器

   id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

   HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。

   以下的样式规则应用于元素属性 id="para1":

   `\#para1` 

   `{`    

   `text-align:center;`   

    `color:red;` 

   `}`

   ID属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。

2. class选择器

   class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。

   class 选择器在 HTML 中以 class 属性表示, 在 CSS 中，类选择器以一个点 **.** 号显示：

   在以下的例子中，所有拥有 center 类的 HTML 元素均为居中。

   `.center {text-align:center;}`

   你也可以指定特定的 HTML 元素使用 class。

   在以下实例中, 所有的 p 元素使用 class="center" 让该元素的文本居中:

   `p.center {text-align:center;}`

   多个 class 选择器可以使用空格分开：

   `.center { text-align:center; }` 

   `.color { color:#ff0000; }`

   类名的第一个字符不能使用数字！它无法在 Mozilla 或 Firefox 中起作用

## 八、导航栏

熟练使用导航栏，对于任何网站都非常重要。

使用CSS你可以转换成好看的导航栏而不是枯燥的HTML菜单。

作为标准的 HTML 基础一个导航栏是必须的。

在我们的例子中我们将建立一个标准的 HTML 列表导航栏。

导航条基本上是一个链接列表，所以使用` <ul>` 和` <li>`元素非常有意义：

<ul>   <li><a href="#home">主页</a></li>   <li><a href="#news">新闻</a></li>   <li><a href="#contact">联系</a></li>   <li><a href="#about">关于</a></li> </ul>

现在，让我们从列表中删除边距和填充：

`ul {`    

`list-style-type: none;`    

`margin: 0;`    

`padding: 0;`

 `}`

例子解析：

- list-style-type:none - 移除列表前小标志。一个导航栏并不需要列表标记
- 移除浏览器的默认设置将边距和填充设置为0

上面的代码，我们只需要 `<a>`元素的样式，建立一个垂直的导航栏：

`a`

 `{`    

`display:block;`    

`width:60px;` 

`}`

示例说明：

- display:block - 显示块元素的链接，让整体变为可点击链接区域（不只是文本），它允许我们指定宽度
- width:60px - 块元素默认情况下是最大宽度。我们要指定一个60像素的宽度

创建一个简单的垂直导航条实例，在鼠标移动到选项时，修改背景颜色：

`ul {`    

`list-style-type: none;`    

`margin: 0;`    

`padding: 0;`    

`width: 200px;`    

`background-color: #f1f1f1;` 

`}`  

`li a {`    

`display: block;`    

`color: #000;`    

`padding: 8px 16px;`    

`text-decoration: none;` 

`}` 

`/* 鼠标移动到选项上修改背景颜色 */` 

`li a:hover {`    

`background-color: #555;`    

`color: white;`

 `}`

在点击了选项后，我们可以添加 "active" 类来标注哪个选项被选中：

`li a.active {`   

 `background-color: #4CAF50;`    

`color: white;` 

`}`

可以在 `<li>` or `<a>` 上添加**text-align:center** 样式来让链接居中。

可以在 **border** `<ul>` 上添加 **border** 属性来让导航栏有边框。如果要在每个选项上添加边框，可以在每个 `<li> `元素上添加**border-bottom** :

`ul {`    

`border: 1px solid #555;` 

`}`  

`li {`    

`text-align: center;`   

`border-bottom: 1px solid #555;` 

`}`  

`li:last-child {`    

`border-bottom: none;` 

`}`

接下来我们创建一个左边是全屏高度的固定导航条，右边是可滚动的内容。

`ul {`    

`list-style-type: none;`    

`margin: 0;`    

`padding: 0;`    

`width: 25%;`    

`background-color: #f1f1f1;`    

`height: 100%; /* 全屏高度 */    `

`position: fixed;     `

`overflow: auto; `

`/* 如果导航栏选项多，允许滚动 */` 

`}`

**注意:** 该实例可以在移动设备上使用。

有两种方法创建横向导航栏。使用**内联(inline)**或**浮动(float)**的列表项。

这两种方法都很好，但如果你想链接到具有相同的大小，你必须使用浮动的方法。

建立一个横向导航栏的方法之一是指定元素， 下述代码是标准的内联:

`li` 

`{`    

`display:inline;` 

`}`

实例解析：

- display:inline; - 默认情况下，`<li>` 元素是块元素。在这里，我们删除换行符之前和之后每个列表项，以显示一行。

在上面的例子中链接有不同的宽度。

对于所有的链接宽度相等，浮动 `<li>`元素，并指定为` <a>`元素的宽度：

`li` 

`{`    

`float:left;` 

`}` 

`a` 

`{`    

`display:block;`    

`width:60px;` 

`}`

实例解析：

- float:left - 使用浮动块元素的幻灯片彼此相邻
- display:block - 显示块元素的链接，让整体变为可点击链接区域（不只是文本），它允许我们指定宽度
- width:60px - 块元素默认情况下是最大宽度。我们要指定一个60像素的宽度

创建一个水平导航条，在鼠标移动到选项后修改背景颜色。

`ul {`    

`list-style-type: none;`    

`margin: 0;`    

`padding: 0;`    

`overflow: hidden;`   

 `background-color: #333;` 

`}`  

`li {`    

`float: left;` 

`}`  

`li a {`    

`display: block;`   

`color: white;`    

`text-align: center;`    

`padding: 14px 16px;`    

`text-decoration: none;` 

`}  /*鼠标移动到选项上修改背景颜色 */` 

`li a:hover {`    

`background-color: #111;` 

`}`

在点击了选项后，我们可以添加 "active" 类来标准哪个选项被选中：

`.active {`    

`background-color: #4CAF50;` 

`}`

`<li> `通过 **border-right** 样式来添加分割线:

`/* 除了最后一个选项(last-child) 其他的都添加分割线 */` 

`li {`    

`border-right: 1px solid #bbb;` 

`}`  

`li:last-child {`    

`border-right: none;` 

`}`

可以设置页面的导航条固定在头部或者底部：

`ul {`    

`position: fixed;`    

`top: 0;`    

`width: 100%;` 

`}`

`ul {`    

`position: fixed;`    

`bottom: 0;`    

`width: 100%;` 

`}`

**注意:** 该实例可以在移动设备上使用。

灰色水平导航条:

`ul {`    

`border: 1px solid #e7e7e7;`    

`background-color: #f3f3f3;` 

`}`  

`li a {`   

 `color: #666;` 

`}`

## 九、具体例子

使用ai生成一个使用HTML和css的具体实例：

<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <title>我的个人博客</title>
  <style>
    /* 全局初始化 */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
​    body {
​      font-family: "Microsoft YaHei", sans-serif;
​      background: #f5f5f5;
​      line-height: 1.7;
​      color: #333;
​    }

​    /* 导航栏 */
​    .nav {
​      background: #2c3e50;
​      padding: 15px 0;
​      text-align: center;
​    }

​    .nav a {
​      color: white;
​      text-decoration: none;
​      margin: 0 15px;
​      font-size: 16px;
​    }

​    .nav a:hover {
​      color: #ffcc00;
​    }

​    /* 博客容器 */
​    .container {
​      max-width: 800px;
​      margin: 30px auto;
​      padding: 0 20px;
​    }

​    /* 卡片样式（盒子模型） */
​    .card {
​      background: white;
​      padding: 25px;
​      margin-bottom: 20px;
​      border-radius: 8px;
​      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
​    }

​    /* 标题 */
​    .card h2 {
​      margin-bottom: 10px;
​      color: #2c3e50;
​    }

​    /* 日期 */
​    .date {
​      color: #7f8c8d;
​      font-size: 14px;
​      margin-bottom: 10px;
​    }

​    /* 图片 */
​    .card img {
​      width: 100%;
​      border-radius: 5px;
​      margin: 10px 0;
​    }

​    /* 底部 */
​    .footer {
​      text-align: center;
​      padding: 20px;
​      background: #2c3e50;
​      color: white;
​      margin-top: 30px;
​    }
  </style>
</head>

<body>

  <!-- 导航栏 -->
  <div class="nav">
    <a href="#home">首页</a>
    <a href="#blog">博客文章</a>
    <a href="#about">关于我</a>
  </div>

  <!-- 内容区域 -->
  <div class="container">

​    <!-- 首页区域 -->
    <div id="home" class="card">
      <h2>欢迎来到我的个人博客</h2>
      <p>记录学习、生活、技术与日常思考。</p>
    </div>

​    <!-- 博客文章 -->
    <div id="blog" class="card">
      <h2>我的第一篇博客</h2>
      <div class="date">2026-04-04</div>
      <img src="https://picsum.photos/800/300" alt="博客图片">
      <p>今天我学会了 HTML + CSS，成功搭建了自己的第一个博客！</p>
      <p>HTML 负责结构，CSS 负责美化，原来做网页这么简单！</p>
    </div>

    <div class="card">
      <h2>学习 CSS 盒子模型心得</h2>
      <div class="date">2026-04-04</div>
      <p>所有网页元素都是盒子！</p>
      <p>内容 → 内边距 → 边框 → 外边距，我终于理解了！</p>
    </div>

​    <!-- 关于我 -->
    <div id="about" class="card">
      <h2>关于我</h2>
      <img src="https://picsum.photos/200/200" alt="我的头像" width="120">
      <p>热爱编程、喜欢写作、正在学习网页制作。</p>
      <p>目标：做出属于自己的漂亮网站！</p>
    </div>

  </div>

  <!-- 底部 -->
  <div class="footer">
    © 2026 我的个人博客 | 纯 HTML + CSS 制作
  </div>
</body>
</html>



