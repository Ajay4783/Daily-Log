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


### 2. Object Destructuring
A convenient way to extract values from objects and assign them to variables.

```javascript
const user = { name: "Ajay", age: 20, role: "Developer" };

// Old way
// const name = user.name;
// const role = user.role;

// ES6 Destructuring
const { name, role } = user;

console.log(${name} is a ${role}); // Output: Ajay is a Developer