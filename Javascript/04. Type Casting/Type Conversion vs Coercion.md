## Conversion

### What is?

As the name implies, type conversion is the process of converting a value from a type to another.

Values in Javascript can be of different types. You could have a number, string, boolean - you name it. Sometimes, you may want to convert data from one type to another to fit certain operation.

Type conversion can either be implicit (autimatically done during code execution) or explicit (done by you the developer)

Implicit Type Conversion is also know (and more commonly referred to) as **Coercion** while Explicit Type Conversion is also know as **Type Casting.** Let's look at the these two conversions in detail.

### Implicit Type Conversion (Coercion)

There are some opertaions that you might try to execute in Javascript which are literally not possible. For example, look at the following code:
```javascript
const sum = 35 + "Hello"
```
Here, you're trying to add a number and a string. This is, practically speaking, not possible. You can only add numbers(**sum**) togetther or add strings(**concatenate**) together.

So what happenes here if you try to run the code?

Well, Javascript is a weakly typed language. Instead of Javascript throwing an error, it coerces the type of one value to fit the type other value so that the operation can be carried out.
https://www.freecodecamp.org/news/coercion-and-type-conversion-in-javascript/