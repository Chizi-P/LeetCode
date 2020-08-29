# 第557题 反转字符串中的单词 III

```javascript
/**
 * @param {string} s
 * @return {string}
 */
var reverseWords = function(s) {
    return s.split(' ').map(e => [...e].reverse().join('')).join(' ');
};
```

