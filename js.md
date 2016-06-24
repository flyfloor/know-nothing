### judge whether a function

`typeof func === 'function'` will be wrong in those circumstance:  
in Forefox, execute on html's <object> element will return function.  
in Safari, Dom NodeList type still be function.  

right way is  `Object.prototype.toString.call(fn) === "[object Function]"`


### find out function caller type

```
function func(){
  this instanceof arguments.callee
}
```

### time

```
date.toLocaleDateString() //2016/6/24
date.toLocaleString() //2016/6/24 下午6:34:35
date.toLocaleTimeString() //下午6:34:35
```
