# 第168题 Excel表列名称

```javascript
/**
 * @param {number} n
 * @return {string}
 */
var convertToTitle = function(n) {
    return n > 0 ? (convertToTitle(Math.floor(n / 26)) + String.fromCharCode(64 + n % 26)) : ''; 
};
```

