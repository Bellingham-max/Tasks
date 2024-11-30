# JavaScript 学习笔记
>跟Java有一点点像

## 一、JavaScript 是what
JavaScript 为网页添加动态的语言

## 二、引入方式
1. **内部脚本**：在 HTML 文件的 `<script>` 标签内直接编写 JavaScript 代码，通常放在 `<body>` 部分的末尾或者 `<head>` 部分。例如：
```html
<head>
  <script>
    function sayHello() {
      alert('Hello, World!');
    }
  </script>
</head>
```
2. **外部脚本**：创建一个单独的 `.js` 文件，在 HTML 文件中通过 `<script>` 标签引入，例如：
```html
<head>
  <script src="script.js"></script>
</head>
```

## 三、基本语法

### （一）变量声明
- 使用 `var`（ES5 及之前常用）、`let`（ES6 引入，块级作用域）、`const`（ES6 引入，声明常量）关键字声明变量。
  - 示例：
```javascript
var num = 5;
let str = 'Hello';
const PI = 3.14;
```

### （二）数据类型
- **基本数据类型**：
  - 数字（Number）：包括整数和小数，如 `10`、`3.14`。
  - 字符串（String）：用单引号或双引号括起来的字符序列，如 `'JavaScript'`、`"Hello"`。
  - 布尔值（Boolean）：只有 `true` 和 `false` 两个值。
  - 空值（Null）：表示空对象指针。
  - 未定义（Undefined）：当变量声明但未赋值时，其值为 `Undefined`。
- **复杂数据类型**：
  - 数组（Array）：用于存储多个值，可以通过索引访问，如 `let arr = [1, 2, 3];`，`arr[0]` 表示第一个元素 `1`。
  - 对象（Object）：由键值对组成，如 `let person = { name: 'John', age: 25 };`，可以通过 `person.name` 访问 `'John'`。

### （三）函数定义
- 函数使用 `function` 关键字定义，可以有参数和返回值。
  - 示例：
```javascript
function add(a, b) {
  return a + b;
}
```

## 四、操作 DOM（文档对象模型）
- 可以通过 JavaScript 操作 HTML 页面中的元素，实现动态更新页面内容等功能。
- **选择元素**：
  - `document.getElementById('id')`：根据元素的 ID 选择元素。
  - `document.getElementsByClassName('class')`：根据类名选择元素，返回一个类似数组的对象。
  - `document.getElementsByTagName('tag')`：根据标签名选择元素，返回类似数组对象。
- **修改元素属性和内容**：
  - 示例：
```javascript
let myElement = document.getElementById('myDiv');
myElement.style.color ='red'; // 修改元素颜色
myElement.innerHTML = '新的内容'; // 修改元素内部 HTML 内容
```

## 五、控制结构
- **条件语句**：
  - `if...else` 语句：根据条件判断执行不同的代码块。
  - 示例：
```javascript
let num = 10;
if (num > 5) {
  console.log('大于 5');
} else {
  console.log('小于等于 5');
}
```
- **循环语句**：
  - `for` 循环：用于重复执行一段代码一定次数。
  - 示例：
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
  - `while` 循环：在条件为真时重复执行代码。
  - 示例：
```javascript
let i = 0;
while (i < 3) {
  console.log(i);
  i++;
}
```

## 六、事件处理
- 当事件发生时执行相应的 JavaScript 代码，例如，为按钮添加点击事件：
```javascript
let button = document.getElementById('myButton');
button.addEventListener('click', function() {
  alert('按钮被点击了');
});
```

 