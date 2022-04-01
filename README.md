[DEMO LINK](https://cxrmx.github.io/test-task/)

1. Data types in JS?
JS has these data types: string, number, boolean, undefined, null, symbol, object, bigInt.
2. How to check that data type is an object?
typeof(yourData) === 'object' && yourData !== null
3. How to check that data type is an array?
Array.isArray(data)
4. All ways to create an array?
const arr = ['', '', ''];
const arr = new Array('', '', '', '');
const arr = Array.of('', '', '');
const arr = [...anotherArr, somethingElse];
const copyArr = Array.from(anotherArr);
5. What is recursion?
When function called itself.
6. How to check an object that it is empty?
Object.keys(obj).length === 0
7. What is the difference between arrow functions and normal functions?
Syntax, Arrow functions do not have an arguments binding, Cant use this in arrow function, Cant use 'new' keyword in arrow function.
8. What is the keyword "this" in methods?
“This” keyword refers to an object that is executing the current piece of code.
9. What is “use strict”?
Strict mode. It helps you to write cleaner code, like preventing you from using undeclared variables.
10. Spread and rest operators. What difference?
The rest operator puts the rest of some specific user-supplied values into a JavaScript array, but the spread syntax expands iterables into individual elements
