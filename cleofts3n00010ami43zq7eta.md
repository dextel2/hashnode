---
title: "Promises in JavaScript"
seoTitle: "Promises in JavaScript"
datePublished: Tue Feb 28 2023 16:02:50 GMT+0000 (Coordinated Universal Time)
cuid: cleofts3n00010ami43zq7eta
slug: promises-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677600006477/367de55c-7f24-47d3-97dd-9395534a3a4f.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1677600143778/5260ce32-b756-40a3-bc9d-3bf3e143af52.webp
tags: javascript, promises, axios

---

Asynchronous programming in JavaScript can be quite complex and difficult to manage. However, the introduction of Promises in ES6 made it easier for developers to handle asynchronous tasks. In this article, we will discuss what Promises are and how they work, using an example with [axios](https://www.npmjs.com/package/axios), a popular library for making HTTP requests.

What are Promises in JavaScript? A Promise is a JavaScript object representing the eventual completion or failure of an asynchronous operation. It is a container for a value that may not yet be available. A Promise can be in one of three states:

1. Pending: The initial state of a Promise before it completes or fails.
    
2. Fulfilled: The Promise has been completed successfully and the resulting value is available.
    
3. Rejected: The Promise has failed, and the reason for the failure is available.
    

Promises in JavaScript provide a way to write asynchronous code that looks and behaves like synchronous code. They allow us to avoid callback hell, where we have multiple nested callbacks, which can be difficult to read and maintain.

## An Example with Axios:

Axios is a popular library for making HTTP requests in JavaScript. It returns a Promise for handling asynchronous responses. Let's look at a simple example of using Axios to fetch data from an API:

```javascript
const axios = require('axios');

axios.get('https://jsonplaceholder.typicode.com/posts/1')
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.log(error);
  });
```

In the code above, we make an HTTP GET request to the JSONPlaceholder API to get a post with ID 1. Axios returns a Promise that we handle using the `.then()` and `.catch()` methods. If the Promise is fulfilled, we log the data from the response. If the Promise is rejected, we log the error message.

Let's break down how the above code works:

1. We import the Axios library using `require`.
    
2. We call the `.get()` method on the Axios object, passing in the URL of the API we want to fetch data from.
    
3. The `.get()` method returns a Promise, which we handle using the `.then()` and `.catch()` methods.
    
4. If the Promise is fulfilled (i.e., the API request is successful), the `.then()` method is called with the response object, which contains the data we want to access. We log this data to the console.
    
5. If the Promise is rejected (i.e., the API request fails), the `.catch()` method is called with the error object, which contains information about the error. We log this error message to the console.
    

## Benefits of Promises

Promises in JavaScript provide several benefits, including:

1. Avoiding callback hell: Promises allow us to write asynchronous code that looks and behaves like synchronous code, making it easier to read and maintain.
    
2. Better error handling: Promises provide a more structured way of handling errors, making it easier to identify and debug issues in our code.
    
3. Chaining operations: Promises allow us to chain multiple asynchronous operations together, making it easier to write complex asynchronous code.