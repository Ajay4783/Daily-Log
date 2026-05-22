# JavaScript ES6 Features

Today I learned about some of the most important ES6 features used heavily in modern JavaScript and React.

### 1. Arrow Functions
A shorter and cleaner way to write functions.

```javascript
// Traditional Function
function add(a, b) {
  return a + b;
}

// Arrow Function
const addArrow = (a, b) => a + b;

console.log(addArrow(5, 10)); // Output: 15