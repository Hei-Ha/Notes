### 数字每三位添加逗号
```js
String(123456789).replace(/(?<!^.*\..*)(?<=\d)((?=[^.]+\.)(?=(\d\d\d)+\.)|(?![^.]+\..*$)(?=(\d\d\d)+$))/g, ',')
```