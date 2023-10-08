![image](https://github.com/NishitaErvantikar9/Web-Development-Bootcamp/assets/120945994/a4f4e932-cbb0-4aee-a4cf-428678479557)

## What is Javascript?

JavaScript is a high-level, dynamic, and versatile programming language primarily used for web development. It is one of the core technologies for building interactive and dynamic content on the internet, alongside HTML (Hypertext Markup Language) and CSS (Cascading Style Sheets). JavaScript enables developers to create interactive web applications, perform client-side scripting, and manipulate web page elements in response to user actions.

## What are the features of Javascript?
| Feature                                | Feature                                | Feature                                |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| High-Level Language                    | Interpreted Language                   | Dynamic Typing                         |
| Object-Oriented                        | Functional Programming                 | Prototype-Based Inheritance           |
| Event-Driven                           | Asynchronous Programming               | Cross-Platform                         |
| Client-Side Scripting                  | Server-Side Scripting                  | Standardized (ECMAScript)              |
| Rich Standard Library                  | DOM Manipulation                       | JSON Support                           |
| Web APIs                               | Active Developer Community             | Cross-Browser Compatibility            |
| Error Handling                         | Prominent Frameworks                   | Package Management                     |
| Security                               | Testing and Debugging                  | Garbage Collection                     |
| Extensible                             | Lexical Scope                          | Closures                               |
| WebAssembly Support                    | Real-Time Communication                | Modular Programming                    |
| Functional Reactive Programming (FRP)   | Meta-Programming                       | Community-Driven Evolution             |


## What is a Javascript Engine?
![image](https://github.com/NishitaErvantikar9/Web-Development-Bootcamp/assets/120945994/de35d315-85dd-455b-8987-3599902a1c9b)
A JavaScript engine is a software component or virtual machine that interprets and executes JavaScript code. It is responsible for running JavaScript programs, converting the human-readable JavaScript source code into machine-executable instructions, and managing various aspects of code execution, such as memory allocation, optimization, and error handling.

Notable JavaScript engines include:

- **V8:** Developed by Google, V8 is used in the Chrome web browser and Node.js.
- **SpiderMonkey:** Developed by Mozilla, SpiderMonkey is used in the Firefox web browser.
- **JavaScriptCore (Nitro):** Developed by Apple, JavaScriptCore is used in the Safari web browser.
- **Chakra:** Developed by Microsoft, Chakra was used in the Edge web browser (replaced by V8 in the new Chromium-based Edge).

Each JavaScript engine may have its own unique features, optimizations, and performance characteristics, but they all serve the fundamental purpose of executing JavaScript code in different environments.


https://medium.com/developers-arena/understanding-the-javascript-v8-engine-6f59bae39f06
## JS Data types
Certainly! Here are examples of each data type in JavaScript:

**Primitive Data Types:**

1. **Number:** Represents both integer and floating-point numbers.
   ```
   let integerNumber = 42;
   let floatingPointNumber = 3.14;
   ```

2. **String:** Represents a sequence of characters enclosed in single or double quotes.
   ```javascript
   let greeting = 'Hello';
   let message = "World";
   ```

3. **Boolean:** Represents a true or false value.
   ```javascript
   let isTrue = true;
   let isFalse = false;
   ```

4. **Undefined:** Represents a variable that has been declared but has not been assigned a value.
   ```javascript
   let x;
   console.log(x); // undefined
   ```

5. **Null:** Represents an intentional absence of any object value or no value at all.
   ```javascript
   let y = null;
   ```

6. **Symbol (ES6):** Represents a unique and immutable value, often used as object property keys.
   ```javascript
   const uniqueKey = Symbol('description');
   ```

7. **BigInt (ES11):** Represents large integers that can't be represented by the Number data type.
   ```javascript
   const bigIntValue = 1234567890123456789012345678901234567890n;
   ```

**Reference Data Types:**

8. **Object:** Represents a collection of key-value pairs.
   ```javascript
   const person = { name: 'John', age: 30 };
   ```

9. **Array:** A specialized object for storing and manipulating ordered lists of data.
   ```javascript
   const numbers = [1, 2, 3];
   ```

10. **Function:** A callable object that can contain a block of code and be invoked with arguments.
    ```javascript
    function add(a, b) {
      return a + b;
    }
    ```

11. **Date:** Represents dates and times.
    ```javascript
    const currentDate = new Date();
    ```

12. **Regular Expression (RegExp):** Represents patterns used for string matching and manipulation.
    ```javascript
    const regexPattern = /pattern/;
    ```

13. **Map (ES6):** Represents a collection of key-value pairs.
    ```javascript
    const myMap = new Map();
    myMap.set('key1', 'value1');
    ```

14. **Set (ES6):** Represents a collection of unique values.
    ```javascript
    const mySet = new Set();
    mySet.add(1);
    mySet.add(2);
    ```

15. **Array Buffer (ES6 Typed Arrays):** Represents a fixed-length binary data buffer.
    ```javascript
    const buffer = new ArrayBuffer(8);
    ```

16. **Typed Arrays (ES6):** Provide a way to work with binary data directly and efficiently.
    ```javascript
    const intArray = new Int32Array(buffer);
    ```

17. **Promise (ES6):** Represents a promise of a future value, often used for asynchronous operations.
    ```javascript
    const myPromise = new Promise(resolve => resolve('Done!'));
    ```

18. **Symbol (ES6):** Can also be used as a reference data type when used as an object property key.
    ```javascript
    const uniqueSymbol = Symbol('description');
    ```

19. **Function:** JavaScript functions are first-class objects and can be assigned to variables, passed as arguments, and returned from other functions.
    ```javascript
    const multiply = function(a, b) {
      return a * b;
    };
    ```

20. **Custom Objects:** You can create custom reference data types by defining your own classes and constructors.
    ```javascript
    class Person {
      constructor(name, age) {
        this.name = name;
        this.age = age;
      }
    }
    const personObject = new Person('Alice', 25);
    ```

These examples demonstrate the various data types in JavaScript and how they can be used in your code.

## JS variables

### Declarations

Certainly! Let's explore the differences between `var`, `let`, and `const` in JavaScript:

**1. Scope:**

- `var`: Variables declared with `var` have function scope, which means they are limited to the function in which they are defined. If declared outside any function, they have global scope.

- `let` and `const`: Variables declared with `let` and `const` have block scope, which means they are limited to the block (surrounded by curly braces) in which they are defined. This includes loops, conditionals, and functions. Block-scoped variables are not accessible outside of their block.

**Example:**

```javascript
function exampleScope() {
  if (true) {
    var x = 10; // 'x' is function-scoped
    let y = 20; // 'y' is block-scoped
    const z = 30; // 'z' is also block-scoped
  }

  console.log(x); // 10 (accessible)
  console.log(y); // ReferenceError: y is not defined (not accessible)
  console.log(z); // ReferenceError: z is not defined (not accessible)
}
```

**2. Hoisting:**

- `var`: Variable declarations using `var` are hoisted to the top of their containing function or global scope during compilation. However, their assignments are not hoisted. This means you can access a `var` variable before it's declared, but it will be initialized with `undefined`.

- `let` and `const`: Variables declared with `let` and `const` are also hoisted to the top of their containing block, but unlike `var`, they are not initialized. Attempting to access them before declaration results in a `ReferenceError`.

**Example:**

```javascript
console.log(x); // undefined (hoisted)
var x = 10;

console.log(y); // ReferenceError: y is not defined (not hoisted)
let y = 20;
```

**3. Reassignment:**

- `var`: Variables declared with `var` can be redeclared and reassigned within the same scope without error.

- `let`: Variables declared with `let` can be reassigned within the same scope, but redeclaration within the same scope is not allowed.

- `const`: Variables declared with `const` cannot be reassigned or redeclared after initialization. They are constants.

**Example:**

```javascript
var a = 10;
var a = 20; // No error (redeclaration)
a = 30; // No error (reassignment)

let b = 10;
let b = 20; // Error: Identifier 'b' has already been declared (redeclaration)
b = 30; // No error (reassignment)

const c = 10;
const c = 20; // Error: Identifier 'c' has already been declared (redeclaration)
c = 30; // Error: Assignment to constant variable (reassignment)
```

**4. Temporal Dead Zone (TDZ):**

- `let` and `const` variables are subject to the Temporal Dead Zone (TDZ). This means that they cannot be accessed before their declaration within their block.

**Example:**

```javascript
console.log(x); // ReferenceError: Cannot access 'x' before initialization
let x = 10;
```

**5. Global Object Property:**

- Variables declared with `var` at the global scope become properties of the global object (e.g., `window` in browsers).

- Variables declared with `let` and `const` at the global scope do not become properties of the global object.

**Example:**

```javascript
var globalVar = 42;
console.log(window.globalVar); // 42 (globalVar is a property of the global object)

let globalLet = 42;
console.log(window.globalLet); // undefined (globalLet is not a property of the global object)
```

**6. Use Cases:**

- `var` is rarely used in modern JavaScript due to its scoping issues and hoisting behavior. It's generally best to avoid using `var`.

- `let` is used when you need to reassign a variable within its scope.

- `const` is used when you want to declare a variable that should not be reassigned after initialization (constants).

In summary, `let` and `const` provide block scoping and are generally preferred over `var` for modern JavaScript development. `let` allows reassignment, while `const` enforces immutability. Choose the one that best suits your variable's requirements.

## Operators and Expressions
Certainly! Let's explore operators and expressions in JavaScript.

**Operators:**

Operators are symbols or keywords that perform operations on operands (values or variables). JavaScript supports various types of operators, including:

1. **Arithmetic Operators:** Used for mathematical operations like addition, subtraction, multiplication, division, and more.

   ```javascript
   let a = 10;
   let b = 5;
   let sum = a + b; // Addition
   let difference = a - b; // Subtraction
   let product = a * b; // Multiplication
   let quotient = a / b; // Division
   let remainder = a % b; // Modulus (remainder)
   ```

2. **Comparison Operators:** Used to compare values and return a Boolean result (true or false).

   ```javascript
   let x = 10;
   let y = 5;
   let isEqual = x === y; // Equal to
   let isNotEqual = x !== y; // Not equal to
   let isGreaterThan = x > y; // Greater than
   let isLessThan = x < y; // Less than
   let isGreaterOrEqual = x >= y; // Greater than or equal to
   let isLessOrEqual = x <= y; // Less than or equal to
   ```

3. **Logical Operators:** Used to combine or manipulate Boolean values.

   ```javascript
   let isTrue = true;
   let isFalse = false;
   let andResult = isTrue && isFalse; // Logical AND
   let orResult = isTrue || isFalse; // Logical OR
   let notResult = !isTrue; // Logical NOT
   ```

4. **Assignment Operators:** Used to assign values to variables.

   ```javascript
   let num = 10;
   num += 5; // Add and assign (num is now 15)
   num -= 3; // Subtract and assign (num is now 12)
   num *= 2; // Multiply and assign (num is now 24)
   num /= 4; // Divide and assign (num is now 6)
   ```

5. **Unary Operators:** Operate on a single operand.

   ```javascript
   let count = 5;
   count++; // Increment by 1 (count is now 6)
   count--; // Decrement by 1 (count is now 5)
   ```

6. **Conditional (Ternary) Operator:** Provides a compact way to write conditional expressions.

   ```javascript
   let age = 18;
   let isAdult = age >= 18 ? 'Yes' : 'No'; // Ternary operator
   ```

**Expressions:**

Expressions are combinations of values, variables, operators, and functions that produce a result. They can be as simple as a single value or as complex as a combination of multiple operations. Here are some examples of expressions:

1. **Arithmetic Expressions:**

   ```javascript
   let result1 = 5 + 3 * 2; // Arithmetic expression
   let result2 = (5 + 3) * 2; // Parentheses can be used to change the order of operations
   ```

2. **Comparison Expressions:**

   ```javascript
   let isGreaterThanTen = 15 > 10; // Comparison expression
   ```

3. **Logical Expressions:**

   ```javascript
   let isTrue = true;
   let isFalse = false;
   let logicalExpression = isTrue && isFalse || !isTrue; // Logical expression
   ```

4. **Assignment Expressions:**

   ```javascript
   let num = 10;
   num += 5; // Assignment expression
   ```

5. **Function Call Expressions:**

   ```javascript
   function add(x, y) {
     return x + y;
   }
   let sum = add(3, 4); // Function call expression
   ```

6. **Ternary Operator Expression:**

   ```javascript
   let age = 18;
   let isAdult = age >= 18 ? 'Yes' : 'No'; // Ternary operator expression
   ```

7. **Array and Object Literal Expressions:**

   ```javascript
   let numbers = [1, 2, 3]; // Array literal expression
   let person = { name: 'John', age: 30 }; // Object literal expression
   ```

8. **Template Literal Expressions:**

   ```javascript
   let name = 'Alice';
   let greeting = `Hello, ${name}!`; // Template literal expression
   ```

Expressions play a crucial role in JavaScript as they are used to perform calculations, make decisions, and produce results. Understanding operators and how they are used within expressions is essential for writing effective JavaScript code.

## Loops
Certainly! Here are examples for each type of loop mentioned:

1. **for Loop:**
   - Iterating a specific number of times:

   ```javascript
   for (let i = 0; i < 5; i++) {
     console.log(i);
   }
   ```

2. **while Loop:**
   - Repeating while a condition is true:

   ```javascript
   let i = 0;
   while (i < 5) {
     console.log(i);
     i++;
   }
   ```

3. **do...while Loop:**
   - Executing at least once and repeating while a condition is true:

   ```javascript
   let i = 0;
   do {
     console.log(i);
     i++;
   } while (i < 5);
   ```

4. **for...in Loop:**
   - Iterating over object properties:

   ```javascript
   const person = {
     name: 'John',
     age: 30,
     city: 'New York'
   };

   for (let key in person) {
     console.log(`${key}: ${person[key]}`);
   }
   ```

5. **for...of Loop:**
   - Iterating over array elements:

   ```javascript
   const fruits = ['apple', 'banana', 'cherry'];

   for (let fruit of fruits) {
     console.log(fruit);
   }
   ```

6. **forEach Loop:**
   - Iterating over array elements with a method:

   ```javascript
   const numbers = [1, 2, 3];

   numbers.forEach(function(number) {
     console.log(number);
   });
   ```

7. **for...await...of Loop (ES8 and later):**
   - Iterating asynchronously over values (e.g., using Promises):

   ```javascript
   const asyncIterable = [asyncFunction1(), asyncFunction2(), asyncFunction3()];

   for await (let result of asyncIterable) {
     console.log(result);
   }
   ```

8. **for...of Loop with Object.values (ES8 and later):**
   - Iterating over object values:

   ```javascript
   const person = {
     name: 'John',
     age: 30,
     city: 'New York'
   };

   for (let value of Object.values(person)) {
     console.log(value);
   }
   ```

9. **for...of Loop with Object.entries (ES8 and later):**
   - Iterating over object entries (key-value pairs):

   ```javascript
   const person = {
     name: 'John',
     age: 30,
     city: 'New York'
   };

   for (let [key, value] of Object.entries(person)) {
     console.log(`${key}: ${value}`);
   }
   ```

10. **for...of Loop with Map (ES6 and later):**
    - Iterating over Map entries:

   ```javascript
   const myMap = new Map([
     ['name', 'John'],
     ['age', 30],
     ['city', 'New York']
   ]);

   for (let [key, value] of myMap) {
     console.log(`${key}: ${value}`);
   }
   ```

11. **for...of Loop with Set (ES6 and later):**
    - Iterating over Set values:

   ```javascript
   const mySet = new Set(['apple', 'banana', 'cherry']);

   for (let fruit of mySet) {
     console.log(fruit);
   }
   ```

These examples demonstrate how each type of loop can be used for various tasks and data structures in JavaScript.

## Javascript Functions
I apologize for the confusion. Let's provide comprehensive examples and detailed explanations for each type of function, covering all the concepts and characteristics:

**1. Function Declaration:**
   - A named function that is hoisted to the top of its containing scope.
   - Can be called before they are declared.

   ```javascript
   sayHello(); // Call before declaration is allowed

   function sayHello() {
     console.log('Hello!');
   }
   ```

**2. Function Expression:**
   - An anonymous function assigned to a variable.
   - Not hoisted like function declarations, so they must be defined before they are called.

   ```javascript
   greet(); // Error: Cannot access 'greet' before initialization

   const greet = function(name) {
     console.log(`Hello, ${name}!`);
   };
   greet('John');
   ```

**3. Arrow Function (ES6+):**
   - Provides a concise syntax for defining functions.
   - Does not have its own `this`, `arguments`, `super`, or `new.target`.
   - Inherits the lexical scoping of `this` from its surrounding code.

   ```javascript
   const add = (a, b) => a + b;
   console.log(add(5, 3)); // 8
   ```

**4. Named Function Expression:**
   - An anonymous function with a name for better debugging.
   - Not hoisted like function declarations.
   - Helps in stack trace debugging.

   ```javascript
   const multiply = function multiply(a, b) {
     return a * b;
   };
   console.log(multiply(4, 6)); // 24
   ```

**5. Immediately Invoked Function Expressions (IIFE):**
   - Defines and executes a function immediately after creation.
   - Used for creating private scopes and avoiding global scope pollution.

   ```javascript
   (function() {
     console.log('I am immediately invoked!');
   })();
   ```

**6. First-Class Functions:**
   - Functions are treated as first-class citizens.
   - Can be assigned to variables, passed as arguments, and returned from other functions.

   ```javascript
   const sayHello = function() {
     return 'Hello';
   };
   const greet = sayHello;
   console.log(greet()); // 'Hello'
   ```

**7. Higher-Order Functions:**
   - Functions that take other functions as arguments or return them.
   - Used for abstraction, code reusability, and functional composition.

   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   const doubled = numbers.map(function(number) {
     return number * 2;
   });
   console.log(doubled); // [2, 4, 6, 8, 10]
   ```

**8. Recursive Functions:**
   - Functions that call themselves.
   - Used for tasks with repeated subtasks, like factorials and traversing tree structures.
   - Requires a base case to avoid infinite recursion.

   ```javascript
   function factorial(n) {
     if (n === 0) {
       return 1;
     } else {
       return n * factorial(n - 1);
     }
   }
   console.log(factorial(5)); // 120
   ```

**9. Constructor Functions:**
   - Used to create custom objects when called with `new`.
   - Functions that initialize object properties.
   - Typically start with an uppercase letter to indicate their constructor nature.

   ```javascript
   function Person(name, age) {
     this.name = name;
     this.age = age;
   }
   const john = new Person('John', 30);
   console.log(john.name); // 'John'
   ```

**10. Callback Functions:**
    - Functions passed as arguments to other functions.
    - Executed after specific events or asynchronous tasks complete.
    - Used for handling asynchronous code, event handling, and more.
   
       ```javascript
       function fetchData(url, callback) {
         // Simulate fetching data
         setTimeout(function() {
           const data = 'Some data';
           callback(data);
         }, 1000);
       }
       fetchData('https://example.com', function(data) {
         console.log('Data received:', data);
       });
       ```

**11. Closure Functions:**
    - Functions that retain access to variables in their outer (lexical) scope.
    - Useful for data encapsulation and creating private variables.
    - Enable the concept of closures, where the function "closes over" its surrounding scope.

       ```javascript
       function outer() {
         const message = 'Hello, ';
         function inner(name) {
           return message + name;
         }
         return inner;
       }
       const sayHello = outer();
       console.log(sayHello('John')); // 'Hello, John'
       ```

These examples and explanations cover all the concepts and characteristics of each type of function in JavaScript. Understanding when and how to use each type is essential for effective coding in the language.

## Arrays
Arrays are a fundamental data structure in JavaScript and are used for storing and manipulating collections of data. Here's a comprehensive overview of what you need to know as a programmer about arrays in JavaScript:

**1. Array Declaration and Initialization:**
   - You can declare an array using square brackets `[]`.
   - Initialize an array by listing its elements inside the brackets, separated by commas.

   ```javascript
   const numbers = [1, 2, 3, 4, 5];
   ```

**2. Accessing Array Elements:**
   - Use square brackets and the index to access array elements.
   - Arrays are zero-indexed, so the first element is at index 0.

   ```javascript
   console.log(numbers[0]); // 1
   ```

**3. Array Properties and Methods:**
   - Arrays have built-in properties and methods like `length`, `push`, `pop`, `shift`, `unshift`, `concat`, `join`, `slice`, and more.

   ```javascript
   console.log(numbers.length); // 5
   numbers.push(6); // Add an element to the end
   numbers.pop(); // Remove the last element
   ```

**4. Iterating Through Arrays:**
   - Use loops like `for`, `for...of`, and `forEach` to iterate through arrays.

   ```javascript
   for (let i = 0; i < numbers.length; i++) {
     console.log(numbers[i]);
   }

   for (const number of numbers) {
     console.log(number);
   }

   numbers.forEach(function(number) {
     console.log(number);
   });
   ```

**5. Modifying Array Elements:**
   - You can change array elements by assigning new values to them.

   ```javascript
   numbers[2] = 30;
   console.log(numbers); // [1, 2, 30, 4, 5]
   ```

**6. Adding and Removing Elements:**
   - Use methods like `push`, `pop`, `shift`, and `unshift` to add or remove elements.

   ```javascript
   numbers.push(6); // Add an element to the end
   numbers.pop(); // Remove the last element
   numbers.shift(); // Remove the first element
   numbers.unshift(0); // Add an element to the beginning
   ```

**7. Array Splicing:**
   - The `splice` method allows you to add, remove, or replace elements at a specific index.

   ```javascript
   numbers.splice(2, 1); // Remove one element at index 2
   numbers.splice(2, 0, 10, 20); // Insert elements at index 2
   ```

**8. Slicing and Copying Arrays:**
   - Use `slice` to create a new array by extracting a portion of an existing array.
   - Use `concat` or the spread operator (`[...array]`) to concatenate arrays.

   ```javascript
   const sliced = numbers.slice(1, 4); // Extract elements at index 1 to 3
   const copy = numbers.slice(); // Copy the entire array
   ```

**9. Searching and Filtering Arrays:**
   - Use methods like `indexOf`, `lastIndexOf`, `includes`, and `find` to search for elements.
   - `filter` and `find` allow you to create new arrays based on specific criteria.

   ```javascript
   const index = numbers.indexOf(4); // Find index of value
   const filtered = numbers.filter(function(number) {
     return number > 2;
   });
   ```

**10. Sorting Arrays:**
    - Use the `sort` method to sort elements in an array in place.
    - Pass a comparison function to `sort` for custom sorting.

    ```javascript
    numbers.sort(); // Sort in ascending order
    numbers.sort(function(a, b) {
      return b - a; // Sort in descending order
    });
    ```

**11. Multidimensional Arrays:**
    - Arrays can contain other arrays, allowing you to create multidimensional arrays or matrices.

    ```javascript
    const matrix = [[1, 2], [3, 4]];
    console.log(matrix[0][1]); // Access element at row 0, column 1
    ```

**12. Array Methods:**
    - JavaScript provides a wide range of array methods for various operations, such as `map`, `reduce`, `every`, `some`, and more.
    - These methods simplify common array operations and are powerful tools for working with data.

    ```javascript
    const doubled = numbers.map(function(number) {
      return number * 2;
    });

    const sum = numbers.reduce(function(total, number) {
      return total + number;
    }, 0);
    ```

**13. Array Destructuring:**
    - You can use array destructuring to extract values from arrays into separate variables.

    ```javascript
    const [first, second, ...rest] = numbers;
    console.log(first, second, rest);
    ```

**14. Array Spread and Rest Operators:**
    - The spread operator (`...`) can be used to spread array elements into other arrays or function arguments.
    - The rest operator (`...`) can collect remaining function arguments into an array.

    ```javascript
    const newArray = [...numbers, 6, 7];
    const sum = (...numbers) => numbers.reduce((total, number) => total + number, 0);
    ```

**15. Array Gotchas:**
    - Be aware of quirks like reference types, where two arrays can reference the same underlying data.

    ```javascript
    const a = [1, 2, 3];
    const b = a; // Both a and b reference the same array
    b.push(4);
    console.log(a); // [1, 2]
    ```
