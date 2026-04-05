# 关于JavaScript的学习

前言：js简单了解，计划学习引入方式，变量与输出，获取页面元素，事件基础，简单dom操作，具体例子六个方面来进行学习。

# 一、引入方式

HTML 中的 Javascript 脚本代码必须位于 `<script> `与 `</script>` 标签之间。

Javascript 脚本代码可被放置在 HTML 页面的` <body>` 和 `<head> `部分中。

也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是 .js。

如需使用外部文件，请在 <script> 标签的 "src" 属性中设置该 .js 文件：

`<!DOCTYPE html> `

`<html> `

`<body> `

`<script src="myScript.js"></script> `

`</body> `

`</html>`

# 二、变量与输出

变量是用于存储信息的"容器"。

在 JavaScript 中，变量用于存储数据，并可以在程序执行过程中动态更改。

在 JavaScript 中，变量可以存储各种类型的数据，如数字、字符串、对象、函数等。

变量名是标识符，用于引用存储在变量中的数据。

在 JavaScript 中，可以使用 **var**、**let** 和 **const** 关键字来声明变量。

- **`var`**：ES5 引入的变量声明方式，具有函数作用域。
- **`let`**：ES6 引入的变量声明方式，具有块级作用域。
- **`const`**：ES6 引入的常量声明方式，具有块级作用域，且值不可变。、

`var x=5;` 

`var y=6;` 

`var z=x+y;`

与代数一样，JavaScript 变量可用于存放值（比如 **x = 5**）和表达式（比如 **z = x + y**）。

变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

- 变量必须以字母开头
- 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
- 变量名称对大小写敏感（y 和 Y 是不同的变量）

JavaScript 变量还能保存其他数据类型，比如文本值 (name="Bill Gates")。

在 JavaScript 中，类似 "Bill Gates" 这样一条文本被称为字符串。

JavaScript 变量有很多种类型，但是现在，我们只关注数字和字符串。

当您向变量分配文本值时，应该用双引号或单引号包围这个值。

当您向变量赋的值是数值时，不要使用引号。如果您用引号包围数值，该值会被作为文本来处理。

`var pi=3.14;`   

`// 如果你熟悉 ES6，pi 可以使用 const 关键字，表示一个常量` 

`// const pi = 3.14;` 

`var person="John Doe";` 

`var answer='Yes I am!';`

在 2015 年以前，我们使用 var 关键字来声明 JavaScript 变量。

在 2015 后的 JavaScript 版本 (ES6) 允许我们使用 const 关键字来定义一个常量，使用 let 关键字定义的限定范围内作用域的变量。

let 是 ES6 引入的新变量声明方式，推荐使用。

let 语法：

```
let variableName = value;
```

let city = "北京";
let age = 30;
console.log(city, age); *// 输出: 北京 30*

const

const 用于定义常量，即一旦赋值后，变量的值不能再被修改。

const 语法：

```
const variableName = value;
```

const z = 10;
*// z = 20; // 报错，常量不可重新赋值*
if (true) {
  const z = 20; *// 不同的常量*
  console.log(z); *// 输出 20*
}
console.log(z); *// 输出 10*

JavaScript 没有任何打印或者输出的函数。

JavaScript 可以通过不同的方式来输出数据：

- 使用 **window.alert()** 弹出警告框。
- 使用 **document.write()** 方法将内容写到 HTML 文档中。
- 使用 **innerHTML** 写入到 HTML 元素。
- 使用 **console.log()** 写入到浏览器的控制台。

你可以弹出警告框来显示数据：

`<!DOCTYPE html>`
`<html>`
`<body>`

`<h1>我的第一个页面</h1>`
`<p>我的第一个段落。</p>`

`<script>
window.alert(5 + 6);
</script>`

`</body>`
`</html>`

如需从 JavaScript 访问某个 HTML 元素，您可以使用 document.getElementById(*id*) 方法。

请使用 "id" 属性来标识 HTML 元素，并 innerHTML 来获取或插入元素内容：

`<!DOCTYPE html>`
`<html>`
`<body>`

`<h1>我的第一个 Web 页面</h1>`

`<p id="demo">我的第一个段落</p>`

`<script>
document.getElementById("demo").innerHTML = "段落已修改。";
</script>`

`</body>`
`</html>`

以上 JavaScript 语句（在` <script> `标签中）可以在 web 浏览器中执行：

**document.getElementById("demo")** 是使用 id 属性来查找 HTML 元素的 JavaScript 代码 。

**innerHTML = "段落已修改。"** 是用于修改元素的 HTML 内容(innerHTML)的 JavaScript 代码。

在大多数情况下，我们将使用上面描述的方法来输出：

出于测试目的，您可以将JavaScript直接写在HTML 文档中：

`<!DOCTYPE html>`
`<html>`
`<body>`

`<h1>我的第一个 Web 页面</h1>`

`<p>我的第一个段落。</p>`

`<script>
document.write(Date());
</script>`

`</body>`
`</html>`

## 三、获取页面元素

JS 要想操作网页，必须先 “找到” 那个标签。 

两种最常用方法 

1.document.querySelector("选择器") 

可以通过类名、id、标签查找，最常用

`let btn = document.querySelector(".btn");` 

`let title = document.querySelector("#title");` 

2.document.getElementById("id名") 

通过 id 查找元素。

`let box = document.getElementById("box");`

## 四、事件基础

那如何能触发事件基础呢？可以通过点击，鼠标移入，加载页面各种事件来触发获取页面元素。

