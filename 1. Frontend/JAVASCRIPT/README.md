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
   ```javascript
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
