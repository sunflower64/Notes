## The concept of Data Types

In programming data types is an important concept, to be able to operate on variables, it's important to know something about the type, without data types a computer can't safely solve this.
```javascript
let x = 18 + "Nissan";
```
Does it make any sense to add `"Nissan"` to sixteen? Will it produce an error or will it produce a result? Javascript will treat the example above as:
```javascript
let x = "18" + "Nissan";
```
Javascript evaluates expressions left to right. Different sequences can produce different results:
```javascript
let x = 18 + 4 + "Nissan";
console.log(x)
// Output: 22Nissan
let y = "Nissan" + 18 + 4;
console.log(y)
// Output: Nissan184
```
## Types are dynamic

Javascript has dynamic types. This means that the same variable can be used to hold different data types:
```javascript
let x; // Now x is undefined
x = 5; // Now x is Number
x = "John" // Now x is String
```
## String

A string (text string) is a series of characters like "John Doe". Strings are written with quotes, you can use single or double quotes:
```javascript
// Using double quotes:
let carName1 = "Nissan"
// Using single quotes:
let carName2 = "Toyota"
```
You can use quotes inside a string, as long as they don't match the quotes surrounding the string:
```javascript
// Single quote inside double quotes:
let answer1 = "It's alright"
// Single quotes inside double quotes:
let answer2 = "He is called 'Jhonny'"
// Double quotes inside single quotes:
let answer3 = 'He is called "Jhonny"'
```
## Number

Numbers are stored as decimal numbers (floating point), numbers can be written with, or without decimals:
```javascript
// With decimals:
let x1 = 34.00;

// Without decimals:
let x2 = 34;
```
### Exponential Notation

Extra large or extra small nymbers can be written with scientific (exponential) notation:
```javascript
let y = 123e5; // 12300000
let z = 123e-5; // 0.00123
```
### Note

Most programming languages have many number types:

Whole numbers (intergers):
byte (8-bit), short (16-bit), int (32-bit), long (64-bit).

Real numbers (floating-point):
float (32-bit), double (64-bit).

**Javascript are always one type:
double (64-bit floating point)**

## BigInt

All Javascript numbers are stored in a 64-bit floating-point format, BigInt is a new datatype (2020) that can be used to store iterger values that are too big to be represented by a normal Javascript Number.
```javascript
let x = BigInt("123456789012345678901234567890")
```

## Boolean

Booleanes can only have two values:
`true` or `false`.

```javascript
let x = 5;
let y = 5;
let z = 6;

(x == y) // Returns true
(x == z) // Returns false
```
Booleans are often used in conditional testing.

## Undefined

A variable without a value, has the value undefined. This thype is also `undefined`.
```javascript
let car; //Value is undefined, type is undefined
```

## Null


## Symbol

ES6 introduced a new primitive data type called `symbol`. Symbols are immutable (can't be changed) and are unique:
```javascript
// Two symbols with the same description
const value1 = Symbol('hello');
const value2 = Symbol('hello');
console.log(value1 = value2)
// Output: False
```
### Creating and accessing a Symbol

```javascript
const x = Symbol('Nissan')
console.log(x.description)
// Output: Nissan
```
### The benefits of using Symbols

In a program, even if the same name is used to store values, the `Symbol` data type will have a unique value.