Hoisting is Javascript default behavior of moving declarations to the top.

## Declarations are Hoisted

In Javascript, a variable can be declared after it has been used. In other words a variable can be used before it has been declared.

### Example 
```javascript
x = 5 // Assign 5 to x
console.log(x) // Display x
var x; // Declare x
```
To understand this, you have to understand the term "hoisting".

Hoisting is Javascript default behavior of moving all declarations to the top of thte current scope (to the top of the current script or the current function).

## The let and const Keywords

Variables defined with `let` and `const` are hoisted to the top of the block, but not _initialized_.

Meaning: The block of code is aware of the variable, but it can't be used until it has been declared.

### Example
```javascript
carName = "Nissan";
let carName;
//ReferenceError
```
Using a `const` variable before it is declared, is a syntax error, so the code will simply not run.
```javascript
carName = "Nissan";
let carName;
//This code will not run
```
## Initializations are Not Hoisted

Only hoists declarations, not initializations.

### Example
```javascript
var x = 5;
var y = 7;
console.log(x + " " + y);
// 5 7
```
The next example returns `Undefined` because initiliazations are not hoisted.
```javascript
var x = 5;
console.log(x + " " + y);
// 5 Undefined
var y = 7;
```
Is the same as writing:
```javascript
var x = 5;
var y;
console.log(x + " " + y);
y = 7;
```
## DECLARE YOUR VARIABLES AT THE TOP

Hoisting is (to many developers) an unknown or overlooked behavior of Javascript, if a developer doesn't understand hoisting, programs may contain bugs, to avoid bugs, always declare all variables at the beginning of every scope, since this is how Javascript interprets the code, it is always a good rule.