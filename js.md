### 判断是否为函数

`typeof func === 'function'` 以下情况得不到正确的结果：  
在 Firefox 下 html 的 <object> 也会返回 function  
在 Safari 下 Dom NodeList 也是 function

所以判断是否为函数应该用 `Object.prototype.toString.call(fn) === "[object Function]"`
