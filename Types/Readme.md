## Javascript Data Types

JavaScript variables can hold many data types: numbers, strings, objects and more:

```js
var length = 10;
var firstName = 'Rahul';

var xyz = {firstName: 'Rahul', lastName: 'Singh'}

```

### Concept of Data Types

In programming, data types is an important concept.
To be able to operate on variables, it it important to know something about the type.

### Primitive Data Types

|Data Types   |  Description                       |
|-------------|------------------------------------|
|  String     | sequence of characters "hello"     |
|  Number     | numeric values 100                 |
|  Boolean    | either false or true               |
|  Undefined  | represents undefined value         |
|  Null       |  represents null (no value at all) |


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