# JavaScript

动态的、弱类型、*解释性*的脚本语言

## DOM(Document Object Model)

- 是对HTML的抽象表示
- 通过DOM可以访问所有的元素
- 文档加载时，浏览器会自动生成DOM

### 查找HTML元素的方法

```javascript
document.getElementById();
document.getElementsByClassName();
document.getElementsByTagName();
```

## ECMAScript

ECMAScript是JavaScript的标准

### ES6

ES6是2015年发布的版本，是ECMAScript的第六版，ES6以后ES每年发布一次新版本，修复了许多错误

## 函数与对象

### 函数定义

```javascript
function myFunction(){}
```

### 函数调用

#### input标签调用

```html
<input type = "button" onclick = {myFunction()}/>
```

#### a标签调用

```html
<a href = "javascript: myFunction()"></a>
```
