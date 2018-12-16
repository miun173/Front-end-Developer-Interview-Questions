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
  - Feature detection is just a way of determining if a feature exists in certain browsers. A good example is a modern HTML5 feature ‘Location’.
  - Feature Inference is when you have determined a feature exists and assumed the next web technology feature you are implementing unto your app exists as well. Its usually bad practice to assume, so its better to explicitly specify features you want to detect and plan a fallback action.
  - UA String or User Agent String is a string text of data that each browsers send and can be access via navigator.userAgent. These “string text of data” contains information of the browser environment you are targeting.

* Explain Ajax in as much detail as possible.
   - Ajax is a way of make an network request to server without interrupt the UI thread.

* What are the advantages and disadvantages of using Ajax?
  - pros: we can make an network request to server without interrupt the UI thread
  - cons: if we want to apply the data from ajax to the DOM, we need a way make it, and it's not intuitive if we are using vanilla js 

* Explain how JSONP works (and how it's not really Ajax).
  - JSONP(as in “JSON with Padding”) is a method commonly used to bypass the cross-domain policies in web browsers (you are not allowed to make AJAX requests to a webpage perceived to be on a different server by the browser). JSON and JSONP behave differently on both the client and the server. JSONP requests are not dispatched using the XMLHTTPRequest, instead a <script> tag is created, whose source is set to the target URL. This script tag is then added to the DOM (normally the <head>).

* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
   - nope
  
* Explain "hoisting".
  - Variable declarations (and declarations in general) are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it’s declared. This behavior is called “hoisting”, as it appears that the variable declaration is moved to the top of the function or global code.

* Describe event bubbling.
  - Event bubbling is a way of event propagation in the HTML DOM API, when an event occurs in an element inside another element, and both elements have registered a handle for that event. The event propagation mode determines in which order the elements receive the event. With bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements.

* Describe event capturing.
  - Event capturing is another way of event propagation in the HTML DOM API. With capturing, the event is first captured by the outermost element and propagated to the inner elements. 

* What's the difference between an "attribute" and a "property"?
  - Attributes are defined by HTML. Properties are defined by DOM. Some HTML attributes have 1:1 mapping onto properties. id is one example of such. Some do not (e.g. the value attribute specifies the initial value of an input, but the valueproperty specifies the current value)

* Why is extending built-in JavaScript objects not a good idea?
  - because it might end up breaking other’s codes.

* Difference between window load event and document DOMContentLoaded event?
  - ` DOMContentLoaded` , load the whole document (HTML) has been loaded. `load`  event the whole document and its resources (e.g. images, iframes, scripts) have been loaded.
  
* What is the difference between `==` and `===`?
  - The identity (===) operator behaves identically to the equality. 
  - (==) operator except no type conversion is done, and the types must be the same to be considered equal. 

* Explain the same-origin policy with regards to JavaScript.
  - The same origin policy states that a web browser permits script contained in one page (or frame) to access data in another page (or frame) only if both the pages have the same origin. It is a critical security mechanism for isolating potentially malicious documents. Two pages have the same origin if the protocol, port (if one is specified), and host are the same for both pages. 

* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
  - answer
  ```javascript
  Array.prototype.duplicator = function () {
   return this.concat(this);
  }
  ```
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
  - “Ternary” means operands with three(n-ary) param. This is a one-line shorthand for an if-then statement. It is called a ternary operator or a conditional operator. 

* What is `"use strict";`? what are the advantages and disadvantages to using it?
  - Strict mode is a way to opt in to a restricted variant of JavaScript. Strict mode isn’t just a subset: it intentionally has different semantics from normal code. Browsers not supporting strict mode will run strict mode code with different behavior from browsers that do, so don’t rely on strict mode.
  
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
```javascript
let out = ''
for(let i=1; i<= 100; i++){
  if(i%3 === 0){
    out += 'fizz';
  } 
  if(i%5 === 0){
    out += 'buzz';
  } 
  if(i%3 !== 0 && i%5 !== 0) {
    out += i;
  }
  out += '\n'
}
console.log(out)
```

* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
  - The primary reason why global variables are discouraged in javascript is because, in javascript all code share a single global namespace, also javascript has implied global variables i.e. variables which are not explicitly declared in local scope are automatically added to global namespace. Relying too much on global variables can result in collisions between various scripts on the same page.

* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
  -  The load event fires at the end of the document loading process. At this point, all of the objects in the document are in the DOM, and all the images, scripts, links and sub-frames have finished loading. To execute anything post document load, we fire these events. ‘DOMContentLoaded’ or jQuery’s loaded are another options. 

* Explain what a single page app is and how to make one SEO-friendly.
  - is a web application or web site that fits on a single web page with the goal of providing a more fluid user experience similar to a desktop application. In a SPA, either all necessary code — HTML, JavaScript, and CSS — is retrieved with a single page load, or the appropriate resources are dynamically loaded and added to the page as necessary, usually in response to user actions
  - SEO-friednly: todays browser can crawl the SPAs, and we can also use SSR framework like next.js, static site generator like GatsbyJs, or prerender like prerender.io 

* What is the extent of your experience with Promises and/or their polyfills?
  - I've used quite frequently Promise for do asyn code, also `async-await` 

* What are the pros and cons of using Promises instead of callbacks?
  - It makes code more lean, and easier for catching multiple exception, because it need to call `.catch()` in the `thenable` chain.

* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
  - pros: usually the language that used to compile to js has a static type checking 
  - cons: it adds tools chain to the development 

* What tools and techniques do you use debugging JavaScript code?
  - using `debugger;` and logging

* What language constructions do you use for iterating over object properties and array items?
  - `map filter for-in reduce`

* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
  
  - Mutable objects are those whose state is allowed to change over time. An immutable value is the exact opposite — after it has been created, it can never change. Strings and Numbers are inherently immutable in javascript
  - It makes sure the object doesn't changed in the middle of the code, because it always create a copy of it
  - using const keyword, and make a copy of the object before operate on it 
  
* Explain the difference between synchronous and asynchronous functions.
  - synchronous: Step wise execution. Next line executed after first. 
  - asynchronous: Execution moves to next step before first is finished. 
  
* What is event loop?
  -  JavaScript has a concurrency model based on an “event loop”. 
  * What is the difference between call stack and task queue?
    - a job queue is a queue of things to do (usually stored persistant) and a call stack is a stack of routines.
    
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
  - First one is declaration defined at parse time while the other is expression defined at run time.

* What are the differences between variables created using `let`, `var` or `const`?
  - `const` is a signal that the identifier won’t be reassigned
  - `let`, is a signal that the variable may be reassigned, such as a counter in a loop, or a value swap in an algorithm. It also signals that the variable will be used only in the block it’s defined in, which is not always the entire containing function.
  -`var` is now the weakest signal available when you define a variable in JavaScript. The variable may or may not be reassigned, and the variable may or may not be used for an entire function, or just for the purpose of a block or loop.

* What are the differences between ES6 class and ES5 function constructors?
  - The difference is how they are declare and how the access modifiers

* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
  - it usefull for inline function return, and in a callback
  - it actually a anonymous function even if give it a name
  
* What advantage is there for using the arrow syntax for a method in a constructor?
  - the arrow will bind automatically to the class object

* What is the definition of a higher-order function?
  - It's a function that accept other functions as params or return a functions

* Can you give an example for destructuring an object or an array?
  ```javascript
  const arr = [1,2,3]
  const [x, y, z] = arr
  
  const foo = {a: 1, b: 2, c:3}
  const {a, b} = foo
  ```
  
* ES6 Template Literals offer a lot of flexibility in generating strings, can you give an example?
  ```javascript
  const name = 'miun'
  const greet = `hello my name is ${name}`
  ```
  
* Can you give an example of a curry function and why this syntax offers an advantage?
  - Currying refers to the process of transforming a function with multiple arity into the same function with less arity. The curried effect is achieved by binding some of the arguments to the first function invoke, so that those values are fixed for the next invocation.
  ```javascript
  const sum = x => y => x + y;
  
  // returns the number 3
  sum (2)(1);
  
  // returns a function y => 2 + y
  sum (2);
  ```
  
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
  - spread allows us to copy an object or array
  - rest allows us to collects multiple elements and 'condenses' them into a single element
  ```javascript
  // spread
  const num = [1, 2, 3]
  const copyNum = [...num]
  
  // rest
  function myFun(a, b, ...manyMoreArgs) {
    console.log("a", a); 
    console.log("b", b);
    console.log("manyMoreArgs", manyMoreArgs); 
  }

  myFun("one", "two", "three", "four", "five", "six");

  // a, one
  // b, two
  // manyMoreArgs, [three, four, five, six]
  ```

* How can you share code between files?
  - using module

* Why you might want to create static class members?
   - when we don't need to instanciate a class, the `static` member is usefull
