Inside the computer's world, there is only data. You can read data, modify data, create new data. All this data is stored as long sequences of bits.

Bits are any kind of two-valued things, usually described as zeros and ones. 

13 in bits.
| 0 | 0 | 0 |  0 | 1 | 1 | 0 | 1 | 
|-|-|-|-|-|-|-|-|
|128|64|32|16|8|4|2|1

So that's the binary number 00001101. It's non-zero digits stand for 8, 4, and 1, and add up to 13.

## VALUES

To separete large quantities of bits without getting lost, we must separete them into chunks thata represent pieces of information.
In a Javascript enviroment, those chunks are called _values_. Though all values are made of bits, they play different roles. Every value has a type that determines its role. Some values are numbers, some values are pieces of text, some values are functions, and so on.

To create a value, you just merely invoke its name.

### NUMBERS

Values of the _number_ type are, usurprisingly, numeric values. In a Javascript program, they are written as follows:
```javascript
13
```
Fractional numbers are written by using a dot.
```javascript
9.81
```
For very big or very small numbers, you also use notation by adding an e (for _exponent_), followed by the exponent of the number.
```javascript
2.998e8
```
	That is 2.988 x 10⁸ = 299,800,000.

The important thing is to be aware of it
and treat fractional digital numbers as approximations, not as precise
values.

#### Aritmetic
The main thing to do with numbers is arithmetics. This take two numbers values and produce a new number from them.

```javascript
(100 + 4) * 11
```
| Operator | Description |
| - | -|
| + | Addition |
| - | Substraction |
| * | Multiplication |
| ** | Exponentiation |
| / | Division |
| % | Modulus |
| ++ | Increment |
| -- | Decrement |

#### Special Numbers 
There are three special values in Javascript thata are considered numbers but don't behave like normal numbers.

The first two are Infinity and -Infinity, which represent the positive and negative infinities.

The other special number is NaN stands for "not a number", even  though it _is_ a value of the number type. You'll get this number, for example, try to calculate 0 / 0. Infinity - Infinity or any number of other numerical operations that don't yield a meaningful result.

### Strings
The next basic data type is the _string_. Strings are used to represent text. They are written by enclosing their content in quotes.
```javascript
`Down on the sea`
"Lie on the ocean"
'Float on the ocean'
```
Few characters are more difficult, you can imagine how putting quotes between quotes might be hard. _Newlines_
can be included without escaping only when the string is quoted  with backticks (`).

To make it possible to include such characters in a string, the following notation is used: whenever a backslash (\\\) is found sinside quoted text, it indicates that the character after it has a special meaning. This is called _escaping_ the character. A quote that is preceded by a backslash will not end the string but be part of it. When an `n` character occurs after a backslash, it is interpreted as a newline. Similarly, a `t` after a backslash means a tab character. 