---
title: "📚 Array methods in JavaScript"
seoTitle: "Array methods in JavaScript"
seoDescription: "While coding in JavaScript, it is most likely that you will fall under circumstances where you have to manipulate an array."
datePublished: Wed Mar 01 2023 13:49:28 GMT+0000 (Coordinated Universal Time)
cuid: clepqi408000309miaxxa7jnc
slug: array-methods-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/cvBBO4PzWPg/upload/0a9293477bd0fd358c5987fc445e2e69.jpeg
tags: javascript, array-methods

---

## 📚 Introduction:

Arrays are one of the most commonly used data structures in JavaScript. They are used to store and manipulate collections of data.

While coding in JavaScript, it is most likely that you will fall under circumstances where you have to manipulate an array.

JavaScript has a variety of built-in array methods that make it easier to work with arrays. In this blog post, we will explore some of the modern array methods in JavaScript and provide examples using emojis to make it fun and easy to understand.

## 🔍 forEach():

The forEach() method executes a provided function once for each array element.

```javascript
const emojis = ["😀", "😆", "😊", "😍"];

emojis.forEach((emoji) => {
  console.log(emoji);
});

// Output:
// 😀
// 😆
// 😊
// 😍
```

## 🔍 map():

The map() method creates a new array with the results of calling a provided function on every element in the calling array.

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map((number) => {
  return number * 2;
});

console.log(doubledNumbers); // Output: [2, 4, 6, 8, 10]
```

## 🔍 filter():

The filter() method creates a new array with all elements that pass the test implemented by the provided function.

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((number) => {
  return number % 2 === 0;
});

console.log(evenNumbers); // Output: [2, 4]
```

## 🔍 find():

The find() method returns the value of the first element in the array that satisfies the provided testing function.

```javascript
const emojis = ["😀", "😆", "😊", "😍"];

const happyEmoji = emojis.find((emoji) => {
  return emoji === "😀" || emoji === "😊";
});

console.log(happyEmoji); // Output: "😀"
```

## 🔍 reduce():

The reduce() method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```javascript
const numbers = [1, 2, 3, 4, 5];

const sumOfNumbers = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);

console.log(sumOfNumbers); // Output: 15
```

## 🔍 some():

The some() method tests whether at least one element in the array passes the test implemented by the provided function.

```javascript
const numbers = [1, 2, 3, 4, 5];

const hasEvenNumber = numbers.some((number) => {
  return number % 2 === 0;
});

console.log(hasEvenNumber); // Output: true
```

## 🔍 every():

The every() method tests whether all elements in the array pass the test implemented by the provided function.

```javascript
const numbers = [2, 4, 6, 8, 10];

const allEvenNumbers = numbers.every((number) => {
  return number % 2 === 0;
});

console.log(allEvenNumbers); // Output: true
```