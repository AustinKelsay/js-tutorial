# JavaScript Tutorial
### Table of Contents:
- [Learn the JavaScript Syntax](#JavaScript-Syntax)
- [Build and understand our simple Bitcoin Price webpage project](#Project-explanation)

# JavaScript-Syntax

## Variable Declaration

```javascript
let x = 5; // Mutable variable
const y = 10; // Immutable variable
```
Explanation:

- let is used to declare mutable variables that can be reassigned later.
- const is used to declare immutable variables that cannot be reassigned.

## Basic Data Types

```javascript
let a = 42; // Number
let b = -100; // Number
let c = 3.14; // Number
let d = true; // Boolean
let e = 'x'; // String (single character)
let f = "Hello, World!"; // String
```
Explanation:

- JavaScript has several basic data types, including numbers, booleans, and strings.
- Numbers can be integers or floating-point values.
- Booleans represent either true or false.
- Strings are sequences of characters enclosed in single or double quotes.

## Objects

```javascript
const person = {
    name: "Alice",
    age: 30
};
```
Explanation:

- Objects in JavaScript are key-value pairs enclosed in curly braces {}.
- Each key-value pair is separated by a comma.
- Keys are strings (or symbols), and values can be of any data type.

## Accessing object properties

```javascript
console.log(person.name); // Alice
console.log(person.age); // 30
```
Explanation:

- Object properties can be accessed using dot notation (object.property).
- The value associated with the specified key is returned.

## Modifying object properties

```javascript
person.age = 31;
console.log(person.age); // 31
```
Explanation:

- Object properties can be modified by assigning a new value to them.
- The value of the property is updated accordingly.

## Arrays

```javascript
const numbers = [1, 2, 3, 4, 5];
console.log(numbers[0]); // 1
```
Explanation:

- Arrays in JavaScript are ordered collections of elements enclosed in square brackets [].
- Elements in an array are separated by commas.
- Array elements can be accessed using their index, starting from 0.

## Modifying array elements

```javascript
numbers[2] = 10;
console.log(numbers); // [1, 2, 10, 4, 5]
```
Explanation:

- Array elements can be modified by assigning a new value to them using their index.
- The value at the specified index is replaced with the new value.

## Functions

```javascript
function greet(name) {
    console.log(`Hello, ${name}!`);
}
greet("Alice"); // Hello, Alice!
```
Explanation:

- Functions in JavaScript are reusable blocks of code that perform a specific task.
- They can take parameters (inputs) and can return a value.
- Functions are defined using the function keyword, followed by the function name and a pair of parentheses.
- The function body is enclosed in curly braces {}.

## Arrow Functions

```javascript
const multiply = (a, b) => a * b;
console.log(multiply(3, 5)); // 15
```
Explanation:

- Arrow functions provide a concise syntax for writing function expressions.
- They are defined using the => syntax, with the parameters on the left side and the function body on the right side.
- If the function body consists of a single expression, the curly braces and return keyword can be omitted.

## Conditional Statements

```javascript
const age = 18;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```
Explanation:

- Conditional statements allow you to execute different code blocks based on certain conditions.
- The if statement checks a condition, and if it evaluates to true, the code block inside the if block is executed.
- If the condition is false, the code block inside the else block (if present) is executed.

## Loops

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
// Output: 0, 1, 2, 3, 4

const fruits = ["apple", "banana", "orange"];
for (let fruit of fruits) {
    console.log(fruit);
}
// Output: apple, banana, orange
```
Explanation:

- Loops allow you to repeatedly execute a block of code.
- The for loop is commonly used to iterate over a range of numbers or elements in an array.
- The for...of loop is used to iterate over the elements of an iterable object, such as an array.

## Array Methods

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = numbers.map(num => num * 2);
console.log(doubledNumbers); // [2, 4, 6, 8, 10]

const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]

const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // 15
```
Explanation:

- JavaScript provides several built-in array methods for manipulating and transforming arrays.
- The map() method creates a new array by calling a provided function on every element in the array.
- The filter() method creates a new array with all elements that pass the test implemented by the provided function.
- The reduce() method applies a function against an accumulator and each element in the array to reduce it to a single value.

## Promises

```javascript
const fetchData = () => {
    return new Promise((resolve, reject) => {
        // Simulating an asynchronous operation
        setTimeout(() => {
            const data = "Some data";
            resolve(data);
        }, 1000);
    });
};

fetchData()
    .then(data => console.log(data))
    .catch(error => console.error(error));
```
Explanation:

- Promises provide a way to handle asynchronous operations in JavaScript.
- A promise represents a value that may not be available yet but will be resolved at some point in the future.
- Promises have three states: pending, fulfilled, or rejected.
- The then() method is used to handle the fulfillment of a promise, while the catch() method is used to handle any errors.

## Async/Await

```javascript
const fetchDataAsync = async () => {
    try {
        const data = await fetchData();
        console.log(data);
    } catch (error) {
        console.error(error);
    }
};

fetchDataAsync();
```
Explanation:

- async/await is a syntax for working with promises in a more concise and readable way.
- The async keyword is used to define an asynchronous function.
- Inside an async function, you can use the await keyword to pause the execution until a promise is resolved.
- The try/catch block is used to handle any errors that may occur during the asynchronous operation.


# Project-explanation
You can find the project code in index.html

Our project is a simple webpage that fetches the bitcoin spot price from the coinbase api every three seconds and shows/updates it on the webpage

## API calls:

- An API (Application Programming Interface) is a way for different software systems to communicate with each other.
- In this example, we are making an API call to the Coinbase API to fetch the current Bitcoin price.
We use the XMLHttpRequest object in JavaScript to send a request to the API endpoint (URL) and receive the response.


## Basic JavaScript syntax:

- const is used to declare a constant variable that cannot be reassigned.
- function is used to define a function, which is a reusable block of code that performs a specific task.
- if is a conditional statement that checks if a condition is true and executes the code inside the block if it is.
- document.getElementById('price') is used to select an HTML element with the ID 'price' and manipulate its content.
- setInterval(fetchBitcoinPrice, 3000) is used to call the fetchBitcoinPrice function every 3000 milliseconds (3 seconds) to continuously update the displayed Bitcoin price.


## Step-by-step explanation of the code:

- We define a function called fetchBitcoinPrice to fetch the current Bitcoin price from the Coinbase API.
```javascript
    function fetchBitcoinPrice() {
      // ...
    }
```
- Inside the function, we create a new XMLHttpRequest object to make the API request.
```javascript
    const xhr = new XMLHttpRequest();
```
- We set the API endpoint URL to https://api.coinbase.com/v2/prices/BTC-USD/spot, which returns the current Bitcoin price in USD.
```javascript
    const apiUrl = 'https://api.coinbase.com/v2/prices/BTC-USD/spot';
```
- We open a GET request to the API endpoint using xhr.open('GET', apiUrl).
```javascript
    xhr.open('GET', apiUrl);
```
- We set the response type to JSON using xhr.responseType = 'json' to indicate that we expect the response to be in JSON format.
```javascript
    xhr.responseType = 'json';
```
- We define an onload function to handle the response from the API when the request is completed.
```javascript
    xhr.onload = function() {
      // ...
    };
```
- Inside the onload function, we check if the request was successful by comparing xhr.status to 200 (which indicates a successful request).
```javascript
    if (xhr.status === 200) {
      // ...
    }
```
- If the request is successful, we extract the current Bitcoin price from the response data using response.data.amount.
```javascript
    const response = xhr.response;
    const bitcoinPrice = response.data.amount;
```
- We display the Bitcoin price on the webpage by setting the textContent of the element with the ID 'price'.
```javascript
    document.getElementById('price').textContent = '$' + bitcoinPrice;
```
- Finally, we send the request to the API using xhr.send().
```javascript
    xhr.send();
```
- We use setInterval(fetchBitcoinPrice, 3000) to call the fetchBitcoinPrice function every 3 seconds to continuously update the displayed Bitcoin price.
```javascript
    setInterval(fetchBitcoinPrice, 3000);
```

# Code:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Bitcoin Price</title>
  <script>
    // Function to fetch the current Bitcoin price from the Coinbase API
    function fetchBitcoinPrice() {
      // Create a new XMLHttpRequest object to make an API request
      const xhr = new XMLHttpRequest();

      // Set the API endpoint URL
      const apiUrl = 'https://api.coinbase.com/v2/prices/BTC-USD/spot';

      // Open a GET request to the API endpoint
      xhr.open('GET', apiUrl);

      // Set the response type to JSON
      xhr.responseType = 'json';

      // Function to handle the response from the API
      xhr.onload = function() {
        // Check if the request was successful (status code 200)
        if (xhr.status === 200) {
          // Get the response data
          const response = xhr.response;

          // Extract the current Bitcoin price from the response
          const bitcoinPrice = response.data.amount;

          // Display the Bitcoin price on the webpage
          document.getElementById('price').textContent = '$' + bitcoinPrice;
        }
      };

      // Send the request to the API
      xhr.send();
    }

    // Call the fetchBitcoinPrice function every 3 seconds
    setInterval(fetchBitcoinPrice, 3000);
  </script>
</head>
<body>
  <h1>Current Bitcoin Price</h1>
  <p>The current price of Bitcoin is: <span id="price"></span></p>
</body>
</html>
```
