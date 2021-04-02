---
layout: post
title: JavaScript Variable Types
subtitle: Var, Let, and Const
cover-img: /assets/img/2021-04-01/cover-img.jpg
thumbnail-img: /assets/img/2021-04-01/share-img.png
share-img: /assets/img/2021-04-01/share-img.png
tags: [web development, javascript]
readtime: true
---
# Var, Let, and Const


## History of JavaScript
The three variables 'var', 'let', and 'const' are three ways you can declare variables in JavaScript. ES6 brought about let and 'const' which can be a confusing concept for those not familiar with JavaScript. So I'm going to go over the difference between all three variables. Before ES6 the only way to declare variables was with var.


## Var

Declaring a variable with 'var' scopes the variable to whatever the current execution context is. In other words, if a variable is declared with 'var' inside of a function, we'd only have access to that variable inside of the function. The same can be said for if a variable is declared globally. As you might've already guessed, declaring a variable globally allows the usage of that variable anywhere. Here's an example of this.

```javascript
var person1 = 'Programmer';
console.log(person1) // Outputs 'Programmer'

function printPerson(){
  var person2 = 'Programmer2';
  console.log(person2); // Outputs 'Programmer2'
  console.log(person1); // Outputs 'Programmer'
}

console.log(person2); // error
```

In this example, 'person2' is scoped inside of the 'printPerson' function scope. 'person1' on the other hand, belongs to the global scope. This allows 'person1' to be called anywhere in the file. As you can also see, trying to access the 'person2' variable outside of the function scope causes an error because it's outside of the declared execution context.

You might start to be thinking that there's nothing new here, this is the regular and usual flow of a variable. However, one issue with declaring a variable with 'var' is that you can re-declare the same variable multiple times. Here's an example below.

```javascript
var person1 = 'John';
var person1 = 'Jane';

console.log(person1) // Outputs 'Jane'
```

If this is intentional there may not be an evident issue however, if this wasn't intentional this can cause some really bad outcomes and may cause a lot of time debugging because of a minor typo of re-declaring 'person1'. Another issue with 'var' is that it's not block scoped. In other words, if declaring a variable in a block the variable will continue to survive outside of the block. Here's an example of this issue.

```javascript
for (var i; i < 10; i++){
  console.log(i);
}
console.log(i); // Outputs 10
```

As you can see, when outside of the loop the initialized variable 'i' is still accessible. ES6's 'let' was an answer to this issues.

## Let

'let' is the new and improved version of 'var'. 'let' is JavaScript's answer to all the issues variables declared with 'var' brought about. Variables declared with 'let' creates variables that are block-scoped, and prevents redeclaration. Let's see an example of how to use 'let'.

```javascript
let person1 = 'Programmer';
console.log(person1) // Outputs 'Programmer'

function printPerson(){
  let person2 = 'Programmer2';
  console.log(person2); // Outputs 'Programmer2'
  console.log(person1); // Outputs 'Programmer'
}

console.log(person2); // error
```

As you can see the expected variable behavior for variables declared with 'let' is the same. At first glance it may seem that he scoping of variables declared with 'let' and 'var' are the same but let's see what happens with variables declared with 'let' in block scopes.

```javascript
for (let i; i < 10; i++){
  console.log(i);
}
console.log(i); // error
```

When you attempt to access a variable declared with 'let' outside of the block it was declared in you'll get an error. This is what 'block-scoped' means, the variables are scoped to the block they are declared in. Another benefit to 'let' is that they prevent redeclarations. Below is an example of this.

```javascript
let person1 = 'John';
let person1 = 'Jane';
// Error
```

When attempting to redeclare a variable already declared with 'let' you'll get an error. This is a major benefit when debugging code because you don't have to worry about minor details like accidentally redeclaring a variable. Last but not least we have 'const'.

## Const

'const' is short for constant so as you may have already guessed variables declared with 'const' are expected to be constants. This means that you're not able to re-assign these variables. Same like 'let', 'const' variables are block-scoped. Here's an example of how you would use a 'const' variable.

```javascript
const person1 = 'John';
person1 = 'John';
// Error, can't reassign const variables

const person1 = 'Jane';
// Error, can't redeclarte const variables
```

I think it's a good practice to use 'let' and 'const' over 'var' because of the benefits and restrictions that come with 'let' and 'const' that don't come with 'var'. Using 'let' and 'const' can potentially save you lots of time debugging your projects.

Happy Coding!

## For More Information:
* [ES6 Features](http://es6-features.org/#Constants)
* [JavaScript Features](https://www.freecodecamp.org/news/var-let-and-const-whats-the-difference/)
