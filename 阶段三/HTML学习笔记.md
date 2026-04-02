# 关于HTML的学习

前言：由于精力有限，这部分内容学习HTML基础结构、文本与段落标签、列表标签、链接与图片、布局容器标签五个方面。

## 一、HTML基础结构

1. html标题

   HTML 标题（Heading）是通过 <h1> - <h6> 等标签进行定义的。

   ```html
   <h1>This is a heading</h1>
   <h2>This is a heading</h2>
   <h3>This is a heading</h3>
   ```

2. html段落

   HTML 段落是通过 <p> 标签进行定义的。

   ```html
   <p>This is a paragraph.</p>
   <p>This is another paragraph.</p>
   ```

3. html链接

   HTML 链接是通过 <a> 标签进行定义的，在 href 属性中指定链接的地址。

   ```html
   <a href="http://www.w3school.com.cn">This is a link</a>
   ```

4. html图像

   HTML 图像是通过 <img> 标签进行定义的，图像的名称和尺寸是以属性的形式提供的。

   ```html
   <img src="w3school.jpg" width="104" height="142" />
   ```

5. html元素

   HTML 元素指的是从开始标签（start tag）到结束标签（end tag）的所有代码。

   | 开始标签                | 元素内容            | 结束标签 |
   | :---------------------- | :------------------ | :------- |
   | <p>                     | This is a paragraph | </p>     |
   | <a href="default.htm" > | This is a link      | </a>     |
   | <br />                  |                     |          |

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

   标题（Heading）是通过 <h1> - <h6> 标签进行定义的。

   从1到6依次减小。

   注意html标题标签只用于标题，不要用于加粗以及大号文本。

   hr标签在 HTML 页面中创建水平线。

   hr 元素可用于分隔内容。

   html注释写法如下：

   <!-- 这是一个注释 -->

   开始括号之后（左边的括号）需要紧跟一个叹号 **!** (英文标点符号)，结束括号之前（右边的括号）不需要。

   | 标签       | 描述           |
   | :--------- | :------------- |
   | <html>     | 定义 HTML 文档 |
   | <body>     | 定义文档的主体 |
   | <h1>-<h6>  | 定义 HTML 标题 |
   | <hr>       | 定义水平线     |
   | <!--...--> | 定义注释       |

2. 再看html段落

   段落是通过 <p> 标签定义的。

   浏览器会自动地在段落的前后添加空行。

   不要忘记结束标签。

   如果想在不产生新段落的情况下换行，可以使用br标签。

   提醒：当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。

3. 文本格式化

   直接给标签

   | 标签     | 描述         |
   | :------- | :----------- |
   | <b>      | 定义粗体文本 |
   | <em>     | 定义着重文字 |
   | <i>      | 定义斜体字   |
   | <small>  | 定义小号字   |
   | <strong> | 定义加重语气 |
   | <sub>    | 定义下标字   |
   | <sup>    | 定义上标字   |
   | <ins>    | 定义插入字   |
   | <del>    | 定义删除字   |

   | 标签   | 描述               |
   | :----- | :----------------- |
   | <code> | 定义计算机代码     |
   | <kbd>  | 定义键盘码         |
   | <samp> | 定义计算机代码样本 |
   | <var>  | 定义变量           |
   | <pre>  | 定义预格式文本     |

   | 标签         | 描述               |
   | :----------- | :----------------- |
   | <abbr>       | 定义缩写           |
   | <address>    | 定义地址           |
   | <kdo>        | 定义文字方向       |
   | <blockquote> | 定义长的引用       |
   | <q>          | 定义短的引用语     |
   | <cite>       | 定义引用、引证     |
   | <dfn>        | 定义一个定义项目。 |

