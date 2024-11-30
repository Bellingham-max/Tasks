# HTML、CSS、JavaScript 学习笔记
>2.0版本信息内容主要来源于网络
>>not all written by 邱怡铭
## 学习内容的目录
- HTML
- CSS
- JavaScript

## 一、HTML（超文本标记语言）
### （一）基本结构
- `<!DOCTYPE html>`：声明文档类型为 HTML5
- `<html>`：整个 HTML 文档的根元素
- `<head>`：包含文档的元信息，如标题、样式表引用等
- `<title>`：设置文档的标题，显示在浏览器标签栏
- `<body>`：包含页面的可见内容

### （二）常用标签
- **文本标签**
    - `<h1>` - `<h6>`：标题标签，从大到小表示不同级别的标题
    - `<p>`：段落标签，用于包裹文本段落
    - `<a>`：链接标签，通过 `href` 属性指定链接目标，如: <br>`<a href="https://www.example.com">链接文本</a>`
- **列表标签**
    - `<ul>`：无序列表，子元素为 `<li>`，用于展示无顺序的项目列表
    - `<ol>`：有序列表，子元素 `<li>`，呈现有序的项目序列
- **图像标签**
    - `<img>`：通过 `src` 属性指定图像的 URL，如: <br>`<img src="image.jpg" alt="图片描述">`，`alt` 

## 二、CSS（层叠样式表）
### （一）引入方式
- **内联样式**：在 HTML 标签内使用 `style` 属性，如 `<div style="color: red;">内容</div>`。
- **内部样式表**：在 HTML 的 `<head>` 部分使用 `<style>` 标签定义样式规则，例如：
```html
<head>
  <style>
    p {
      font-size: 16px;
    }
  </style>
</head>
```
- **外部样式表**：创建一个单独的 `.css` 文件，在 HTML 中通过 `<link>` 标签引入，如:<br>`<link rel="stylesheet" href="styles.css">`。

### （二）基本选择器
- **元素选择器**：直接根据 HTML 元素名称选择，如 `p` 选择所有段落元素。
- **类选择器**：以 `.` 开头，用于选择具有特定类名的元素，例如 `.my-class` 可选择所有 `class="my-class"` 的元素。
- **ID 选择器**：以 `#` 开头，用于选择具有特定 ID 的元素，如 `#my-id` 选择 `id="my-id"` 的元素。

### （三）常见属性
- **字体相关**：`font-family`（字体家族）、`font-size`（字体大小）、`font-weight`（字体粗细）。
- **颜色相关**：`color`（文本颜色）、`background-color`（背景颜色）。
- **盒模型属性**：`width`（宽度）、`height`（高度）、`padding`（内边距）、`margin`（外边距）、`border`（边框）。

## 三、JavaScript(不同于Java)
### （一）引入方式
- **内部脚本**：在 HTML 的 `<script>` 标签内直接编写 JavaScript 代码，放在 `<head>` 或 `<body>` 中，例如：
```html
<head>
  <script>
    function sayHello() {
      alert('Hello, World!');
    }
  </script>
</head>
```
- **外部脚本**：创建一个单独的 `.js` 文件，在 HTML 中通过 `<script>` 标签引入，如 `<script src="script.js"></script>`。

### （二）基本语法
- **变量声明**：使用 `var`（ES5 及之前）、`let`（ES6 及之后，块级作用域）、`const`（ES6 及之后，常量）关键字声明变量，如 `let myVariable = 10;`。
- **数据类型**：包括数字、字符串、布尔值、数组、对象、函数等。例如 `var num = 5;`（数字），`var str = "Hello";`（字符串）。
- **函数定义**：
```javascript
function functionName(parameters) {
  // 函数体
  return value;
}
```
### （三）操作 DOM（文档对象模型）
- **选择元素**：可以使用 `document.getElementById`（通过 ID 选择元素）、`document.getElementsByClassName`（通过类名选择元素）、`document.getElementsByTagName`（通过标签名选择元素）等方法。例如 `var myElement = document.getElementById('my-id');`。
- **修改元素属性和内容**：
```javascript
myElement.style.color ='red'; // 修改元素样式
myElement.innerHTML = '新内容'; // 修改元素内部 HTML 内容
```

## 四、总结
HTML 用于构建网页的结构和内容，CSS 负责美化页面的样式，JavaScript 则为网页添加交互性和动态功能