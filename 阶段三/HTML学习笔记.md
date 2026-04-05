# 关于HTML的学习

前言：由于精力有限，这部分内容学习HTML基础结构、文本与段落标签、列表与表格标签、链接与图片、布局容器标签五个方面。

## 一、HTML基础结构

1. html标题

   HTML 标题（Heading）是通过` <h1> - <h6> `等标签进行定义的。

   ```html
   <h1>This is a heading</h1>
   <h2>This is a heading</h2>
   <h3>This is a heading</h3>
   ```

2. html段落

   HTML 段落是通过 `<p>` 标签进行定义的。

   ```html
   <p>This is a paragraph.</p>
   <p>This is another paragraph.</p>
   ```

3. html链接

   HTML 链接是通过 `<a>` 标签进行定义的，在 href 属性中指定链接的地址。

   ```html
   <a href="http://www.w3school.com.cn">This is a link</a>
   ```

4. html图像

   HTML 图像是通过` <img>` 标签进行定义的，图像的名称和尺寸是以属性的形式提供的。

   ```html
   <img src="w3school.jpg" width="104" height="142" />
   ```

5. html元素

   HTML 元素指的是从开始标签（start tag）到结束标签（end tag）的所有代码。

   | 开始标签                  | 元素内容            | 结束标签 |
   | :------------------------ | :------------------ | :------- |
   | `<p>`                     | This is a paragraph | `</p>`   |
   | `<a href="default.htm" >` | This is a link      | `</a>`   |
   | `<br />`                  |                     |          |

   大多数 HTML 元素可以嵌套（可以包含其他 HTML 元素）。

   HTML 文档由嵌套的 HTML 元素构成。

   ```html
   <html>
   
   <body>
   <p>This is my first paragraph.</p>
   </body>
   
   </html>
   ```

   注意要写结束标签。

   空元素是指没有内容的元素，例如：

   - `<br>`（换行）推荐
   - `<img>`（图片）
   - `<input>`（输入框）

   注意统一使用小写标签。

6. html的属性

   属性是 HTML 元素提供的附加信息。

   属性通常出现在 HTML 标签的开始标签中，用于定义元素的行为、样式、内容或其他特性。

   属性总是以 **name="value"** 的形式写在标签内，**name** 是属性的名称，**value** 是属性的值。

   - HTML 元素可以设置**属性**
   - 属性可以在元素中添加**附加信息**
   - 属性一般描述于**开始标签**

   属性值应该始终被包括在引号内。

   双引号是最常用的，不过使用单引号也没有问题。

   注意最好使用小写属性。

   下面列出了适用于大多数 HTML 元素的属性：

   | 属性名        | 适用元素                                          | 说明                                                         |
   | :------------ | :------------------------------------------------ | :----------------------------------------------------------- |
   | `id`          | 所有元素                                          | 为元素指定唯一的标识符。                                     |
   | `class`       | 所有元素                                          | 为元素指定一个或多个类名，用于 CSS 或 JavaScript 选择。      |
   | `style`       | 所有元素                                          | 直接在元素上应用 CSS 样式。                                  |
   | `title`       | 所有元素                                          | 为元素提供额外的提示信息，通常在鼠标悬停时显示。             |
   | `data-*`      | 所有元素                                          | 用于存储自定义数据，通常通过 JavaScript 访问。               |
   | `href`        | `<a>`, `<link>`                                   | 指定链接的目标 URL。                                         |
   | `src`         | `<img>`, `<script>`, `<iframe>`                   | 指定外部资源（如图片、脚本、框架）的 URL。                   |
   | `alt`         | `<img>`                                           | 为图像提供替代文本，当图像无法显示时显示。                   |
   | `type`        | `<input>`, `<button>`                             | 指定输入控件的类型（如 `text`, `password`, `checkbox` 等）。 |
   | `value`       | `<input>`, `<button>`, `<option>`                 | 指定元素的初始值。                                           |
   | `disabled`    | 表单元素                                          | 禁用元素，使其不可交互。                                     |
   | `checked`     | `<input type="checkbox">`, `<input type="radio">` | 指定复选框或单选按钮是否被选中。                             |
   | `placeholder` | `<input>`, `<textarea>`                           | 在输入框中显示提示文本。                                     |
   | `target`      | `<a>`, `<form>`                                   | 指定链接或表单提交的目标窗口或框架（如 `_blank` 表示新标签页）。 |
   | `readonly`    | 表单元素                                          | 使输入框只读。                                               |
   | `required`    | 表单元素                                          | 指定输入字段为必填项。                                       |
   | `autoplay`    | `<audio>`, `<video>`                              | 自动播放媒体。                                               |
   | `onclick`     | 所有元素                                          | 当用户点击元素时触发 JavaScript 事件。                       |
   | `onmouseover` | 所有元素                                          | 当用户将鼠标悬停在元素上时触发 JavaScript 事件。             |
   | `onchange`    | 表单元素                                          | 当元素的值发生变化时触发 JavaScript 事件。                   |

   全局属性是所有 HTML 元素都可以使用的属性。

   **id**：为元素指定唯一的标识符。

   ```
   <div id="header">This is the header</div>
   ```

   **class**：为元素指定一个或多个类名，用于 CSS 或 JavaScript 选择。

   ```
   <p class="text highlight">This is a highlighted text.</p>
   ```

   **style**：用于直接在元素上应用 CSS 样式。

   ```
   <p style="color: blue; font-size: 14px;">This is a styled paragraph.</p>
   ```

   **title**：为元素提供额外的提示信息，通常在鼠标悬停时显示。

   ```
   <abbr title="HyperText Markup Language">HTML</abbr>
   ```

   **data-\***：用于存储自定义数据，通常通过 JavaScript 访问。

   ```
   <div data-user-id="12345">User Info</div>
   ```

