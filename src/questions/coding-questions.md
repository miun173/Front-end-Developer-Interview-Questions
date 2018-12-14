---
title: Coding Questions
layout: layouts/page.njk
permalink: /questions/coding-questions/index.html
---

### Question: What is the value of `foo`?
```javascript
var foo = 10 + '20';
```
Answer: `"1020"`

### Question: What will be the output of the code below?
```javascript
console.log(0.1 + 0.2 == 0.3);
```
Answer: `false`

### Question: How would you make this work?
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
Answer:
```javascript
// add element on array
const sum =(arr) => arr.reduce((acc, curr) => acc + curr)

const adder = (numArgs, prevArgs = []) => {
  // if args is empty
  return function() {
    let totalArgs = prevArgs.concat(Array.from(arguments))

    return totalArgs.length === numArgs  ? sum(totalArgs) 
      : adder(numArgs, totalArgs)
  }
}

const add = adder(2, [])

add(2, 5); // 7
add(2)(5); // 7
```

### Question: What value is returned from the following statement?
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
Answer:
`"goh angasal a m'i"`

### Question: What is the value of `window.foo`?
```javascript
( window.foo || ( window.foo = "bar" ) );
```

### Question: What is the outcome of the two alerts below?
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
Answer:
```
1st IIFE alert would be output: "Hello world"
2nd alert would be output: error bar not defined, because bar is inside IIFE scope
```

### Question: What is the value of `foo.length`?
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
Answer:
```
2
```

### Question: What is the value of `foo.x`?
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
Answer
```
foo.x // undefined
```


### Question: What does the following code print?
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
Promise.resolve().then(function() {
  console.log('three');
})
console.log('four');
```
Answer:
```
one
four
three
undefined
two
```

### Question: What is the difference between these four promises?
```javascript
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```
Answer:
```
1st Promise return a doSomething(), it can be called in the next `thenable`
2nd Promise call a function inside that `thenable`
3rd Promise
```
