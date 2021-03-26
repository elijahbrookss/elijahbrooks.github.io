---
layout: post
title: Difference Between a Framework And a Package
subtitle: Detailed breakdown on the difference between the two
cover-img: /assets/img/2021-03-25/Difference-between-Framework-and-Library-1.png
thumbnail-img: /assets/img/2021-03-25/Difference-between-Framework-and-Library-1.png
share-img: /assets/img/2021-03-25/Difference-between-Framework-and-Library-1.png
tags: [library, frameworks, web development]
readtime: true
---

In the developer community the words 'framework' and 'library' are constantly being thrown around and are used interchangeably. But  there is a crucial difference between the two. This blog is going to go over the difference between the two and provide several examples for a framework and a library.

The similarity between a 'framework' and a 'library' is that they are both code written by someone else that can be used in your code to solve problems. I've often been told that frameworks and libraries are like magic and make your code easier. Unfortunately that's not the case. There's nothing magical about frameworks or libraries. Both frameworks and libraries are re-usable code that can help you solve problems easier and efficiently. Most often these libraries and frameworks take the tediousness of code away from you so you can focus on the meat of your app and not the tedious parts.

Let's have an example of what a library exactly is. Let's say you're using the following code to check for if an item is present in an array. We're going to pretend as if there's no high order array functions for this method just for the simplicity of the example.

```javascript
const isElementInArray = (element, arr) => {
  let isInArray = false;
  for (let i = 0; i < arr.length; i++){
    if (arr[i] === element) {isInArray = true}
  }

  return isInArray
}
```

If you were to import this code into an app to check and see if an element was in an array then congratulations you just created a library! Here's a real world example on what a library is. You can think of a library as a ...