1. 点击

   鼠标点击时触发

   ```
   <button id="btn">点我</button>
   
   <script>
     let btn = document.querySelector("#btn");
     btn.onclick = function(){
       alert("你点击了按钮！");
     };
   </script>
   ```

2. 移入

   鼠标放上去就触发

   ```
   <div id="box">鼠标放上来</div>
   
   <script>
     let box = document.querySelector("#box");
     box.onmouseover = function(){
       box.style.color = "red";
     };
   </script>
   ```

3. 移出

   鼠标离开时触发

   ```
   <div id="box">鼠标离开我</div>
   
   <script>
     let box = document.querySelector("#box");
     box.onmouseout = function(){
       box.style.color = "black";
     };
   </script>
   ```

4. 页面加载完成

   网页一打开就自动执行

   ```
   <script>
     window.onload = function(){
       alert("网页加载完成！");
     };
   </script>
   ```

## 五、简单DOM操作

首先dom是HTML的各种标签，dom操作时js控制网页的变化。下面列举几种简单的dom操作：

1. 修改文字内容

   修改标签内容，让文字换行变标题变颜色

   ```
   元素.innerHTML = "新的内容";
   ```

   ```
   <p id="txt">原来的文字</p>
   <button onclick="changeText()">点我修改文字</button>
   
   <script>
   function changeText() {
     let t = document.querySelector("#txt");
     t.innerHTML = "我是新的文字内容";
   }
   </script>
   ```

2. 修改样式

   修改颜色大小背景等样式

   ```
   元素.style.样式名称 = "值";
   ```

   ```
   <p id="box">我会改变样式</p>
   <button onclick="changeStyle()">点我改变样式</button>
   
   <script>
   function changeStyle() {
     let b = document.querySelector("#box");
     b.style.color = "red";
     b.style.fontSize = "24px";
     b.style.backgroundColor = "pink";
   }
   </script>
   ```

3. 隐藏元素

   让元素看不见

   ```
   元素.style.display = "none";
   ```

   ```
   <p id="hide">这个内容会隐藏</p>
   <button onclick="hideBox()">隐藏内容</button>
   
   <script>
   function hideBox() {
     let h = document.querySelector("#hide");
     h.style.display = "none";
   }
   </script>
   ```

4. 显示元素

   让隐藏的元素显示出来

   ```
   元素.style.display = "block";
   ```

   ```
   <p id="show" style="display:none;">我是隐藏的内容</p>
   <button onclick="showBox()">显示内容</button>
   
   <script>
   function showBox() {
     let s = document.querySelector("#show");
     s.style.display = "block";
   }
   ```

5. 修改图片

   切换图片

   ```
   图片元素.src = "新图片路径";
   ```

   ```
   <img id="img" src="1.jpg">
   <button onclick="changeImg()">切换图片</button>
   
   <script>
   function changeImg() {
     let i = document.querySelector("#img");
     i.src = "2.jpg";
   }
   </script>
   ```

6. 添加类

   给元素添加css类

   ```
   元素.classList.add("类名");
   ```

   ```
   <style>
     .red { color: red; font-size: 24px; }
   </style>
   
   <p id="c1">添加样式类</p>
   <button onclick="add()">添加类</button>
   
   <script>
   function add() {
     let c = document.querySelector("#c1");
     c.classList.add("red");
   }
   </script>
   ```

7. 删除类

   删除元素的css类

   ```
   元素.classList.remove("类名");
   ```

   ```
   <p id="c2" class="red">删除这个类</p>
   <button onclick="remove()">删除类</button>
   
   <script>
   function remove() {
     let c = document.querySelector("#c2");
     c.classList.remove("red");
   }
   </script>
   ```

8. 切换类

   点击一次添加类，再点击一次删除类

   ```
   元素.classList.toggle("类名");
   ```

   ```
   <p id="c3">切换类样式</p>
   <button onclick="toggle()">切换</button>
   
   <script>
   function toggle() {
     let c = document.querySelector("#c3");
     c.classList.toggle("red");
   }
   </script>
   ```

9. dom的完整写法（总结）

   `// 找到元素` 

   `let 变量 = document.querySelector("#选择器");` 

   `// 绑定点击事件` 

   `变量.onclick = function() {`  

   `// 执行DOM操作`  

   `变量.innerHTML = "新内容";`  

   `变量.style.color = "blue";` 

   `};`

## 六、具体例子

运用ai生成一个运用js，HTML，css三种技术的网站：

<!DOCTYPE html> <html lang="zh-CN"> <head>     <meta charset="UTF-8">     <title>我的简单网页</title>     <style>         /* CSS：美化页面 */         body {             text-align: center;             margin-top: 100px;             background: #f0f8ff;         }          h1 {             color: #2c3e50;         }          #box {             width: 300px;             height: 150px;             background: #ffffff;             margin: 30px auto;             line-height: 150px;             border-radius: 10px;             box-shadow: 0 0 10px #ccc;         }          button {             padding: 10px 20px;             font-size: 16px;             background: #3498db;             color: white;             border: none;             border-radius: 5px;             cursor: pointer;         }          button:hover {             background: #2980b9;         }     </style> </head> <body>      <!-- HTML：页面结构 -->     <h1>我是一个简单网页</h1>     <div id="box">点下面按钮试试！</div>     <button onclick="changeText()">点我</button>      <!-- JavaScript：让网页动起来 -->     <script>         function changeText() {             document.getElementById("box").innerHTML = "你成功触发了JS！🎉";         }     </script>  </body> </html>