## 二、文本与段落标签

1. 再看html标题

   标题（Heading）是通过 `<h1> - <h6>` 标签进行定义的。

   从1到6依次减小。

   注意html标题标签只用于标题，不要用于加粗以及大号文本。

   hr标签在 HTML 页面中创建水平线。

   hr 元素可用于分隔内容。

   html注释写法如下：

   !-- 这是一个注释 --

   开始括号之后（左边的括号）需要紧跟一个叹号 **!** (英文标点符号)，结束括号之前（右边的括号）不需要。

   | 标签         | 描述           |
   | :----------- | :------------- |
   | `<html>`     | 定义 HTML 文档 |
   | `<body>`     | 定义文档的主体 |
   | `<h1-h6>`    | 定义 HTML 标题 |
   | `<hr>`       | 定义水平线     |
   | `<!--...-->` | 定义注释       |

2. 再看html段落

   段落是通过 `<p>` 标签定义的。

   浏览器会自动地在段落的前后添加空行。

   不要忘记结束标签。

   如果想在不产生新段落的情况下换行，可以使用br标签。

   提醒：当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。

3. 文本格式化

   直接给标签

   | 标签       | 描述         |
   | :--------- | :----------- |
   | `<b>`      | 定义粗体文本 |
   | `<em>`     | 定义着重文字 |
   | `<i>`      | 定义斜体字   |
   | `<small>`  | 定义小号字   |
   | `<strong>` | 定义加重语气 |
   | `<sub>`    | 定义下标字   |
   | `<sup>`    | 定义上标字   |
   | `<ins>`    | 定义插入字   |
   | `<del>`    | 定义删除字   |

   | 标签     | 描述               |
   | :------- | :----------------- |
   | `<code>` | 定义计算机代码     |
   | `<kbd>`  | 定义键盘码         |
   | `<samp>` | 定义计算机代码样本 |
   | `<var>`  | 定义变量           |
   | `<pre>`  | 定义预格式文本     |

   | 标签           | 描述               |
   | :------------- | :----------------- |
   | `<abbr>`       | 定义缩写           |
   | `<address>`    | 定义地址           |
   | `<kdo>`        | 定义文字方向       |
   | `<blockquote>` | 定义长的引用       |
   | `<q>`          | 定义短的引用语     |
   | `<cite>`       | 定义引用、引证     |
   | `<dfn>`        | 定义一个定义项目。 |

