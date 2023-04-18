# JSON（JavaScript Object Notation）

## 特征

- 独立于语言
- 自描述
- 轻量级的数据交换格式

> 虽然JSON的语法来自于JS对象，但是独立于语言

## 语法

```json
{
  "key": "value",
  [
    {
      "key": "value",
      "number": 0,
    },
    {
      "key": "value",
      "number": 0,
    }
  ]
}
```

## JS对象与JSON对象互转

`JSON.parse([JSON Object])`, `JSON.stringify([JS Object])`

