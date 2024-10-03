---
title: "JavaScript : Understanding hasOwnProperty"
seoTitle: "JavaScript Understanding hasOwnProperty"
datePublished: Mon Feb 27 2023 13:37:55 GMT+0000 (Coordinated Universal Time)
cuid: clemv7k21000i09jq0kkm6yau
slug: javascript-understanding-hasownproperty
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/ZS67i1HLllo/upload/f435d4343dad6fe37fcea45153912a20.jpeg
tags: javascript, object

---

JavaScript is a programming language that is widely used in web development. It provides developers with several useful built-in methods and functions that make it easy to work with objects and manipulate their properties. One such method is `hasOwnProperty()`. In this blog, we will discuss what `hasOwnProperty()` is, how it works, and when to use it.

## What is `hasOwnProperty()`?

`hasOwnProperty()` is a built-in method of the JavaScript `Object` class. It is used to determine whether an object has a property with a specific name. The method returns a boolean value indicating whether the object has the specified property as a direct property of the object itself. In other words, it checks if the property exists on the object and not on its prototype chain.

## Syntax of `hasOwnProperty()`

The syntax of `hasOwnProperty()` is as follows:

```javascript
object.hasOwnProperty(property)
```

Here, `object` is the object that you want to check for the presence of a property, and `property` is the name of the property that you want to check.

## How does `hasOwnProperty()` work?

When you call `hasOwnProperty()` on an object, it checks if the object has a property with the specified name. If the property exists on the object itself, the method returns `true`. Otherwise, it returns `false`.

For example, consider the following object:

```javascript
let obj = {
  name: "John",
  age: 30
};
```

To check if the `obj` has a property named `name`, you can call the `hasOwnProperty()` method as follows:

```javascript
console.log(obj.hasOwnProperty("name")); // Output: true
```

Similarly, to check if the `obj` has a property named `address`, you can call the `hasOwnProperty()` method as follows:

```javascript
console.log(obj.hasOwnProperty("address")); // Output: false
```

## When to use `hasOwnProperty()`?

The `hasOwnProperty()` method is particularly useful when you want to check if an object has a specific property and you want to make sure that the property exists on the object itself and not on its prototype chain. This is important because if the property exists on the object's prototype chain, it may not have the value that you expect.

For example, consider the following object:

```javascript
let person = {
  name: "John",
  age: 30
};

let employee = Object.create(person);
employee.salary = 50000;
```

Here, the `employee` object is created using the `Object.create()` method, with `person` as its prototype. This means that `employee` inherits the properties of `person`, including `name` and `age`. However, `employee` also has a property named `salary`, which is not present on `person`.

To check if the `employee` object has a property named `salary`, you can call the `hasOwnProperty()` method as follows:

```javascript
console.log(employee.hasOwnProperty("salary")); // Output: true
```

Similarly, to check if the `employee` object has a property named `name`, you can call the `hasOwnProperty()` method as follows:

```javascript
console.log(employee.hasOwnProperty("name")); // Output: false
```

Here, `employee` does not have its own `name` property. Instead, it inherits the `name` property from its prototype `person`. Therefore, calling `hasOwnProperty()` on `employee` with the argument `name` returns `false`.