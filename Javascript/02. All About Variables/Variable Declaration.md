
Creating a variable in Javascript is called "declaring" a variable, you declare a Javascript variable with `var` or `let` keywords.

### What are variables?

Variables are containers for storing data (soting data values) example:
```javascript
const name = "Esteban";
let age = 20;
```
### When to use `var`?

The `var` keyword is used in all Javascript code from 1995 to 2015. `let` and `const` keywords were added to Javascript in 2015, if you want your code to run in older browsers, you must use `var`.

### When to use `const`?

If you want a general rule, always declare variables with `const`. If you think the value of the variable can change, use `let`.

### Assignment Operator
 
In Javascript, the equal sign `=` is an "assignment" operator, not an "equal to" operator. The equal to operator is `==`

### Variable Declaration

You declare a Javascript variable with the `var` or `let` keyword:
```javascript
var carName;
let carName;
```
After the declaration the variable has no valuable, technically it is `undefined`, to assign a value to the variable use the equal sign.

```javascript
carName = "Nissan"
```
You can also assign a value to the variable when you declare it:
```javascript
let carName = "Nissan"
console.log(carName)
// output: Nissan
```
You can declare many variables in one statement start the statement whith a varible keyword and separete the variables with comma:
```javascript
let person = "Esteban", carName = "Nissan", price = 200;
```
You also can span multiple lines:
```javascript
let person = "Esteban",
	carName = "Nissan",
	price = 200;
```
## Value = undefined

In computer programs, variables are often declare without a value. The value can be calculated be something that has to be calculated, or something that will be provided later, like user input.

A variable declared without a value will have the value `undefined`. The variable carName will have the value `undefined` after the execution of this statement:
```javascript 
let carName;
```