## 三、列表与表格标签

1.列表标签

HTML 支持有序、无序和定义列表。

无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。

无序列表使用 `<ul>` 标签

`<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>`

浏览器显示如下：

- Coffee
- Milk

同样，有序列表也是一列项目，列表项目使用数字进行标记。 有序列表始于 `<ol> `标签。每个列表项始于 `<li>` 标签。

列表项使用数字来标记。

`<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>`

浏览器中显示如下：

1. Coffee
2. Milk

自定义列表不仅仅是一列项目，而是项目及其注释的组合。

自定义列表以` <dl> `标签开始。每个自定义列表项以` <dt> `开始。每个自定义列表项的定义以` <dd>` 开始。

`<dl>
<dt>Coffee</dt>
<dd>- black hot drink</dd>
<dt>Milk</dt>
<dd>- white cold drink</dd>
</dl>`

浏览器显示如下：

- Coffee

  - black hot drink

- Milk

  - white cold drink

| 标签   | 描述                 |
| :----- | :------------------- |
| `<ol>` | 定义有序列表         |
| `<ul>` | 定义无序列表         |
| `<li>` | 定义列表项           |
| `<di>` | 定义列表             |
| `<dt>` | 自定义列表项目       |
| `<dd>` | 定义自定列表项的描述 |

注意：列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

2.表格标签

HTML 表格由` <table> `标签来定义。

HTML 表格是一种用于展示结构化数据的标记语言元素。

每个表格均有若干行（由 `<tr>`标签定义），每行被分割为若干单元格（由 `<td>` 标签定义），表格可以包含标题行（`<th>`）用于定义列的标题。

- **tr**：tr 是 table row 的缩写，表示表格的一行。
- **td**：td 是 table data 的缩写，表示表格的数据单元格。
- **th**：th 是 table header的缩写，表示表格的表头单元格。

数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

`<thead > `用于定义表格的标题部分: 在` <thead > `中，使用 `<th >` 元素定义列的标题

`<tbody >` 用于定义表格的主体部分: 在 `<tbody > `中，使用` <tr > `元素定义行，并在每行中使用 `<td >` 元素定义单元格数据

通过使用` <th > `元素定义列标题，可以使其在表格中以粗体显示，与普通单元格区分开来。

HTML 表格还可以具有其他部分，如` <tfoot > `（表格页脚）和 `<caption >` （表格标题），`<tfoot >` 可用于在表格的底部定义摘要、统计信息等内容。` <caption > `可用于为整个表格定义标题。

HTML 表格还支持合并单元格和跨行/跨列的操作，以及其他样式和属性的应用，以满足各种需求。

| 标签         | 描述                 |
| :----------- | :------------------- |
| `<table>`    | 定义表格             |
| `<th>`       | 定义表格的表头       |
| `<tr>`       | 定义表格的行         |
| `<td>`       | 定义表格单元         |
| `<caption>`  | 定义表格标题         |
| `<colgroup>` | 定义表格列的组       |
| `<col>`      | 定义用于表格列的属性 |
| `<thead>`    | 定义表格的页眉       |
| `<tbody>`    | 定义表格的主体       |
| `<tfoot>`    | 定义表格的页脚       |

## 四、链接与图片标签

