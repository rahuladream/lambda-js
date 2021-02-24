# Javascript Interview 👨‍💻️ Questions Data Types 

1. What are the **falsy values** in Javascript?

```js
Following are the falsy values
- ''
- 0
- null
- undefined
- false
- NaN
```

2. How to check if value is falsy?

```js
Use the !! operator or Boolean function to check if they’re falsy.
If a value is falsy, then both will return false.

!!0                     // false
```

3. What are Wrapper Objects?

```js
Wrapper objects are objects that are created from constructors that return primitive values but have the type 'object' if it’s a number or a string. Symbols and BigInt have their own types.

Primitive values are temporarily converted to wrapper objects to call methods.

'foo'.toUpperCase()

Then we get `FOO`. It works by converting the 'foo' literal to an object and then call the toUpperCase() method on it.
```

4. What is the difference between Implicit and Explicit Coercian

```js

Implicit coercion means that the JavaScript interpreter converts a piece of data from one type to another without explicitly calling a method.

1 + '2'                 // 12

Explicit conversion is done by calling a method or using an operator to convert a type.

+'1' + +'2'             // 3
gets us 3 since we have '1' and '2' are both converted to numbers by the unary + operator.
```

5. What Does 0 || 1 Return?

```js
Since 0 is falsy, it’ll trigger the second operand to run, which gives us 1. Therefore, it should return 1.
```

6. What Does 0 && 1 Return?

```js
Since 0 is falsy, it’ll stop running since we have short-circuited evaluation. Therefore, we get 0 returned.
```

7. What Does false == ‘0’ Return?

```js
false is falsy and '0' is converted to 0, which is falsy, so they are the same in terms of the ==’s comparison criteria. Therefore, we should get true returned.
```

8. What Does 4 < 5 < 6 Return?

```js
In JavaScript, comparisons are done from left to right. So first 4 < 5 will be evaluated, which gives us true . Then true < 6 is evaluated, which is converted to 1 < 6 which is also true .

Therefore, we get true returned.

```

9. What Does typeof undefined == typeof null Return?

```js
typeof undefined returns 'undefined' and typeof null returns 'object' .

Since 'undefined' does equal 'object' , the expression should be false .
```

10. What Does typeof typeof 10 Return?

```js
JavaScript evaluates typeof typeof 10 as typeof (typeof 10) . Therefore, this returns typeof 'number' , which returns 'string' since 'number' is a string.
```