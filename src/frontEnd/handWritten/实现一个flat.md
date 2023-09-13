## 实现一个 flat

### 方法一：

```javascript
const flat2 = (arr, n) => {
    if (n <= 0) return arr;
    if (!Array.isArray(arr)) return arr;
    let result = [];
    for (let i = 0; i < arr.length; i++) {
        result = result.concat(flat2(arr[i]));
    }
    return result;
}
```

### 方法二：

```javascript
const flat3 = (arr) => {
    if (!Array.isArray(arr)) return arr;
    return arr.reduce((pre, cur) => {
        return pre.concat(flat3(cur));
    }, [])
}
```