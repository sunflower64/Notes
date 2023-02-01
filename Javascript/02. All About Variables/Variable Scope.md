Scope determines the acessibility (visibility) of variables.
Javascript has 3 types of scopes:

## Block Scope

Before ES6(2015), had only [[#Global Scope]] and [[#Function Scope]], ES6 introduced two important new Javascript keywords `let` and `const`. These two keywords provide Block Scope in Javascript.

Variables declared inside a { } block can't be accessed from outside the block:
```javascript
{
	let x = 2
}
console.log(x)
// ReferenceError: x is not defined
```
Variables declared with the `var` keyword can NOT have block scope, variables declared inside a { } block can be accessed from outside the block.
```javascript
{
	var x = 2;
}
console.log(x)
// Output: 2
```
## Local Scope

Variables declared with a function, become **LOCAL** to the function.
```javascript
function myFunction(){
	let carName = "Nissan"
	console.log(carName)
	//Nissan
}
console.log(carName)
// ReferenceError: x is not defined
```
Local variables have **Function Scope**, they can only be accessed from within the function.

Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.

Local variables are created when a function starts, an deleted when the function is completed.

## Function Scope

Each function creates a new scope.

Variables defined inside a function are not accessible (visible) from outside the function.

`var`, `let`, and `const` they all have **Function Scope**
```javascript
function myFunction(){
	var carName = "Nissan"
	const carYear = 1999
	let carKm = 75000
}
console.log(carName, carYear, carKm)
// ReferenceError: carName is not defined.
```
## Global Scope

A variable declared outside a function, becomes **GLOBAL**.
```javascript
let carName = "Nissan"
console.log(carName)
// Output: Nissan
function myFunction(){
	console.log(carName)
	// Output: Nissan
}
```