---
title: "Understanding Shallow Copy vs Deep Copy using lodash"
seoTitle: "Shallow Copy Vs Deep copy in JavaScript"
seoDescription: "There are two main types of cloning in JavaScript: shallow copy and deep copy. Shallow copy creates a new object with the same properties as the original"
datePublished: Mon Feb 27 2023 14:08:36 GMT+0000 (Coordinated Universal Time)
cuid: clemwb0k500100al8akuu4x9f
slug: understanding-shallow-copy-vs-deep-copy-using-lodash
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/g5jpH62pwes/upload/d20aab4579b7eaaf60fb9e9a65d4d5d0.jpeg
tags: javascript, lodash, shallowcopy, deep-copy-vs-shallow-copy

---

Cloning an object in JavaScript is an important operation that allows you to create a copy of an existing object without modifying the original. This can be useful in many situations, such as when you want to make changes to an object without affecting the original or when you want to pass an object to a function without modifying it.

There are two main types of cloning in JavaScript: shallow copy and deep copy. Shallow copy creates a new object with the same properties as the original, but the values of the properties are references to the original object's values. Deep copy creates a new object with the same properties as the original, but the values of the properties are copies of the original object's values. In this blog post, we will explore how to clone objects in JavaScript using both shallow copy and deep copy using the popular JavaScript library Lodash.

## Shallow Copy

Shallow copying of an object is a simple operation that can be achieved using Lodash's `clone` method. This method creates a new object with the same properties as the original object, but the values of the properties are references to the original object's values.

Here's an example of how to use the `clone` method:

```javascript
const originalObj = { name: 'John', age: 30, address: { street: 'Main St', city: 'New York' } };
const clonedObj = _.clone(originalObj);

console.log(clonedObj === originalObj); // false
console.log(clonedObj.address === originalObj.address); // true
```

In this example, we first create an object called `originalObj` with three properties: `name`, `age`, and `address`. The `address` property is itself an object with two properties: `street` and `city`.

We then use lodash's `clone` method to create a shallow copy of the `originalObj` and assign it to a new variable called `clonedObj`. We then log the result of two comparisons to the console: the first compares `clonedObj` and `originalObj` to check if they are the same object (which they are not), and the second compares the `address` property of `clonedObj` and `originalObj` to check if they are the same object (which they are).

As you can see, the `clone` method creates a new object with the same properties as the original object, but the values of the properties are references to the original object's values. This means that if you modify the `address` property of `clonedObj`, it will also modify the `address` property of `originalObj`, because both properties reference the same object.

## Deep Copy

Deep copying an object is a bit more complex than shallow copying, because you need to create copies of all the nested objects as well. Lodash's `cloneDeep` method makes this easy by recursively creating copies of all the nested objects in the original object.

Here's an example of how to use the `cloneDeep` method:

```javascript
const originalObj = { name: 'John', age: 30, address: { street: 'Main St', city: 'New York' } };
const clonedObj = _.cloneDeep(originalObj);

console.log(clonedObj === originalObj); // false
console.log(clonedObj.address === originalObj.address); // false
```

In this example, we use the same `originalObj` object as in the previous example, but we use Lodash's `cloneDeep` method to create a deep copy of the object instead of a shallow copy. We assign the result to a new variable called `clonedObj`.

We then log the result of two comparisons to the console: the first compares `clonedObj` and `originalObj`