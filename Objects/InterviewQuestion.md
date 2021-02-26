<div align="center">
  <h1> Javascript Interview 👨‍💻️ Questions Objects </h1>
 </div>


#### 1. What is output of following code?

```js
var dwayne = {}, daniel = { firstName: 'Daniel'}, jason = {key: 'jason'};

dwayne[daniel]=123;
dwayne[jason]=456;

console.log(dwayne[daniel]);
```

#### 2. What will be the output of the following code?

```js
const func = (function(a){
  delete a;
  return a;
})(5);

console.log(func);
```

#### 3. What is the output of the following code snippet?

```js
console.log({a:1} == {a:1});
console.log({a:1} === {a:1});
```

#### 4. Which approach is better and why?

```js
const jamesBond = {
    firstName: "Daniel",
    lastName: "Craig",
    getFullName: function () {
        return `${this.firstName} ${this.lastName}`.trim();
    }
};
jamesBond.getFullName();
```

or

```js
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
}
Person.prototype.getFullName = function () {
    return `${this.firstName} ${this.lastName}`.trim();
};
const jamesBond = new Person("Daniel", "Craig");
jamesBond.getFullName();
```

#### 5. What is the difference between Object and Map?

#### 6. What Are Object Properties?

#### 7. What Is User-defined Objects?

#### 8. What Is The 'with' Keyword?

#### 9. What Are The Javascript Native Objects?

#### 10. What Is Javascript Arrays Object?

#### 11. What Is Javascript Math Object?

#### 12. What Are Regular Expressions And Regexp Object?