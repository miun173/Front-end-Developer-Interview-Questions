---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

* Explain event delegation
  - When an event is fired from an element, the event will be bubbled up to its parent nodes

* Explain how `this` works in JavaScript
  - `this` normally refers to the object which `owns` the method or property, but it depends on how a function is called.

* Explain how prototypal inheritance works
  - Inherit another objects prototype for example:
  ```javascript
  var animal = { eats: true }
  var rabbit = { jumps: true }

  rabbit.__proto__ = animal // inherit
  ```
  if there is a property found it will skip it

* What do you think of AMD vs CommonJS?
  - AMD uses define which can get a little hard to read. Have to return object. Require js uses the mad pattern. I like common js which uses require() syntax to load in new files. Uses exports to return object: exports.name = 'bar'; or module.exports = {}. I am personally like to use ES6 modules by use of imports and export default {} to return or return multiple objects :
  ```javascript
  export const sqrt = Math.sqrt;
  export function square(x) {
    return x * x;
  }
  
  export * from './source.js'
  ```

* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
  ```javascript
  (function foo() { })(); // or
  (function foo() { }());
  ```

* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
  undeclared.
  
  - A variable is undeclared when it does not use the var keyword. It gets created on the global object (that is, the window), thus it operates in a different space as the declared variables.
  ```javascript
  var declaredVariable = 1;

  function scoppedVariables() {
  undeclaredVariable = 1;
  var declaredVariable = 2;
  }

  scoppedVariables();

  undeclaredVariable; // 1
  declaredVariable; // 1
  ```
  
  - Something is undefined when it hasn't been defined yet. If you call a variable or function without having actually created it yet the parser will give you an not defined error.
  ```javascript
  var undefinedVariable; // undefined
  typeof undefinedVariable; // "undefined"

  undefinedFunction(); // undefined
  typeof undefinedFunction; // "undefined"
  ```
  
  - null is a variable that is defined to have a null value.
  ```javascript
  var nullVariable = null; // null
  typeof nullVariable // "object"
  ```
  
* What is a closure, and how/why would you use one?
  - Closures are expressions, usually functions, which can work with variables set within a certain context. Or, to try and make it easier, inner functions referring to local variables of its outer function create closures.

* Can you describe the main difference between a `forEach` loop and a `.map()` loop and why you would pick one versus the other?
  - forEach just loop on array
  - map itterate the array and can change the current element and return a new array
  - I'll peak `map` if I need to modify the current array. for forEach it's rare case

* What's a typical use case for anonymous functions?
  - In a callback

* How do you organize your code? (module pattern, classical inheritance?)
   - I just grouping a module based on it's features and export it as a single module through `index` file  
  
* What's the difference between host objects and native objects?
  - Host objects: what an environment(browser, Node.js, etc) provides  
  - Native objects: what JavaScript provides

* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
  - `function Person() {}`
    - Function Declaration
    - Code above declares a function statement (statements perform an action) but does not execute, however, it does get registered into the global namespace.
  - `var person = Person()`
    - Function Expression
    - A variable ‘var person’ has been defined and contains a value reference to a Person function. Any JavaScript Expressions (including Function Expressions) always returns a value. This may also be an Anonymous function if no name has been assign to a function but wrapped in parenthesis to be interpreted as an expression.

  - `var person = new Person()`
    - Function Constructor
    - By adding the keyword ‘new’. We are instantiating a new object of the Person class constructor. A function declaration is just a regular function unless it has been instantiated, it then becomes a class constructor.  

* What's the difference between `.call` and `.apply`?
  - The difference is that apply lets you invoke the function with arguments as an array; call requires the parameters be listed explicitly. A useful mnemonic is "A for array and C for comma."

* Explain `Function.prototype.bind`.
  - The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
* Describe event capturing.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between window load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
* What are the differences between variables created using `let`, `var` or `const`?
* What are the differences between ES6 class and ES5 function constructors?
* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
* What advantage is there for using the arrow syntax for a method in a constructor?
* What is the definition of a higher-order function?
* Can you give an example for destructuring an object or an array?
* ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?
* Can you give an example of a curry function and why this syntax offers an advantage?
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
* How can you share code between files?
* Why you might want to create static class members?
