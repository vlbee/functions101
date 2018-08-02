# JavaScript Functions 101
Mini interactive Founders &amp; Coders group workshop to review JS functions and function jargon.

Copy the code below into [Repl.it](https://repl.it/) to run code and see what each function type example returns. Uncomment/comment as needed!

```
// DECLARED NAMED FUNCTION

// Create a new function in your JavaScript by "declaring" it with a name - the below is an example of a "named function declaration".
function sayHelloWorld() {
  console.log("a declared named function saying Hello World")
}

// Declared functions are not executed immediately. That is, they don't actually run or do anything when you declare them. 

// Instead, a declared function is saved in memory for use elsewhere in your code. They exist in the "scope" of your programme. They will only be executed at another point in the code, when they are "called" (a.k.a. "invoked").
sayHelloWorld();



// ANONYMOUS FUNCTION EXPRESSION

// If you do not give your function declaration a "name", it will instead be an "anonymous function expression":

// function () {
//   console.log("hello world!")
// };
  
// The code above will throw an error at runtime. 

// This is because function expressions cannot exist on their own in the global programme scope. They need to be part of an an "execution statement" or assigned to a variable. 

// For example, you can assign a function expression to a variable:
var sayHelloWorldAgain = function () {
  console.log("hello world again!")
};

// and invoke it by calling upon the variable later:
sayHelloWorldAgain();



// IMMEDIATELY INVOKED FUNCTION EXPRESSION aka IIFE

// Another thing you can do with a function expression is invoke it immediately by first wrapping up the whole function expression inside (parenthesis). 

// This is called an IIFE ('IFFY') Function - "Immediately-Invoked Function Expression"

(function () {
  console.log("I'm an IIFE function saying hello world!")
})();

// Wrapping your function expression in (parentheses) matters!!! 
// The first pair of parentheses around the function expression (function(){...}) encapsulates the code within (in this case, a function) into an executable expression so it can be evaluated at run time. 
// The second pair of parentheses at the end (function(){...})() INVOKES the function that results from that evaluated expression.

// Think about parentheses in math - they give precedence to certain math expressions so you know how to evaluate that expression. 
// 1+2*3 = 7 or 9?
// (1+2)*3 = 9
// 1+(2*3) = 7

// Similarly, when writing IF/ELSE boolean expressions, you need to wrap those expressions in parentheses for JavaScript to know how to evaluate the expression.



// CALLING FUNCTIONS WITHIN OTHER FUNCTIONS

// You can call any named function or functions assigned to variables  inside the {scope} of another functions.

(function () {
  console.log("I'm an IIFE function calling sayHelloWorld");
  sayHelloWorld(); // a function called within the block scope of an IFFE function
})();



// ARGUMENTS & PARAMETERS

// When you run a function, you can pass in data for the function to act upon that data.

// When you declare a new function, the variables representing that future data are called "PARAMETERS"
// When you invoke that function, the variables representing the actual data you are passing in at runtime are called "ARGUMENTS"

// The "name" used twice below in this function declaration is a parameter
function sayHello(name) { 
  console.log("a declared named function saying Hello " + name)
}
// When you call sayHello below, 'Sarah' is an argument.
sayHello('Sarah');



// CALLBACKS

// An argument can be any data type - e.g. a string, number, array, boolean, object. An argument can also be another function - in JavaScript this is known as a CALLBACK. 

// A callback function can be either named or anonymous:

// Named function callback:
function sayHelloToSomeone(name, callback) { // It is common praction to name your parameter 'callback' or 'cb' when declaring your function.
  return callback(name)
}
sayHelloToSomeone('Laura', sayHello) // named function callback argument

// Anonymous function expression callback: 
function sayGoodbyeToSomeone(name, callback) {
  return callback(name)
}
sayGoodbyeToSomeone('George', function (name) {
   console.log("Goodbye " + name)
})

// For practice, highlight the anonymous function expression callback in the function invocation of sayGoodbyeToSomeone above.  
```