1. 再看链接

   HTML 链接 通过`<a>`标签创建，通常用于将用户从一个页面导航到另一个页面、从一个部分跳转到页面中的另一个部分、下载文件、打开电子邮件应用程序或执行 JavaScript 函数等。

   ### 基本语法

   ```
   <a href="URL">链接文本</a>
   ```

   - `<a>` 标签：定义了一个超链接（anchor）。它是 HTML 中用来创建可点击链接的主要标签。
   - `href` 属性：指定目标 URL，当点击链接时，浏览器将导航到此 URL。

   以下实例演示来如何在 HTML 文档中创建链接：

   `<a href="/index.html">本文本</a>`是一个指向本网站中的一个页面的链接。`</p>`

   `<p><a href="https://www.microsoft.com/">本文本</a>`是一个指向万维网上的页面的链接。`<p>`

   HTML使用标签` <a>`来设置超文本链接。

   超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。

   当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手。

   在标签` <a> `中使用了` href `属性来描述链接的地址。

   默认情况下，链接将以以下形式出现在浏览器中：

   - 一个未访问过的链接显示为蓝色字体并带有下划线。
   - 访问过的链接显示为紫色并带有下划线。
   - 点击链接时，链接显示为红色并带有下划线。

   以下内容介绍html各链接属性：

   1、href：定义链接目标

   这是超链接最重要的属性，用来指定链接的目的地，可以是另一个网页、文件、邮件、电话号码或 JavaScript。

   `<a href="https://www.example.com">访问 Example</a>`

   2、target：定义链接的打开方式

   - `_blank`: 在新窗口或新标签页中打开链接。
   - `_self`: 在当前窗口或标签页中打开链接（默认）。
   - `_parent`: 在父框架中打开链接。
   - `_top`: 在整个窗口中打开链接，取消任何框架。

   `<a href="https://www.example.com" target="_blank" rel="noopener">新窗口打开 Example</a>`

   3、rel：定义链接与目标页面的关系

   **nofollow**: 表示搜索引擎不应跟踪该链接，常用于外部链接。

   **noopener** 和 **noreferrer**: 防止在新标签中打开链接时的安全问题，尤其是使用 **target="_blank"** 时。

   - `noopener`: 防止新的浏览上下文（页面）访问`window.opener`属性和`open`方法。
   - `noreferrer`: 不发送referer header（即不告诉目标网站你从哪里来的）。
   - `noopener noreferrer`: 同时使用`noopener`和`noreferrer`。例子: `<a href="https://www.example.com" rel="noopener noreferrer">安全链接</a>`

   `<a href="https://www.example.com" target="_blank" rel="noopener noreferrer">安全链接</a>`

   4、download：提示浏览器下载链接目标而不是导航到该目标

   如果指定了文件名，浏览器会提示下载并保存为指定文件名。

   例如：

   `<a href="file.pdf" download="example.pdf">下载文件</a>`

   5、title：定义链接的额外信息，当鼠标悬停在链接上时显示的工具提示

   `<a href="https://www.example.com" title="访问 Example 网站">访问 Example</a>`

   6、id：用于链接锚点，通常在同一页面中跳转到某个特定位置

   `<!-- 链接到页面中的某个部分 -->`
   `<a href="#section1">跳转到第1部分</a>`

   `<div id="section1">这是第1部分</div>`

   7、hreflang: 指定链接的目标URL的语言

   `<a href="https://www.example.com/es" hreflang="es">访问西班牙语网站</a>`

   8、type: 指定链接资源的MIME类型

   `<a href="style.css" type="text/css">样式表</a>`

   9、class: 用于指定元素的类名（CSS中定义）

   `<a href="https://www.example.com" class="external-link">外部链接</a>`

   10、style: 直接在元素上定义CSS样式

   `<a href="https://www.example.com" style="color: red;">红色链接</a>`
   
   注意：链接文本不一定是文本，图片或者其他元素都可以成为链接
   
   以下给出相关链接的写法：
   
   文本链接：最常见的链接类型是文本链接，它使用 `<a> `元素将一段文本转化为可点击的链接，例如：
   
   ```
   <a href="https://www.example.com">访问示例网站</a>
   ```
   
   图像链接：您还可以使用图像作为链接。在这种情况下，`<a> `元素包围着` <img> `元素。例如：
   
   ```
   <a href="https://www.example.com">
     <img src="example.jpg" alt="示例图片">
   </a>
   ```
   
   锚点链接：除了链接到其他网页外，您还可以在同一页面内创建内部链接，这称为锚点链接。要创建锚点链接，需要在目标位置使用 <a> 元素定义一个标记，并使用#符号引用该标记。例如：
   
   ```
   <a href="#section2">跳转到第二部分</a>
   <!-- 在页面中的某个位置 -->
   <a name="section2"></a>
   ```
   
   下载链接：如果您希望链接用于下载文件而不是导航到另一个网页，可以使用 download 属性。例如：
   
   `<a href="document.pdf" download>下载文档</a>`
   
   target属性：
   
   使用 target 属性，你可以定义被链接的文档在何处显示。
   
   下面的这行会在新窗口打开文档：
   
   `<a href="https://www.runoob.com/" target="_blank" rel="noopener noreferrer">访问菜鸟教程!</a>`
   
   id属性：
   
   id 属性可用于创建一个 HTML 文档书签。
   
   在HTML文档中插入ID:
   
   ```
   <a id="tips">有用的提示部分</a>
   ```
   
   在HTML文档中创建一个链接到"有用的提示部分(id="tips"）"：
   
   ```
   <a href="#tips">访问有用的提示部分</a>
   ```
   
   或者，从另一个页面创建一个链接到"有用的提示部分(id="tips"）"：
   
   `<a href="https://www.runoob.com/html/html-links.html#tips">
   访问有用的提示部分</a>`
   
   空链接：
   
   | 方法                        | 作用                       | 是否会跳转 | 场景适用性                   |
   | :-------------------------- | :------------------------- | :--------- | :--------------------------- |
   | `href="#"`                  | 导航到页面顶部             | 是         | 占位符，捕获点击事件         |
   | `href="javascript:void(0)"` | 阻止默认行为，不刷新页面   | 否         | 阻止跳转，配合 JS 使用       |
   | `href=""`                   | 刷新当前页面               | 是         | 需要页面刷新时               |
   | `href="about:blank"`        | 打开空白页面               | 是         | 新窗口打开空白页面           |
   | `role="button"`             | 链接表现为按钮，无默认行为 | 否         | 配合 JS 实现按钮功能，无跳转 |

