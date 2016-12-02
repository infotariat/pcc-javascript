# W3Schools OOP JavaScript

## Basics of JavaScript Objects

### Real life objects, properties, and methods
In real life, a car is an *object*.

A car has *properties* like weight and color, and *methods* like start and stop.
```javascript
// properties
car.name = 'Fiat';
car.model = '500';
car.weight = '850 kg';
car.color = 'white';

// methods
car.start();
car.drive();
car.brake();
car.stop();
```

All cars have the same properties, but the property values differ from car to car.

All cars have the same methods, but the methods are performed at different times.

### JavaScript objects
We have already learned that JavaScript variables are containers for data values.

This code assigns a *simple value* (Fiat) to a *variable* named **car**:
```javascript
var car = 'Fiat';
```

Objects are variables too. But objects can contain many values.

This code assigns *many values* (Fiat, 500, white) to a *variable* named **car**:
```javascript
var car = {type: 'Fiat', model: '500', color: 'white'};
```

The values are written as *name:value pairs* (name and value separated by a colon). JavaScript objects are containers for *named values*.

### Object properties
The name:value pairs in JavaScript objects are called *properties*.
```javascript
var person = {firstName: 'John', lastName: 'Doe', age: 50, eyeColor: 'blue'};
```

| Property | Property Value |
| :------- | :------------- |
| firstName | John |
| lastName | Doe |
| age | 50 |
| eyeColor | blue |


### Object methods
Methods are *actions* that can be performed on objects.

Methods are stored in properties as *function definitions*.

| Property | Property Value |
| :------- | :------------- |
| firstName | John |
| lastName | Doe |
| age | 50 |
| eyeColor | blue |
| fullName | **function()** *{return this.firstName+this.lastName;}* |

JavaScript objects are containers for named values called properties or methods.

### Object definition
You define (and create) a JavaScript object with an object literal:

```javascript
var person = {firstName: 'John', lastName: 'Doe',
             age: 50, eyeColor: 'blue'};
```
Spaces and line breaks are not important. An object definition can span multiple lines:
```javascript
var person = {
    firstName:'John',
    lastName:'Doe',
    age:50,
    eyeColor:'blue'
};
```

### Accessing object properties
You can access object properties in two ways:

```javascript
objectName.propertyName
```
or

```javascript
objectName["propertyName"]
```

##### Examples
```javascript
person.lastName;
person['lastName'];
```

### Accessing object methods
You can access an object method with the following syntax:
```javascript
objectName.methodName()
```

### Example
```javascript
name = person.fullName();
```

If you access the **fullName** method *without ()*, it will return the *function definition*:
```javascript
name = person.fullName;
```

A method is actually a function definition stored as a property value.

### Do not declare strings, numbers, or booleans as objects!!
When a JavaScript variable is declared with the keyword **new**, this variable is created as an object:
```javascript
var x = new String(); // Declares x as a String object
var y = new Number(); // Declares y as a Number object
var z = new Boolean(); // Declares z as a Boolean object
```
Avoid **String**, **Number**, and **Boolean** objects. They complicate your code and slow down execution speed.

## Object Definitions

### JavaScript Objects
In JavaScript, objects are king. If you understand objects, you understand JavaScript.

In JavaScript, *almost* everything is an object.
* Booleans can be objects (or primitive data treated as objects)
* Numbers can be objects (or primitive data treated as objects)
* Strings can be objects (or primitive data treated as objects)
* Dates are *always* objects
* Maths are *always* objects
* Regular expressions are *always* objects
* Arrays are *always* objects
* Functions are *always* objects
* Objects are objects

In JavaScript all values, except primitive values, are objects. Primitive values are strings ('John Doe'), numbers (3.14), true, false, null, and undefined.

### Objects are variables containing variables
JavaScript variables can contain single values:
```javascript
var person = 'John Doe';
```
Objects are variables too. But an object can contain many values. Again, tehse values are stored as *key:value* pairs. A JavaScript object is a *collection of named values*. Objects written as name:value pairs are similar to:
* Associative arrays in PHP
* Dictionaries in Python
* Hash tables in C
* Hash maps in Java
* Hashes in Ruby and Perl

### Object methods
Methods are *actions* that can be performed on objects. Object properties can be both primitive values, other objects, and functions. An *object method* is an object property containing a *function definition*. JavaScript objects are containers for named values, called *properties* and *methods*.

### Creating a JavaScript object
With JavaScript, you can define and create your own objects.

There are different ways to create new objects:
* Define and create a single object, using an *object literal*.
* Define and creaet a single object with the keyword **new**.
* Define an *object constructor*, and then create objects of the constructed type.
* In **ECMAScript 5**, an object can also be created with the function **Object.create()**.

### Using an object literal
This is the easiest way to create a JavaScript object.

Using an *object literal*, you both define and create an object in one statement. An object literal is a list of name:value pairs (such as **age:50;**) inside curly braces **{}**. The following example creates a new JavaScript object with four properties:
```javascript
var person = {firstName:'John', lastName:'Doe', age:50, eyeColor:'blue'};
```

### Using the JavaScript keyword new
This example will also create the aforementioned obejct:
```javascript
var person = new Object();
person.firstName = 'John';
// etc.
```

The two examples above do exaactly the same thing. There is no need to use **new Object()**. For simplicity, readability, and execution speed, use the first one (the *object literal* method).

### Using an object constructor
