# HTML 学习笔记

## 一、HTML 是what
HTML就好比网页的骨架，告诉浏览器如何展示网页内容

## 二、基本结构
- `<!DOCTYPE html>`：这行代码放在最开头
- `<html>` 标签：整个网页的内容都包裹在这个标签里
- `<head>` 部分：主要放一些关于网页的信息，但不会直接在页面上显示出来。比如：
  - `<title>` 标签：设置网页的标题，会显示在浏览器的标签栏
- `<body>` 部分：这里面的内容才是我们在浏览器中真正看到的网页内容

## 三、常用标签

### （一）文本标签
- `<h1>` - `<h6>`：用来定义标题，数字越小，标题越大越重要。比如：
  - `<h1>这是一级标题</h1>`
  - `<h2>这是二级标题</h2>`
- `<p>`：代表段落，用于包裹一段文字，例如 `<p>这是一段普通的段落文字。</p>`
- `<a>`：创建链接，通过 `href` 属性指定链接的地址，如 `<a href="https://www.example.com">点击这里跳转到示例网站</a>`

### （二）列表标签
- `<ul>`：无序列表，里面的每个项目用 `<li>` 标签包裹，项目前会有小圆点。例如：
  - `<ul>
      <li>你</li>
      <li>你好</li>
    </ul>`
- `<ol>`：有序列表，同样用 `<li>` 包裹项目，项目前会有数字序号。比如：
  - `<ol>
      <li>我</li>
      <li>我好</li>
    </ol>`

### （三）图像标签
- `<img>`：用来插入图片，需要通过 `src` 属性指定图片的路径或网址，`alt` 属性用来在图片无法显示时提供文字说明。例如 `<img src="image.jpg" alt="一张图片">`

## 四、表单标签（基础部分）
- `<form>`：定义一个表单区域
- `<input>`：可以创建多种输入框，通过 `type` 属性区分。比如：
  - `type="text"` 是文本输入框，像 `<input type="text" placeholder="请输入用户名">`，`placeholder` 属性可以设置提示文字。
  - `type="password"` 是密码输入框，输入的内容会被隐藏。
  - `type="radio"` 是单选按钮，多个单选按钮如果名字相同，只能选一个，如 `<input type="radio" name="gender" value="male">男 <input type="radio" name="gender" value="female">女`。
  - `type="checkbox"` 是复选框，可以多选，如 `<input type="checkbox" name="hobby" value="reading">阅读 <input type="checkbox" name="hobby" value="music">音乐`。
- `<textarea>`：创建多行文本输入区域，比如 `<textarea rows="4" cols="30">在这里输入多行文字...</textarea>`，`rows` 和 `cols` 可以设置行数和列数。
- `<button>`：创建按钮，`type="submit"` 时可以用来提交表单，如 `<button type="submit">提交表单</button>`

