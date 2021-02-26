<div align="center">
  <h1> Javascript Objects 😹️ </h1>
 </div>

#### 1. Objects, Properties, and Methods

Let's see a `real life example:`

In real life, a car is an **object**.

A car has properties like `weight` and `color`, and *methods* like `start` and `stop`:

##### 1.1.1 Car Properties

```js
car.name = 'Fiat'
car.model = 500
car.weight = 850kg
car.color = 'white'
```

##### 1.1.2 Car Methods

```js
car.start()
car.drive()
car.brake()
car.stop()
```

All cars have the same `properties`, but the property values differ from `car to car`.

All cars have the same methods, but the methods are performed **at different times**.

#### 1.2 Defination Objects 

JavaScript objects are containers for named values called properties or methods.

```js
var car = { type: "Fiat", model: "500", color: "white" }
```

You define (and create) a JavaScript object with an object literal:

```js
var person = {firstName:"Rahul", lastName:"Singh", age:15, eyeColor:"black"};
```

#### 1.3 Accessing Object Properties

You can access object properties in two ways:

```js
objectName.propertyName

// To avoid nullish error
objectName?.propertyName
```

or

```js
objectName['propertyName']
```

#### 1.4 Object Methods

- Objects can also have methods.

- Methods are actions that can be performed on objects.

- Methods are stored in properties as function definitions.

`A method is a function stored as a property.` Example:

```js
var person = {
  firstName: "Rahul",
  lastName : "Singh",
  id       : 1,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

#### 1.5 The `this` keyword

- In a function definition, this refers to the `"owner"` of the function.

- In the example above, this is the `person object` that `"owns"` the `fullName` function.

- In other words, `this.firstName` means the firstName property of this object.

#### 1.6 Accessing Object Methods

You access an object method with the following syntax:

```js
objectName.methodName()

let name = person.fullName();
// Output - From above example
Rahul Singh
```

#### 1.7 Do not declare strings, Numbers, and Booleans as Objects

When a JavaScript variable is declared with the keyword `"new"`, the variable is created as an object:

```js
var x = new String();        // Declares x as a String object
var y = new Number();        // Declares y as a Number object
var z = new Boolean();       // Declares z as a Boolean object
```

Avoid `String`, `Number`, and `Boolean objects`. They complicate your code and slow down execution speed.




🍻🎉💊 Congrats for completing **Day 3** 🍻🎉💊

if you are preparing for interview have a look at [interview questions of Objects](./InterviewQuestion.md) 
