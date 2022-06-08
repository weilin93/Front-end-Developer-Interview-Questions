---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

* Explain event delegation.
* Explain how `this` works in JavaScript.
  * Can you give an example of one of the ways that working with `this` has changed in ES6?
  * this is a special variable that holds value which depending on how the function is called. 
     * If it's called as object method, "this" refers to the object value.
     * In function, "this" equal to undefined if strict mode is on, else it refers to global object.
     * Arrow functions dont get its own "this", instead it refers to "this" of its surrouding scope. 
     * If .bind(), .call(), .apply() is applied, "this" refers to the argument that gets passed in to the method.
* Explain how prototypal inheritance works.
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What language constructions do you use for iterating over object properties and array items?
* Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?
* What's a typical use case for anonymous functions?
* What's the difference between host objects and native objects?
* Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
* Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain "hoisting".
  * It's a behavior that makes some types of variables are accessable before it is declared. On the surface, it looks like it is being lifted to the top of its scope. Underneath the hood, variable declaration is not actually moved. Instead, before the execution, JavaScript engine parses the declarations during compilation and becomes aware of declarations and their scopes. 
  * Function declaration => hoisted and present actual value.
  * var => hoisted and undefined.
  * let & const => hoisted and TDZ (unitialised and reference error)
  * Function expression & arrow function => depends on using var/ let/ const.
  
* Describe event bubbling.
* Describe event capturing.
* What's the difference between an "attribute" and a "property"?
* What are the pros and cons of extending built-in JavaScript objects?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
* What is strict mode? What are some of the advantages/disadvantages of using it?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
  * JS is a single-thread programming language, it has a single call stack which means that it only runs one thing at a time, line by line in the engine. This event loop consists 3 pieces: call stack, web APIs and task queue. It is a loop that constantly monitoring call stack and task queue. Things like Ajax call, setTimeOut callback and DOM event callback will be registered and run inside Web APIs evironment in a non-blocking way and then passed into task queue, when the call stack is empty, things in task queue gets dequeued and pushed to call stack to be executed.
  * e.g setTimeout: web APIs takes care of timer (say 3s), after 3s the callback func is put in task queue and wait for its turn, once's it gets to the front of the queue and the call stack is empty, it is then put to call stack and get executed.
  
* What are the differences between variables created using `let`, `var` or `const`?
  * Variables declared using the var keyword are scoped to the function in which they are created, or if created outside of any function, to the global object. let and const are block scoped, meaning they are only accessible within the nearest set of curly braces (function, if-else block, or for-loop).
  * var allows variables to be hoisted, meaning they can be referenced in code before they are declared. let and const will not allow this, instead throwing an error.
  *   Redeclaring a variable with var will not throw an error, but let and const will.
  *   
* What are the differences between ES6 class and ES5 function constructors?
* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
* What advantage is there for using the arrow syntax for a method in a constructor?
* What is the definition of a higher-order function?
* Can you give an example for destructuring an object or an array?
* Can you give an example of generating a string with ES6 Template Literals?
* Can you give an example of a curry function and why this syntax offers an advantage?
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
* How can you share code between files?
* Why you might want to create static class members?
* What is the difference between `while` and `do-while` loops in JavaScript?
* What is a promise? Where and how would you use promise?

## Coding questions
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* What will be returned by each of these?
```javascript
console.log("hello" || "world")
console.log("foo" && "bar")
```
* Write an immediately invoked function expression (IIFE)