2. 图片标签

   在 HTML 中，图像由`<img>` 标签定义。

   `<img> `是空标签，意思是说，它只包含属性，并且没有闭合标签。

   要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。

   定义图像的语法是：

   `<img src="url" alt="some_text">`

   URL 指存储图像的位置。如果名为 "pulpit.jpg" 的图像位于` www.runoob.com `的 images 目录中，那么其 URL 为` http://www.runoob.com/images/pulpit.jpg`。

   浏览器将图像显示在文档中图像标签出现的地方。如果你将图像标签置于两个段落之间，那么浏览器会首先显示第一个段落，然后显示图片，最后显示第二段。

   alt属性：

   alt 属性用来为图像定义一串预备的可替换的文本。

   替换文本属性的值是用户定义的。

   `<img src="boat.gif" alt="Big Boat">`

   在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。为页面上的图像都加上替换文本属性是个好习惯，这样有助于更好的显示信息，并且对于那些使用纯文本浏览器的人来说是非常有用的。

   图像高度与宽度的设置：

   height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。

   属性值默认单位为像素:

   `<img src="pulpit.jpg" alt="Pulpit rock" width="304" height="228">`

   提示: 指定图像的高度和宽度是一个很好的习惯。如果图像指定了高度宽度，页面加载时就会保留指定的尺寸。如果没有指定图片的大小，加载页面时有可能会破坏HTML页面的整体布局。

   注意：加载图片需要时间，所以慎用图片。注意插入页面图像的路径，如果不能正确设置图像的位置，浏览器无法加载图片，图像标签就会显示一个破碎的图片。

   html图像标签：

   | 标签     | 描述                       |
   | :------- | :------------------------- |
   | `<img>`  | 定义图像                   |
   | `<map>`  | 定义图像地图               |
   | `<area>` | 定义图像地图中的可点击区域 |

