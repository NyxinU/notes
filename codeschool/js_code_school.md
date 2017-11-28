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

### Closure 
* returned a function from a function and complete with varible that showed up in the external function
* closure wraps up an entire environemtn, binding necessary variables from other scopes
* can be used to make very similar functions
* function that makes a ticket and is passed the method of transportation
* have a passenger tracker in the ticket maker




