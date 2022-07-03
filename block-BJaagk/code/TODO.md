1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here

let percentage = function (marks, total) {
  return (marks * 100) / total;
}

let percentage => (marks, total) {
  return (marks * 100) / total;
}

```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer
Declaration
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};  
Expression
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
}; 
Expression
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
Expression
```

```js
let percentage = (marks, total) => (marks * 100) / total;
Expression
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

A function is an object & object can be valid to an expression.
eg, let sum = (a, b) => {a + b};

4. Why is a function call an expression in JavaScript?

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // Answer Valid
five = add; // Answer Valid
five = five(10, 11); // Answer Invalid
five = function () {
  return 'Hello';
}; // Answer Invalid
```

6. What is the difference between function definition and function call? Explain with an example.
In function we defines the function steps where as in function call we make them process those steps.

Ex. 
 function sum (a, b) {
  return a + b;
 } // this is the function defination.

 sum (4, 5) // this is function calling

7. What is the similarities between function definition and function call?
// The processing steps are same.


8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // valid or invalid 
// Invalid, We did not had the value of user yet and function does not work as an object data.
```

9. What is higher order function explain with an example.
// When we use callback fn the very first function in which we are calling the calBck function is higher order function.

10. Explain what is callback function. Why you can pass a function inside a function?
// when we use function itself as a parameter inside a function is called callback function.
