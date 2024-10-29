# Lektion-24-10-29

# Lektion Arrays, Loops, Functions

## Arrays
An arrays is just a collection of data. And we can see it as a list of one or more items. The proper terms are and array of different amount of elements. 

In order to have and array you need square brackets `[]`, and inside of those we have items, or elements that are seperated with a comma, it can look like this: 

```js 
[1, 2, 3, 4, 5, 6 , 7, 8, 9, 10]
```

The above is an array of numbers. We can also have an array of string.

```js 
["Johan", "Jerry", "Ruben", "Sebbe", "Måns"]
```

Since we are using JS, we can mix the types inside of and array, This would be prohibited in other langugages as Java or C#. 

```js 
[3, 10, 46, "Johan", true, 24, "Jerry"]; 
```

Even if this is alright, mixing data types inside the array, you shouldn't do that because it's bad practise. Keep the clean, only one data type per array, The array itself can have multiple elements, but they should all be of the same type.

The purpose of an array is to collect larger amouts of data and handle it as one entity. Take the name arrays for instance, instead of creating four variables that must be handled one by one, we can have just one array instead that we handle. Makes it easier and let's us handle bigger amount of data in a easy way. 

For more info, check w3schools.

## Creating arrays

To create an array just create an variable and assign it to an array. 

```js 
const numbers = [46, 34, 10, 77];
```

When we create an array like this, the address, _(reference)_ is saved to the variable. And by address I mean the address to the place on the hard drive with the content of the array is saved. This reference is a so-called pointer. 

Passed/by-reference is something that relates to this. 

## Accesing elements in Arrays

There are two ways to acces elements in an array. The first one, the most common is to acces it by index. Each element in an array is given an index position and this position count always starts from zero. An array is zero-index-based. In order to acces the first element in the array, we access the element on index position 0, the second one on index position 1 and so on..

So to access an alement, we just reference the variable that points to the array, and access it with an index with the help of square brackets, `[]`.

```js 
const numbers = [46, 34, 10, 77];

console.log(numbers[0]); // 46
``` 

The third element: 

```js 
console.log(numbers[2];) // 10
```

The second way of accessing and element in array is  to use an array method called `at()`

Same example access the first element.

```js 
const colors = ["Red", "Green", "Blue", "Orange"];

console.log(colors.at(0)); // Red
```

In the case above, using `at()` allows us to use an negative numbers which starts counting the array backwards. If we type `at.(-1)` the color whould be Blue.So -1 whould be the last element in the array. 

