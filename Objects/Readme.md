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

#### 1.8 Setting new key for an Object

An object is a mutable data structure and we can modify the content of an object after it gets created.

```js
var person = {
  firstName: "Rahul",
  lastName : "Singh",
  id       : 1,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

// Setting a new key here
person.country = 'India'
person.title = 'Engineer'
person.isMarried = true

// also you create complete new function as key
person.getPersonInfo = function() {
    let statement = `${fullName} is a ${this.title}.\nHe lives in ${this.country}.\nHe ${isMarried ? 'Married' : 'Not Married'}.`
    return statement
}
```
#### 1.9 Different Object Methods Available

```js
var person = {
  firstName: "Rahul",
  lastName : "Singh",
  id       : 1,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

// Object methods
1. Object.assign
2. Object.values
3. Object.entries
4. Object.hasOwnProperty()

// Let's use object.assign to assign whole value

const clonePerson = Object.assign({}, person)
```

###### 1.9.1 Getting object keys 

Object.keys: To get the keys or properties of an object as an array

```js
Object.keys(clonePerson)
// Output
['firstName', 'lastName', 'id', 'fullName']
```

hasOwnProperty: To check if a specific key or property exist in an object

###### 1.9.2 Checking properties using hasOwnProperty()

hasOwnProperty: To check if a specific key or property exist in an object

```js
copyPerson.hasOwnProperty('firstName')

// Output
true
```

### Some style guide

##### 1.10 Use the literal syntax for object creation `eslint`

```js
// bad
const item = new Object(); 

// good
const item = {};
```

##### 1.11 Use computed property names when creating objects with dynamic property names.

Why? They allow you to define all the properties of an object in one place.

```js
function getKey(k) {
  return `a key named ${k}`;
}

// bad
const obj = {
  id: 5,
  name: 'San Francisco',
};
obj[getKey('enabled')] = true;

// good
const obj = {
  id: 5,
  name: 'San Francisco',
  [getKey('enabled')]: true,
};
```

#### 1.12 Use object method shorthand.

```js
// bad
const atom = {
  value: 1,

  addValue: function (value) {
    return atom.value + value;
  },
};

// good
const atom = {
  value: 1,

  addValue(value) {
    return atom.value + value;
  },
};
```

##### 1.13 Group your shorthand properties at the beginning of your object declaration.

Why? It’s easier to tell which properties are using the shorthand.


```js
const anakinSkywalker = 'Anakin Skywalker';
const lukeSkywalker = 'Luke Skywalker';

// bad
const obj = {
  episodeOne: 1,
  twoJediWalkIntoACantina: 2,
  lukeSkywalker,
  episodeThree: 3,
  mayTheFourth: 4,
  anakinSkywalker,
};

// good
const obj = {
  lukeSkywalker,
  anakinSkywalker,
  episodeOne: 1,
  twoJediWalkIntoACantina: 2,
  episodeThree: 3,
  mayTheFourth: 4,
};
```

##### 1.14 Only quote properties that are invalid identifiers.

Why? In general we consider it subjectively easier to read. It improves syntax highlighting, and is also more easily optimized by many JS engines.

```js
// bad
const bad = {
  'foo': 3,
  'bar': 4,
  'data-blah': 5,
};

// good
const good = {
  foo: 3,
  bar: 4,
  'data-blah': 5,
};
```


🍻🎉💊 Congrats for completing **Day 3** 🍻🎉💊

if you are preparing for interview have a look at [interview questions of Objects](./InterviewQuestion.md) 
