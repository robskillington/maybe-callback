maybe-callback
==============

Maybe call a callback if it really is who it says it is


## Usage
```js
var maybeCallback = require('maybe-callback');
 
function callback(arg) {
    return arg + 1;
}

maybeCallback(callback)(1);  //=> 2
maybeCallback(null)(1);  //=> undefined

var once = maybeCallback.once(callback);
once(1); //=> 2
once(1); //=> undefined
```
