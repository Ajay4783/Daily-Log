# JavaScript Data Types

Today I learned about the basic data types in JavaScript. JavaScript is a dynamically typed language, which means the same variable can be used to hold different data types.

### 1. Primitive Data Types
* **String:** Text data wrapped in quotes (single, double, or backticks).
* **Number:** Can be integers or decimals.
* **Boolean:** Represents a logical entity and can have two values: `true` or `false`.

### 2. Complex Data Types
* **Array:** A list of items (technically a special type of object in JS).
* **Object:** A collection of key-value pairs.

---

### Code Example (All in one script):

```javascript
// =========================
// 1. String
// =========================
const firstName = "Ajay";
console.log("String:", firstName);

// =========================
// 2. Number
// =========================
const age = 20;
const price = 99.99;
console.log("Number:", age, "and", price);

// =========================
// 3. Boolean
// =========================
const isDeveloper = true;
const isTired = false;
console.log("Boolean:", isDeveloper);

// =========================
// 4. Array (List of items)
// =========================
const skills = ["React", "Python", "Django"];
console.log("Array:", skills);
console.log("First Skill:", skills[0]); // Output: React

// =========================
// 5. Object (Key-Value pairs)
// =========================
const userProfile = {
  name: "Ajay",
  role: "Full Stack Developer",
  location: "Tiruppur"
};
console.log("Object:", userProfile);
console.log("Role:", userProfile.role); // Output: Full Stack Developer

// =========================
// Bonus: typeof Operator
// =========================
// You can use 'typeof' to check a variable's data type
console.log(typeof firstName); // Output: string
console.log(typeof age);       // Output: number
console.log(typeof isDeveloper); // Output: boolean