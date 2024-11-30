# CSS 学习笔记

## 一、CSS 基础概念
- CSS 即层叠样式表，用于控制网页的样式和布局，使网页内容呈现出丰富多样的外观效果


## 二、选择器类型

### （一）元素选择器
- 直接使用 HTML 元素名称作为选择器，会选中页面中所有该类型的元素。
  - 示例：
```css
p {
  line-height: 1.5;
}
```


### （二）类选择器
- 以 `.` 开头，后面跟着自定义的类名。可以为多个不同的元素添加相同的类名来共享样式。
  - 示例：
```css
.highlight {
  background-color: yellow;
}
```


### （三）ID 选择器
- 以 `#` 开头，后面跟着唯一的 ID 名称。ID 在页面中应该是唯一的，用于精准定位某个特定元素。
  - 示例：
```css
#header {
  text-align: center;
  font-weight: bold;
}
```
- 对应 HTML 中的 `<div id="header">` 元素会使文本居中并加粗。

### （四）后代选择器
- 用于选择某个元素的后代元素。用空格分隔选择器。
  - 示例：
```css
article p {
  font-family: Arial, sans-serif;
}
```
- 表示选择在 `<article>` 元素内部的所有 `<p>` 段落元素，并设置字体。

### （五）伪类选择器
- 如 `:hover`（鼠标悬停）、`:active`（元素被激活时）、`:visited`（链接被访问后）等，用于为元素在特定状态下添加样式。
  - 示例：
```css
a:hover {
  color: red;
}
```
- 当鼠标悬停在链接（`<a>`）上时，文字颜色变为红色。

## 三、常见属性

### （一）字体属性
- `font-family`：指定字体类型，如 `font-family: "Times New Roman", serif;`。
- `font-size`：设置字体大小，可以是像素值（`px`）、相对单位（`em`、`rem`）等，如 `font-size: 12px;`。
- `font-weight`：控制字体粗细，如 `font-weight: bold;` 或使用数字值表示（`400` 为正常，`700` 为加粗）。

### （二）文本属性
- `color`：设置文本颜色，如 `color: #333;`（十六进制颜色代码）。
- `text-align`：文本对齐方式，有 `left`（左对齐）、`right`（右对齐）、`center`（居中对齐）等，如 `text-align: center;`。
- `text-decoration`：用于添加或去除文本装饰，如 `text-decoration: underline;`（下划线）。

### （三）背景属性
- `background-color`：设置元素背景颜色，如 `background-color: #f0f0f0;`。
- `background-image`：设置背景图片，如 `background-image: url('image.jpg');`。
- `background-repeat`：控制背景图片的重复方式，有 `repeat`（重复）、`no-repeat`（不重复）、`repeat-x`（水平重复）、`repeat-y`（垂直重复）等。

### （四）盒模型属性
- `width` 和 `height`：设置元素的宽度和高度，可以是固定值或百分比，如 `width: 200px; height: 100px;`。
- `padding`：内边距，用于在元素内容和边框之间添加空间，如 `padding: 10px;`（四个方向均为 10px）或 `padding: 5px 10px 15px 20px;`（上 5px、右 10px、下 15px、左 20px）。
- `margin`：外边距，控制元素与周围元素的间距，用法与 `padding` 类似，如 `margin: 20px;`。
- `border`：边框，可以设置边框的宽度、样式和颜色，如 `border: 1px solid black;`。

### （五）布局属性
- `display`：用于控制元素的显示方式，常见的值有 `block`（块级元素）、`inline`（内联元素）、`inline-block`（既具有内联元素特点又具有块级元素特点）、`none`（元素不显示）等。
- `float`：使元素向左或向右浮动，如 `float: left;`，常用于实现多列布局，但使用后可能需要清除浮动。
- `position`：确定元素的定位方式，有 `static`（默认值，正常文档流）、`relative`（相对定位）、`absolute`（绝对定位）、`fixed`（固定定位）等，不同的定位方式会影响元素在页面中的位置计算。

## 四、样式的层叠与优先级
- 当多个样式规则应用于同一个元素时，会根据选择器的优先级来确定最终的样式。一般来说，ID 选择器优先级高于类选择器，类选择器优先级高于元素选择器。内联样式的优先级最高。
- 可以使用 `!important` 关键字来强制某个样式属性具有最高优先级，但应谨慎使用，以免造成样式难以修改和维护。

