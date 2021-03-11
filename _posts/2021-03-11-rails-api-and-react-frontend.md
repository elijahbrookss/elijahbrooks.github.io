---
layout: post
title: Rails API and React Frontend Structure
subtitle: How the Rails API and React frontend structure works
cover-img: /assets/img/api-banner.jpg
thumbnail-img: /assets/img/react-rails.png
share-img: /assets/img/react-rails.png
tags: [computer science, programming, languages, react, rails]
readtime: true
---

# The Structure of a Rails API and React Frontend Web Application


When learning how to code in a boot camp, the goal of the boot camp is for their students to graduate with abilities to use various popular frameworks and stacks. One issue I found with this method is that with the quick amount of time students are introduced to stacks, there's not much time or resources spent understanding why that stack was chosen or the bigger picture of the stack in the first place.

As a side note I'm not going to go into how to set this up physically, this post is for the understanding of how this certain stack works.

### What Is an API? (Application Programming Interface)

First let's start off with our understanding of what an API is. By definition an API is a software intermediary that allows two applications to talk to each other. Each time you use an app like Facebook, send an instant message, or check the weather on your phone, you’re using an API.

**Well what does that mean for our Rails API  + React application?**

In a Rails API and React application we have two apps our Rails backend which contains our models, routes, and controllers, and we have our React frontend which contains our styling, user input, and user interface. So what building an API allows us to do is communicate from our backend to our frontend in the form of requests.

Below is an illustration of how this works.

![api-model](/assets/img/api-model.png)

As you can see in the illustration whenever a user interacts with the web site (React frontend) the frontend sends a request through the API (Rails API) to our web server and database (Rails). But how exactly does an API, more specifically our Rails API, communicate between the two apps?

## How APIs Communicate to Other Applications

As with real languages, when mediating between two different languages there has to be a median language that both sides understand. What is that language for web applications? One of the most popular and one of my favorites is JSON. JSON stands for **J**ava**S**cript **O**bject **N**otation. JSON allows us to turn any JavasScript object into JSON and send JSON to the server. We can also convert any data the server sends through into JSON so that JavaScript can understand it. This is EXTREMELY useful because now we can read and work with data from both sides!

Below is an example of what JSON looks like.

![api-model](/assets/img/json-example.jpg)

As you can see all JSON is, is a giant string object. Which is why it's readable on both sides, Rails API and React frontend. React isn't the only frontend this works with however, since JSON stands for **J**ava**S**cript **O**bject **N**otation, we can assume that it works for any framework or frontend that involves JavaScript. Isn't that amazing!

But what happens when the API sends the request through our Rails API?
## Deeper Dive Into Rails API

As mentioned earlier, JSON can convert any JavaScript models into JSON for our Rails API to then pick up and use. But what can our Rails API do with this JSON data? Well that's completely up to you! Since you're reading this blog I'm assuming you already know about routes and controllers. As a recap, when you set up a controller you're deciding what to do with the information sent when a request is given for a certain route. You can assume a certain build for the data you're going to receive and dish out your own data as well.

Something more commonly done with Rails API is the transfer of JWT or JSON Web Tokens. I won't go in too much detail on JWT in this blog, but since you're able to turn data into string which can be read by the server, you can now check the authentication of a user by sending their token through the API to verify if the user is who they claim to be.

For more information on the topics discussed in this post refer to the links below.

### For More Information:
* [What is an API?](https://www.mulesoft.com/resources/api/what-is-an-api)
* [What are web tokens?](https://jwt.io)
* [How to use an API with Ruby](https://rapidapi.com/blog/how-to-use-an-api-with-ruby/)
