## 1. Javascript Data Types

JavaScript variables can hold many data types: numbers, strings, objects and more:

```js
var length = 10;
var firstName = 'Rahul';

var xyz = {firstName: 'Rahul', lastName: 'Singh'}

```

### 1.2 Concept of Data Types

In programming, data types is an important concept.
To be able to operate on variables, it it important to know something about the type.

### 1.3 Primitive Data Types

|  Data Type  |  Description                       |
|-------------|------------------------------------|
|  String     | sequence of characters "hello"     |
|  Number     | numeric values 100                 |
|  Boolean    | either false or true               |
|  Undefined  | represents undefined value         |
|  Null       |  represents null (no value at all) |

### 1.4 Non-Primitive Data Types

| Data Type   |  Description                                |
|-------------|---------------------------------------------|
|  Object     | instance through which member can access    |
|  Array     | group of similar values                      |
|  RegExp    | regular expression                           |


Without data types, a computer connot safely solve this:

```js
var makeSense = 16 + "Car"
```

Does it make any sense to add `Car` to `16`? More importantly will it *produce an error or result?*

The pretiness of javascript, it will treat above examples as :

```js
var makeSense = "16" + "Car"

// Output
"16Car"
```

### 1.5 Javascript Types are Dynamic

JavaScript has dynamic types. This means that the same variable can be used to hold different data types:

```js
var x           // x is undefined
x = 5;          // x is number
x = "Rahul"     // x is string
```

### 1.6 Strings

A string (or a text string) is a series of characters like "Rahul". Strings are written with quotes. You can use single or double quotes:

```js
var marvelName = "Scarlett Witch"
var marvelName2 = 'Wanda Maximoff" 
```

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

```js
var answer1 = "It's alright";             // Single quote inside double quotes
var answer2 = "He is called 'Johnny'";    // Single quotes inside double quotes
var answer3 = 'He is called "Johnny"';    // Double quotes inside single quotes
```

### 1.7 Numbers

JavaScript has only one type of numbers. Numbers can be written with, or without decimals:

```js
var x1 = 34.00;     // Written with decimals
var x2 = 34;        // Written without decimals
```

Extra large or extra small numbers can be written with scientific (exponential) notation:

```js
var y = 123e5;      // 12300000
var z = 123e-5;     // 0.00123
```

### 1.8 Booleans

Booleans can only have two values: `true` or `false`. Booleans are often used in conditional testing.


```js
var x = 5;
var y = 5;
var z = 6;
(x == y)       // Returns true
(x == z)       // Returns false

var x = null
!!x            // Return false

x = 5
!!x            // Return True

// this one is very handy in react project
```

### 1.9 Arrays

JavaScript arrays are written with square brackets. Array items are separated by commas.

```js
var ecommerce_site = ["Amazon", "Flipkart", "Ebay", "Bewkoof"]
```

Array indexes are zero-based, which means the `first item is [0], second is [1]`, and so on.

### 1.10 Objects

JavaScript objects are written with curly braces `{}`. Object properties are written as `name:value pairs, separated by commas`.

```js
var person = {firstName:"Rahul", lastName:"Singh", age:21, eyeColor:"black", sex:"Male"};
```

The object (person) in the example above has 5 properties: firstName, lastName, age, and eyeColor, sex.

### 1.11 `typeof` Operator

You can use the JavaScript `typeof` operator to find the type of a JavaScript variable.

```js
typeof ""             // Returns "string"
typeof "John"         // Returns "string"
typeof "John Doe"     // Returns "string"
typeof 0              // Returns "number"
typeof 314            // Returns "number"
typeof 3.14           // Returns "number"
typeof (3)            // Returns "number"
typeof (3 + 4)        // Returns "number"
```

### 1.12 Undefined

In JavaScript, a variable without a value, has the value `undefined`. The type is also `undefined`.

```js
var Hotel;    // Value is undefined, type is undefined
```

Any variable can be emptied, `by setting the value to undefined`. The type will also be undefined.

```js
var Hotel = undefined   // Value is undefined
```

### 1.13 Empty Values

An `empty value` has nothing to do with `undefined`. An `empty string` has both a `legal value and a type`.

```js
var hotel = "";    // The value is "", the typeof is "string"
```

### 1.14 Null

In JavaScript null is `"nothing"`. It is supposed to be something that doesn't exist Unfortunately, in JavaScript, the `data type of null is an object`.

```js
var person = {firstName:"Rahul", lastName:"Singh", age:21, eyeColor:"black", sex:"Male"};
person = null;      // Now value is null, but data type is still an object
```

### 1.15 Difference between Undefined and Null

`undefined` and `null` are equal in value but different in type:

```js
typeof undefined           // undefined
typeof null                // object

null === undefined         // false
null == undefined          // true
```

### 1.16 Complex Data

The `typeof` operator can return one of two complex types:

1. function
2. object

The `typeof` operator `returns "object"` for objects, arrays, and null.

The `typeof` operator `does not return "object"` for functions.

```js
typeof {name:'John', age:34} // Returns "object"
typeof [1,2,3,4]             // Returns "object" (not "array", see note below)
typeof null                  // Returns "object"
typeof function myFunc(){}   // Returns "function"
```
