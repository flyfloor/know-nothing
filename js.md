### js

#### judge whether a function

`typeof func === 'function'` will be wrong in those circumstance:  
in Forefox, execute on html's <object> element will return function.  
in Safari, Dom NodeList type still be function.  

right way is  `Object.prototype.toString.call(fn) === "[object Function]"`


#### find out function caller type

```
function func(){
  this instanceof arguments.callee
}
```

#### time

```
date.toLocaleDateString() //2016/6/24
date.toLocaleString() //2016/6/24 下午6:34:35
date.toLocaleTimeString() //下午6:34:35
```


#### greedy DOM IDs

```
<form id="form">
    <input type="text" id="length"/>
    <input type="submit" id="submit"/>
</form>
```

```
document.getElementsByTagName("input").length
```

Under IE and opera will got `<input type="text" id="length"/>`, `document.getElementById("form").submit()` will throw an error.


#### How `==` act  

1. ReturnIfAbrupt(x).
2. ReturnIfAbrupt(y).
3. If Type(x) is the same as Type(y), then
    Return the result of performing Strict Equality Comparison x === y.
4. If x is null and y is undefined, return true.
5. If x is undefined and y is null, return true.
6. If Type(x) is Number and Type(y) is String,
    return the result of the comparison x == ToNumber(y).
7. If Type(x) is String and Type(y) is Number,
    return the result of the comparison ToNumber(x) == y.
8. If Type(x) is Boolean, return the result of the comparison ToNumber(x) == y.
9. If Type(y) is Boolean, return the result of the comparison x == ToNumber(y).
10. If Type(x) is either String, Number, or Symbol and Type(y) is Object, then
    return the result of the comparison x == ToPrimitive(y).
11. If Type(x) is Object and Type(y) is either String, Number, or Symbol, then
    return the result of the comparison ToPrimitive(x) == y.
12. Return false.

