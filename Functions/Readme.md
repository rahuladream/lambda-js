<div align="center">
  <h1> Javascript Functions 😹️ </h1>
 </div>

### 1. Defination

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

See an example

```js
function sampleFunc(a, b) {
    return a + b
}
```

### 1.2 Function Syntax

A javascript is defined with the `function` keyword, followed by a **name**, followed by parentheses `()`.

Function names can contain letters, digits, underscores, and dollar signs.

The code to be executed, by the function, is placed inside `curly brackets: {}`

**NOTE**
A Function is much the same as a Procedure or a Subroutine, in other programming languages.

### 1.3 Function Invocation

The code inside the function will execute when "something" invokes (calls) the function:

- When an event occurs
- When it is invoked from code
- Automatically (self-invoked)


### 1.4 Function Return

When JavaScript reaches a `return` statement, the function will stop executing.

Functions often compute a return value. The return value is **"returned"** back to the **"caller"**:

```js
var multiply = multiplyFunc(4, 5);  // Function is called

function multiplyFunc(a, b){
    return a * b;                  // return products of a,b
}

// Output
20
```

### 1.5 Why use Functions

You can reuse code: Define the code once, and use it many times.

You can use the same code many times with different arguments, to produce different results.

```js
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}

// Output
25
```

### 1.6 Function Used as Variable

Functions can be used the same way as you use variables, in all types of formulas, assignments, and calculations.


```js
// Instead of using this
var degree = toCelsius(77);

// You can use function directly as variable
var roomTemp = "The temperate is " + toCelsius(77) + "Celsius"
```

### 1.7 Function declaration

A function can be declared or created in couple of ways:

- Declaration function
- Expression Function
- Anonymouse Function
- Arrow Function

### 1.8 Function without a parameter and return

Function can be declared without parameter and even without return.

```js
function Cube() {
    let num = 3
    let cube = num * num * num;
    console.log(cube)
}

// Invoking function
Cube()                  // 9
```

### 1.9 Function with parameter

In a function we can pass different data types(number, string, boolean, object, function) as a parameter.

```js
function AnySense(param1) {
    return param1
}

function areaOfCircle(radius) {
    let area = Math.PI * r * r
    return area
}
```

### 1.10 Function with unlimited number of parameters

Sometimes we do not know how many arguments the user going to pass. Therefore, we should know how to write a function which can take unlimited number of arguments.

We will be using `arrow function` to handle the unlimited number of scope.

```js
const sumAllNums = (...args) => {
    let sum = 0;
    for (const element in args) {
        sum += element
    }
    return sum
}

sumAllNums(1,2,3,4)
//Output
10
```
The above function is also know as `arrow function`.

### 1.11 Anonymouse Function

Anonymous function or without name

```js
const noName = function() {
    return whatever
}
```

### 1.12 Expression Function

Expression functions are anonymous functions. After we create a function without a name and we assign it to a variable.

```js
// Function expression
const square = function(n) {
  return n * n
}
square(2)
```

### 1.13 Self Invoking Function

Self invoking functions are anonymous functions which do not need to be called to return a value.

```js
(function(n) {
    return n * n
})(2)

let cubeNum = (function(n) {
    return n * n * n;
})(10)

//Output
1000
```

### 1.14 Arrow Function

Arrow function is an alternative to write a function, however function declaration and arrow function have some minor differences.

```js
const square = n => {
  return n * n
}

square(3)
// Output
9
```

One more example

```js
onst changeToUpperCase = arr => {
  const newArr = []
  for (const element of arr) {
    newArr.push(element.toUpperCase())
  }
  return newArr
}

const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
changeToUpperCase(countries)
// ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]

```


🍻🎉💊 Congrats for completing **Day 2** 🍻🎉💊

if you are preparing for interview have a look at [interview questions of Functions](./InterviewQuestion.md) 
