## Real life Objects, Properties, and Methods

In real life, a car is an object. a car has **properties** like weight and color, an **methods** like start and stop:

Object
**CAR**
|**Object**| **Properties**      | **Methods** |
| - | ------------------- | ----------- |
| **CAR**|car.name = Nissan   | car.start() |
| |car.model = Skyline | car.drive() |
| |car.weight = 1550kg | car.brake() |
| |car.color = gray    | car.stop()  |

All cars have the same **properties**, but the property **values** differ from car to car. All cars have the same **methods**, but the methods are perfirmed **at different times**.

Objects are variables toom but objects can contain many values.
```javascript
const car = {type: "Nissan", model: "Skyline", color: "gray"};
```
It's a common practice declare objects with the `const` keyword.
Spaces and line breaks are not important. An object definition can span multiple lines:
```javascript
const car = {
type: "Nissan",
model: "Skyline",
color: "gray"
};
```
## Properties

The name:values pairs in objects are called properties:
| Poperty | Property Value |
| ------- | -------------- |
| Type    | Nissan         |
| Model   | Skyline        |
| Year    | 1999           |
| Color   | Gray           |

You can **acess** object properties in to ways:
```javascript
// objectName.PropertyName
console.log(car.type);
// Output: Nissan

// objectName["propertyName"]
console.log(car["type"])
// Output: Nissan
```
## Methods

Objects can also have methods, methods are actions that can be performed on objects.
Methods are stored in properties as **function definitions**.

| Poperty   | Property Value                            |
| --------- | ----------------------------------------- |
| type      | Nissan                                    |
| model     | Skyline                                   |
| year      | 1999                                      |
| color     | Gray                                      |
| typeModel | function(){return this.type + " " + this.model; |

In code:
```javascript
const car = {
type: "Nissan",
model: "Skyline",
color: "gray",
typeModel: function(){
	return this.type + " " + this.model;
}
};
```
In the example above, `this` refers to the **car** object .

### What is **this**?

the `this` keyword refers to an **object**, which object depends on how this is being invoked(used or called)

|            |
| --- |
| In an objectr method, `this` refers to the **object**.  |
| Alone, `this` refers to the **global**  object.|                    
| In a function, `this` refers to the **global** object.|
| In a function, in strict mode,  `this` is `undefined`. |                          
| In an event, `this` refers to the **element** thaht received the event. |
| Methods like `call()`, `apply()`, and `bind()` can refer `this` to **any** object. |

## Do NOT

Don't use `new` to declare a var, the variable is created  as an object and they complicate your code and slow down execution speed.

```javascript
x = new String()// Declares x as a String object
y = new Number(); // Declares x as a Number object
z = new Boolean(); // Declares x as a Boolean object
```
## Object Prototype

All objects properties and methods from a prototype.

Now we use the an object constructor:
```javascript
function Car(type, model, year, color) {
	this.Type = type;
	this.Model = model;
	this.Year = year;
	this.Color = color;
}

const Car1 = new Car("Nissan", "Skyline", 1999, Gray)
```


## Prototypal Inheritance

All objects inherit properties and methods from a prototype:
- `Date` objects inherit from `Date.prototype`
- `Array` objects inherit from `Array.prototype`
- `Car` objects inherit from `Car.prototype`

The `Object.prototype` is on the top of the prototype inheritance chain:

`Date` objects, `Array` objects, and `Person` object inherit from `Object.prototype`.

### Using the `prototype` Property

`prototype` property allows you to add new properties to object to object constructors:
```javascript
function Car(type, model, year, color) {
	this.Type = type;
	this.Model = model;
	this.Year = year;
	this.Color = color;
}
Car.prototype.country = "Japan";
```

## Build-in Objects
how 