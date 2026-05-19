# JavaScript Variables: let, const, and var

Today I learned the basics of declaring variables in JavaScript and the key differences between `let`, `const`, and `var`.

### 1. `let` (Block Scoped, Reassignable)
Use `let` when you know the value of the variable will change or be reassigned later in your code. 

```javascript
let userName = "John";
console.log(userName); // Output: John

// Reassigning the value
userName = "Alex"; 
console.log(userName); // Output: Alex

const birthYear = 1998;
console.log(birthYear); // Output: 1998

// birthYear = 2000; // This will throw a TypeError: Assignment to constant variable.

var greeting = "Hello World";
console.log(greeting);