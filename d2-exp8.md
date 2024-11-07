# Essential JavaScript Basics

## 1. Variables and Data Types

- **Variables**: Used to store data.
  - `let`: Block-scoped variable (use this most often).
  - `const`: Block-scoped, but constant (the value can’t change).
  - `var`: Globally scoped (avoid this in modern JavaScript).
  - **Example**:
    ```javascript
    let name = "John";
    const age = 30;
    ```

- **Data Types**:
  - **String**: `"hello"`
  - **Number**: `25`
  - **Boolean**: `true` or `false`
  - **Array**: `[1, 2, 3]`
  - **Object**: `{ key: "value" }`

## 2. Operators

- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Comparison Operators**: `===` (equal), `!==` (not equal), `<`, `>`, `<=`, `>=`
- **Logical Operators**: `&&` (and), `||` (or), `!` (not)
- **Example**:
    ```javascript
    const isAdult = age >= 18;
    ```

## 3. Functions

- Functions allow you to write reusable blocks of code.
  - **Function Declaration**:
    ```javascript
    function greet() {
      console.log("Hello!");
    }
    greet();
    ```

  - **Arrow Function**:
    ```javascript
    const greet = () => {
      console.log("Hello!");
    };
    ```

## 4. Conditionals

- Use `if`, `else if`, and `else` to perform conditional checks.
  - **Example**:
    ```javascript
    const age = 20;
    if (age >= 18) {
      console.log("You are an adult.");
    } else {
      console.log("You are a minor.");
    }
    ```

## 5. Loops

- **For Loop**: Use when you know the number of iterations.
    ```javascript
    for (let i = 0; i < 5; i++) {
      console.log(i);
    }
    ```

- **While Loop**: Use when the number of iterations is not known.
    ```javascript
    let i = 0;
    while (i < 5) {
      console.log(i);
      i++;
    }
    ```

## 6. Arrays

- An array is a list of items stored in a single variable.
- **Common Array Methods**:
  - `push()`: Add item to the end.
  - `pop()`: Remove item from the end.
  - `map()`: Apply a function to each element.
  - **Example**:
    ```javascript
    const fruits = ["apple", "banana", "cherry"];
    fruits.push("orange"); // ["apple", "banana", "cherry", "orange"]
    ```

## 7. Objects

- Objects are collections of key-value pairs.
- Access values with dot notation or bracket notation.
- **Example**:
    ```javascript
    const person = {
      name: "John",
      age: 30,
      greet: function() {
        console.log("Hello, " + this.name);
      }
    };
    person.greet(); // "Hello, John"
    ```

## 8. ES6 Features (Essential for React)

- **Template Literals**: Embed expressions in strings with backticks (\`) and `${}`.
    ```javascript
    const name = "John";
    console.log(`Hello, ${name}!`);
    ```

- **Destructuring**: Extract values from arrays or objects.
    ```javascript
    const person = { name: "John", age: 30 };
    const { name, age } = person;
    ```

- **Spread and Rest Operators**:
  - **Spread**: Expands elements in an array/object.
      ```javascript
      const arr1 = [1, 2];
      const arr2 = [...arr1, 3, 4]; // [1, 2, 3, 4]
      ```

  - **Rest**: Collects remaining elements.
      ```javascript
      function sum(...numbers) {
        return numbers.reduce((acc, num) => acc + num, 0);
      }
      sum(1, 2, 3); // 6
      ```

## 9. DOM Basics (for React’s virtual DOM)

- The Document Object Model (DOM) represents the structure of an HTML document as a tree of elements.
- Manipulate elements with JavaScript by selecting them:
    ```javascript
    const heading = document.querySelector("h1");
    heading.textContent = "New Title";
    ```

## 10. Basic Event Handling

- You’ll need to understand events like `click` and `submit` for React.
- **Example**:
    ```javascript
    const button = document.querySelector("button");
    button.addEventListener("click", () => {
      console.log("Button clicked!");
    });
    ```

Mastering these fundamentals will give you a solid base to dive into React! Let me know when you’re ready for the next step.
