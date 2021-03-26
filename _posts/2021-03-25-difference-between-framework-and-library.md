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

# Framework Vs. Package

In the developer community the words 'framework' and 'library' are constantly being thrown around and are used interchangeably. But  there is a crucial difference between the two. This blog is going to go over the difference between the two and provide several examples for a framework and a library.

The similarity between a 'framework' and a 'library' is that they are both code written by someone else that can be used in your code to solve problems. I've often been told that frameworks and libraries are like magic and make your code easier. Unfortunately that's not the case. There's nothing magical about frameworks or libraries. Both frameworks and libraries are re-usable code that can help you solve problems easier and efficiently. Most often these libraries and frameworks take the tediousness of code away from you so you can focus on the meat of your app and not the tedious parts.

## Library Example

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

### Library
If you were to import this code into an app to check and see if an element was in an array then congratulations you just created a library! Here's a real world example on what a library is. You can think of a library as a dish soap. You already have the towel and water all you need is the soap so you can wash the dish. You are in control.

![dish-soap](/assets/img/2021-03-25/dish-soap.jpg)

### Framework
A Framework on the other hand, is like the dishwasher. It's the system that's going to wash the dish you just need to add the soap, water, and dish. The dishwasher is the one in control and it will be in charge of washing the dishes.

![dish-washer](/assets/img/2021-03-25/dish-washer.png)

## The Technical Difference

The technical difference between a framework and library lies in a term called inversion of control. Inversion control is all about inverting the control. To explain this in layman's terms, suppose you drive a car to your work place. This means you control the car. The inversion control principle suggests to invert the control, meaning that instead of driving the car yourself, you hire a cab, where another person will drive the car. Thus, this is called inversion of the control - from you to the cab driver. You don't have to drive a car yourself and you can let the driver do the driving so that you can focus on your main work.

When you use a library, you are in charge of the flow of the application. You are choosing when and where to call the library. When you use a framework, the framework is in charge of the flow. It provides some places for you to plug in your code, but it calls the code you plugged in as needed.
