# BOM(Browser Object Model)

- window
  - document
  - history
  - location
  - navigator
  - screen
  - frame

## window 对象

window对象是所有对象的顶层对象，使用时不需要显式调用

```javascript
[window.]document.getElementById();
[window.]alert();
```

## JavaScrpit事件

为了让程序对环境做出响应

鼠标、键盘、DOM、表单等事件

### 添加事件处理器的方法

#### 在DOM元素中直接绑定

```HTML
<input type="button" onclick="run()">
```

#### 在JS代码中动态绑定

```javascript
document.getElementById("demo").onclick = function(){}
```

#### 绑定事件监听函数

```javascript
document.getElementByTd("demo").addActionListener("click", ()=>{}, useCapture)
```
