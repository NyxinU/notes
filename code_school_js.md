## function expressions
### functions on the fly 
* Building functins within code execution rather than at program load time
* declared fucntions are loaded right when the program is run and held in memory until run

declared function 
``` javascript
function diffOfSquares (a,b) {
  return a*a - b*b;
}
```

function expression

only built when that line of code is reached
``` javascript 
var diff = function diffOfSquares (a,b) {
  return a*a - b*b;
};
```
* can be an anon function


