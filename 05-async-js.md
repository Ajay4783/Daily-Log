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


### 2. Promises
A Promise represents the eventual completion (or failure) of an asynchronous operation. It has 3 states: Pending, Fulfilled, or Rejected.

```javascript
const myPromise = new Promise((resolve, reject) => {
  let success = true;
  if (success) {
    resolve("Operation was successful!");
  } else {
    reject("Operation failed.");
  }
});

myPromise
  .then(result => console.log(result))
  .catch(error => console.log(error));


### 3. async / await (ES8)
This is syntactic sugar on top of Promises. It makes asynchronous code look and behave a little more like synchronous code, which is easier to read.

```javascript
const fetchData = async () => {
  console.log("Fetching data...");
  const result = await myPromise; // Waits for the promise to resolve
  console.log(result);
};

fetchData();


### 4. Fetch API
The `fetch()` method is used to request data from a server. It returns a Promise.

```javascript
const getUser = async () => {
  const response = await fetch('[https://jsonplaceholder.typicode.com/users/1](https://jsonplaceholder.typicode.com/users/1)');
  const data = await response.json();
  console.log("User Name:", data.name);
};

getUser();



### 5. Error Handling (try...catch)
When using `async/await`, it's best practice to wrap your code in a `try...catch` block to handle any network errors or rejected promises.

```javascript
const getBadData = async () => {
  try {
    const response = await fetch('[https://invalid-url.com](https://invalid-url.com)');
    const data = await response.json();
  } catch (error) {
    console.error("Oops! Something went wrong:", error.message);
  }
};

getBadData();