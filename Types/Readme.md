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

#### 1.6.1 String Methods

```js
let string = 'JavaScript'
let firstLetter = string[0]                 // J

// toUpperCase()
let string = 'JavaScript'
string.toUpperCase()                        // JAVASCRIPT

// toLowerCase()
let string = 'JavasCript'
string.toLowerCase()                        // javascript

// substr()
let string = 'JavaScript'
string.substr(4,6)                          // Script

// substring()
let string = 'JavaScript'
string.substring(0,4)                       // Java

// split()
let string = '30 Days Of JavaScript'
string.split()                              // Changes to an array -> ["30 Days Of JavaScript"]
string.split(' ')                           // Split to an array at space -> ["30", "Days", "Of", "JavaScript"]

// includes()
let string = '30 Days Of JavaScript'
string.includes('Days')                     // true
string.includes('days')                     // false - it is case sensitive!

// charAt()
let string = '30 Days Of JavaScript'
string.charAt(0)                            // 3

// search()
let string = 'I love JavaScript. If you do not love JavaScript what else can you love'
string.search('love')                       // 2
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

### 1.17 Math Object

Javascript also provide Math object with lot of methods to work with numbers;

```js
Math.PI                     // 3.1415
Math.round(PI)              // 3 to the ground values
Math.round(9.91)            // 10 nearest ground values

Math.min(-5,3,4,20)         // -5
Math.max(-5,3,5,20)         // 20

Math.random()               // generate random 0 to 0.9999 value

Math.abs(-10)               // 10
Math.sqrt(100)              // 10

Math.pow(3,2)               // 9 i.e 3 power 2
Math.E                      // 2.178

Math.log(2)                 // 0.69314
Math.log(10)                // 2.3025

Math.sin(0)                 // 0
Math.sin(60)                // -0.3048

```

### 1.18 String Concatention

Connecting two or more strings together is called concatenation. Using the strings declared in the previous String section:

```js
let first_name = 'Gandhi'
let last_name = 'Rahul'

let full_name = last_name + first_name
'Rahul Gandhi'
```

### 1.19 Template Strings/Literals

To create a template strings, we use `two back-ticks`. We can inject data as expressions inside a template string. 

To inject data, we enclose the expression with a `curly bracket({})` preceded by a `$ sign`.

```js
let name = 'Rajnandini'
let place = 'Varanasi'
let dob = '10-08-1996'

`Hi 👋️ Myself ${name} and I live in ${place}`
```

### 1.20 Data Type Casting

Converting one data type to another data type. We use `parseInt(), parseFloat(), Number(), + sign, str()`.

```js
// String to Int
let num = '10'
let numInt = parseInt(num)
numInt                                    // 10

// String to float
let num = '9.81'
let numFloat = parseFloat(num)
numFloat                                  // 9.81
```
 
 ## Javascript Day1 Practice Quiz 👨‍💻️

>>**The following languages are in the Indo-European family:**
       [x] Urdu
       [ ] Finnish
       [x] Marathi
       [x] French
       [ ] Hungarian
