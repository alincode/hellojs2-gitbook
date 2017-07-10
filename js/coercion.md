# 強制轉型 (coercion)

### 轉換成布林

輸入       | 結果      | 輸入     | 結果
----------|----------|----------|----------
1         | true     | 0        | false
object    | true     | undefined| false
"hi"      | true     | NaN      | false
          |          | ""       | false     
          |          | null     | false

### 轉換成數字

輸入       | 結果      | 輸入     | 結果
----------|----------|----------|----------
undefined | NaN      | number   | 原來的值
null      | 0        | string   | 原來的值
true      | 1        | object   | 表示此物件預設的代表數字
false     | 0

### 範例

**範例一**

```js
console.log(false < 1); // 答案是？
```

**範例二**

```js
// not good, why?
var b = null;
if(b == null || b == undefined || b == '') {
  console.log('flow 1');
} else{
  console.log('flow 2');
}
```

**範例三**

```js
// good job
var b = null;
if(b) {
  console.log('flow 2');
} else{
  console.log('flow 1');
}
```

**範例四**

```js
var a = {};
if(a) {
  console.log('flow 1');
} else{
  console.log('flow 2');
}
```