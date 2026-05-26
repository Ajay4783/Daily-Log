# Asynchronous JavaScript

Today I learned how JavaScript handles asynchronous operations (tasks that take time to finish, like fetching data from a server).

### 1. The Basics (setTimeout)
JavaScript runs code line by line (synchronous). But we can use functions like `setTimeout` to delay execution without blocking the rest of the code.

```javascript
console.log("1. Start");

setTimeout(() => {
  console.log("2. This runs after 2 seconds");
}, 2000);

console.log("3. End"); 
// Output order will be: Start -> End -> This runs after 2 seconds