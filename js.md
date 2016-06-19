### judge whether a function

`typeof func === 'function'` will be wrong in those circumstance:  
in Forefox, execute on html's <object> element will return function.  
in Safari, Dom NodeList type still be function.  

right way is  `Object.prototype.toString.call(fn) === "[object Function]"`
