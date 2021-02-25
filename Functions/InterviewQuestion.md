<div align="center">
  <h1> Javascript Interview 👨‍💻️ Questions Functions </h1>
 </div>

### 1. What is the value of x & y?
```js
const fn = (a, ...numbers, x, y) => {
    console.log(x, y)
};
```

### 2. Guess the output of the following code:
```js
var hero = {
    _name: 'John Doe',
    getSecretIdentity: function (){
        return this._name;
    }
};
var stoleSecretIdentity = hero.getSecretIdentity;
console.log(stoleSecretIdentity());
console.log(hero.getSecretIdentity());
```

### 3. What is the output of the following code snippet?
```js
function greet() {
    console.log(this.name);
}
const sayHello1 = greet.bind({name: "Tom Cruise"});
sayHello1();
const sayHello2 = sayHello1.bind({name: "Zac Efron"});
sayHello2();
```

### 4. What will be logged to the console after running the snippet below?

```js
function greet() {
  setTimeout(function() {
    console.log(this.name);
  }, 500);
}
greet.call({name: 'Daniel Craig'});
```

### 5. What will be logged to the console?
```js
function Employee(name) {
    this.name = name;
}
Employee.prototype.getName = () => {
    return this.name;
};
const jason = new Employee('Jason');
console.log(jason.getName());
```

### 6. What is wrong with the code written below?

```js
var something = null;
var randomFunction = function () {
  var somethingElse = something;
  var unused = function () {
    if (somethingElse)
      console.log("hi");
  };
  something = {
    longStr: new Array(1000000).join('*'),
    someMethod: function () {
      console.log(someMessage);
    }
  };
};
setInterval(randomFunction, 1000);
```