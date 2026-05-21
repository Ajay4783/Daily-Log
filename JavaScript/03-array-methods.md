# JavaScript Array Methods

Today I learned about the three most powerful array methods in JavaScript: `map`, `filter`, and `reduce`. These are heavily used in React!

### 1. map()
Creates a new array by applying a function to every element in the original array. It does not change the original array.

```javascript
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);

console.log("Original:", numbers); // [1, 2, 3, 4]
console.log("Doubled:", doubled);  // [2, 4, 6, 8]

### 2. filter()
Creates a new array filled with elements that pass a test (condition) provided by a function.

```javascript
const ages = [15, 22, 18, 10, 30];
const adults = ages.filter(age => age >= 18);

console.log("Adults only:", adults); // [22, 18, 30]

### 3. reduce()
Executes a reducer function on each element, resulting in a single output value (like summing up prices in a cart).

```javascript
const cartPrices = [10, 20, 30];
// 0 is the initial value of 'sum'
const total = cartPrices.reduce((sum, price) => sum + price, 0);

console.log("Total Cart Price:", total); // 60