## 五、布局容器标签

网页布局可以用`<div>`和`<table>`两种元素来布局，但大部分情况都是用div元素，所以这部分只学习div。

div 元素是用于分组 HTML 元素的块级元素。

下面的例子使用五个 div 元素来创建多列布局：

<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
<div id="container" style="width:500px">

<div id="header" style="background-color:#FFA500;">
<h1 style="margin-bottom:0;">主要的网页标题</h1></div>


<div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
<b>菜单</b><br>
HTML<br>
CSS<br>
JavaScript</div>

<div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
内容在这里</div>

<div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
版权 © runoob.com</div>
`</div>`

`</body>`
`</html>`

html布局标签：

| 标签     | 描述                                  |
| :------- | :------------------------------------ |
| `<div>`  | 定义文档区块，块级(block-level)       |
| `<span>` | 定义 span，用来组合文档中的行内元素。 |

## 六、关于HTML的例子

只看以上内容显然很难串联在一起，所以我使用ai生成了一个只用HTML的例子：

`<!-- HTML5文档声明，固定第一行 -->`

`<!DOCTYPE html>`

`<!-- 网页根标签，语言中文 -->`
`<html lang="zh-CN">`

`<!-- 头部：设置标题和编码 -->`

`<head>`
`    <meta charset="UTF-8">  <!-- 中文不乱码 -->`
`    <title>我的个人博客</title>  <!-- 浏览器标题 -->`
`</head>`



`<!-- 网页主体内容 -->`
`<body>`

    <!-- 博客顶部大标题 -->
    
    <h1>我的个人博客</h1>
    
    <!-- 导航菜单 -->
    
    <p>
        <a href="#home">首页</a> | 
        <a href="#articles">文章</a> | 
        <a href="#about">关于我</a>
    </p>


    <hr> <!-- 分割线 -->


    <!-- 首页区域 -->
    
    <h2 id="home">首页</h2>
    
    <!-- 博客封面图片：在线图片，直接显示 -->
    <img src="https://picsum.photos/600/200" alt="博客封面" width="600">
    
    <p>欢迎来到我的博客，记录学习、生活和成长。</p>
    
    <hr>


    <!-- 文章列表区域 -->
    
    <h2 id="articles">我的文章</h2>
    
    <!-- 文章1 -->
    
    <h3>文章1：学习HTML的心得</h3>
    
    <!-- 文章图片 -->
    <img src="https://picsum.photos/400/200?random=1" alt="学习图片" width="400">
    
    <p>日期：2026-04-04</p>
    <p>HTML是网页的基础，非常简单，我已经学会啦！</p>
    
    <br>
    
    <!-- 文章2 -->
    
    <h3>文章2：我的博客搭建记录</h3>
    
    <img src="https://picsum.photos/400/200?random=2" alt="博客图片" width="400">
    
    <p>日期：2026-04-04</p>
    <p>今天我用纯HTML做了一个带图片的博客！</p>
    
    <hr>


    <!-- 关于我区域 -->
    
    <h2 id="about">关于我</h2>
    
    <!-- 个人头像图片 -->
    <img src="https://picsum.photos/200/200?random=3" alt="我的头像" width="200">
    
    <p>我是一名热爱编程的新手。</p>
    <p>喜欢写博客、分享学习笔记。</p>
    
    <hr>


    <!-- 底部版权 -->
    
    <p>© 2026 我的个人博客</p>

`</body>`
`</html>`

对这个ai生成的例子进行总结，HTML的部分主要分为两部分：

1. `<head>`头部，这部分内容是给浏览器看的，用户看不到，作用为设置网页信息，里面可以放置网页标题（显示在浏览器标签上），字符编码，css美化，图标，seo标签等等内容
2. `<body>`身体，这部分内容是给用户看的，作用为放置网页上所有能看到的东西，里面可以放置标题h，文字p，图片img，链接a以及其他部分。
