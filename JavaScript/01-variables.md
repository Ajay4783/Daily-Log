# JavaScript Variables: let, const, and var

Today I learned the basics of declaring variables in JavaScript and the key differences between `let`, `const`, and `var`.

### 1. `let` (Block Scoped, Reassignable)
Use `let` when you know the value of the variable will change or be reassigned later in your code. 

### 2. `const` (Block Scoped, Not Reassignable)
Use `const` for values that should never change. Once you assign a value to a `const` variable, you cannot reassign it. This is the recommended default way to declare variables in modern JavaScript.

### 3. `var` (Function Scoped, Old Way)
`var` is the old way of declaring variables before ES6 (2015). It can lead to unexpected bugs because of how its scoping works. It is generally recommended to avoid using `var`.

---

### Code Example (All in one script):

```javascript
// =========================
// 1. let Example
// =========================
let userName = "John";
console.log(userName); // Output: John

userName = "Alex"; // Reassigning the value
console.log(userName); // Output: Alex


// =========================
// 2. const Example
// =========================
const birthYear = 1998;
console.log(birthYear); // Output: 1998

// birthYear = 2000; // Uncommenting this will throw a TypeError


// =========================
// 3. var Example
// =========================
var greeting = "Hello World";
console.log(greeting); // Output: Hello World

greeting = "Hi there"; // Reassigning works, but avoided now
console.log(greeting); // Output: Hi there