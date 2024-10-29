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

In the case above, using `at()` allows us to use an negative numbers which starts counting the array backwards. If we type `at.(-1)` the color would be Blue. So -1 whould be the last element in the array. 

## Modifying elements in Arrays

In order to edit and element we need to know  its index position and the we can just use square brackets so in order to access it and modify it.  We modify it by assigning a new value to it

```js 
const colors = ["Red", "Green", "Blue", "Orange"];
colors[0] = "Yellow" // Changes Red to Yellow
console.log(colours); 

colors[2] = "Brown";
console.log(colors) 
```

We can also update an element of an array with  `with()`. The difference is that this metoh takes two parameters. The frist one is the index position of the element we want to change. The second one is the new value that we want to give that element. Then a copy of array is returned to us with the modifications. 

```js 
const colors = ["Red", "Green", "Blue", "Orange"];

const updatedColors = colors.with(1, "Pink");
console.log(updateColors);
console.log(colors);
```

## Properties of Arrays

Properties are just fixed values, in our case the property we are interested in is the `.length` -property. This property gives us the length, as a number, of the array to us. If we have fice elements in an array, the valuse of length will be 5.

```js 
const colors = ["Red", "Green", "Blue", "Orange"];

const length = colors.length; // Here we jsut save the value to a variable, we do not have to this. 
console.log(length); // 4
console.logg(colors.length); // 4
``` 

So if we add or remove elements of the array, this value will update accordingly. 

## Array Methods

A method is just a set of intructions that are predefined and bundle inside a methos. These instructions are usually very common and instead of us writing the same code over and over, JS has created this method for us to use whenever we want to. 

#### push(itme2, item2, item...) => new length of array

Is used to add an element to the end of a existing array. It takes one or more parameterrs, and theses parameters are the new elements to be added. It also returns something , and that something is the new length of the array. 

```js
const numbers = ["1", "2", "3", "4", "5", "6", "7", "8";]

// Let's push a 9 to the end. 
number.push(9);

//Let's push 10 and 11 to the end
number.push(10, 11); 

// Push 12 and save the new length in a new variable
const newLength = numbers.push(12); 
console.log(newLength);
```

#### pop( ) => the removed element

Is ised to remove the last element of an array. The element that was removed is also returned by the mothod. 

```js
const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"]; 

// Remove the last element and ignore the reurn value
cities.pop();
console.log(cities);
``` 

#### unshift(item1, item2, item...) => new length of array

Is used to add an element to the beginning of the array instead of the end. It also returns the new length of the array as a number. 

```js 
const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"];

cities.unshift("Linköping"); 
console.log(cities); 
```

#### shift() => The removed element

Is used to remove an element from the beginning of the array and reurns that removed element. 

```js 
const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"];

cities.shift();
console.log(cities); // Removes Stockholm
```

#### includes(item) => Boolean (True/False) 

Is used to check if an item/element exists in an array or not. The parameter is the item/element we are looking for and the return value either true or false. 

```js 
const numbers = [2, 4, 6 , 8, 10];

if (numbers.includes(6)) {
    console.log("The number 6 exists in the array");

}   else {

    console.log("There is no number 6 in the array");
}

const number8Exist = numbers.include(8);
if (number8Exist) {
    // Do something if number 8 exists
}
```

If you have more complex conditions in your if checks, always try to store them in variables with readable names instead. It makes the code more readable and maintainable. 

#### indexOf(item) => the index position OR -1 if it doesn't exist.

Is used to find an index position of a specific item/element inside tthe array. If it exists, the index is returned as a number, and if it doesn't, negative one `-1` is returned. Keep that in mind when using it in if checks. 

```js
const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"];

const indexOfMalmö = cities.indexOf("Malmö"); 
console.log(cities);
console.log(indexOfMalmo); 
``` 

 If we try to get an index that doesn't exist, will get back `-1`. 

 ```js
 const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"];

const indexOfSkurup = cities.indexOf("Skurup"); 
console.log(indexOfMalmo); // -1
```

Remember, if you use this in if check, check for `-1` if you want to do something it the item doesn't exist in the array. 

#### join() => A string including all the elements

Is used to convert a array of elements to a string containing those elements. It doesn't matter if it's numbers, string or something else, the method always tries to convert everything to a long string. It also takes a parameter that is a character that will be used to seperate the elements with. Can be an empty space, dash, underscore or any other character. The seperator is optional, hence the question matk in the syntax. 

```js 
const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"];

const citiesAsstring = cities.join();
```

If we don't specify a seperator, per default every element will be seperated with a comma. 

```js
console.log(citiesAsString); // Stockholm,Göteborg,Malmö,Lund
``` 

```js 
const cities = ["Stockholm", "Göteborg", "Malmö", "Lund"];

const citiesAsString = "StockholmGöteborgMalmöLund"; 

"Stockholm-Göteborg-Malmö-Lund"
// Above, just an example. Hard to read, not good.
```

In short, `join()` converts an array to an string with and seperates every element with a separator, that is defined inside `join()` - `join( / )` gives an / beetwen the cities, for example. 

#### splice(start, deleteCount, item1?, item2?, Item?...) => 

The splice method lets us modify the content of an array on any given index position. 

It takes several parameters. The first one is the index on which we would like to start our modification. 

The next one is the delete count, how many elements do we want to delete? If we don't want to delete anything we just assign 0 to this parameter. If we delete something it will `start` deleting from the start parameter, in other words the index position we assign to `start`. 

The third one (or more) is the nwe items/elements we whould like to add to the array. 