# JavaScript Functions 101
Mini interactive Founders &amp; Coders group workshop to review JS functions and function jargon.

Copy the code below into Rept.it to run code and see what each function type example returns. Uncomment/comment as needed!

```
// Declared (Named) Function - ie. "function declaration"

function sayHelloWorld() {
  console.log("a declared named function saying Hello World")
}

// Declared functions are not executed immediately. They exist in the scope of your programme code are "saved for later use", and will be executed later, when they are INVOKED (called upon).

sayHelloWorld();



// Anonymous Function Expression 
// This will through an error when running your code, because function expressions cannot simply exist on their own. They need to be part of an an execution statement or assigned to a variable. 
// This code below will through an error at run time.   

// function () {
//   console.log("hello world!")
// };



// You can assign a function expression to a variable. 

var sayHelloWorldAgain = function () {
  console.log("hello world again!")
};

// and invoke it through the variable later:

sayHelloWorldAgain();



// Another thing you can do with a function expression is invoke it immediately by first wrapping up the whole function expression in (parenthesis). 
// This is called an IIFE - 'IFFY' Function - "Immediately-Invoked Function Expression"

(function () {
  console.log("I'm an IIFE function saying hello world!")
})();

// Wrapping your function expression in (parentheses) matters!!! 
// The first pair of parentheses (function(){...}) turns the code within (in this case, a function) into an expression, and the second pair of parentheses (function(){...})() calls the function that results from that evaluated expression.
// Think about parentheses in math: 
// 1+2*3 = 7 or 9?
// (1+2)*3 = 9
// 1+(2*3) = 7



// You can call named functions or functions assigned to variables within other functions.

(function () {
  console.log("I'm an IIFE function calling sayHelloWorld");
  sayHelloWorld();
})();



// Functions can be called with one or more ARGUMENTS (referred to as PARAMETERS in the function declaration, but essentially you can think of them as being the same thing for now)

function sayHello(name) {
  console.log("a declared named function saying Hello " + name)
}

sayHello('Sarah');



// Function Arguments can be other functions (a CALLBACK) - either named or anonymous:

// Named function callback:
function sayHelloToSomeone(name, callback) {
  return callback(name)
}
sayHelloToSomeone('Laura', sayHello)

// Callbacks can also be written as an anonymous function expression: 
function sayGoodbyeToSomeone(name, callback) {
  return callback(name)
}

 sayGoodbyeToSomeone('George', function (name) {
   console.log("Goodbye " + name)
 })
```
