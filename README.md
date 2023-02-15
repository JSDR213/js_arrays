### JSDR 213

# JavaScript Arrays

![Arrays](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fcleverbeagle-uploads%2FWhat-are-JavaScript-arrays-BPH.png&f=1&nofb=1)

## Lesson Overview

## Objectives
 - Learn about JavaScript Arrays
 - Do some practice with JavaScript Arrays

## Lesson Instructions

### Arrays

Unfortunately, strings and numbers are not enough for most programming purposes.
What is needed are collections of data that we can use efficiently: **Arrays**.

Arrays are great for:
 * Storing data
 * Enumerating data, i.e. using an index to find them
 * Quickly reordering data

Arrays, ultimately, are a data structure that is similar in concept to a list. Each item in an array is called an element, and the collection can contain data of the same or different types. In JavaScript, they can dynamically grow and shrink in size.

```javascript
let friends = ['Moe', 'Larry', 'Curly'];
=> ['Moe', 'Larry', 'Curly']
```

Items in an array are stored in sequential order, and indexed starting at `0` and ending at `length - 1`.

```javascript
// First friend
let firstFriend = friends[0];
 => 'Moe'
// Get the last friend
let lastFriend = friends[2]
=> 'Curly'
```

We can even use strings like arrays:

```javascript
let friend = "bobby bottleservice";
// pick out first character
friend[0]
//=> 'b'
friend.length
//=> 19
```

![Ray](https://c.tenor.com/lK9WCmPFfUIAAAAC/finding-nemo-sting-ray.gif)

### Working with Arrays

Using the JavaScript Keyword `new`, is one way of creating arrays:

```javascript
let a = new Array;
=> undefined

a[0] = 'dog';
=> "dog"

a[1] = 'cat';
=> "cat"

a[2] = 'hen';
=> "hen"

a
=> ['dog', 'cat', 'hen']

a.length;
=> 3
```

A more convenient notation is to use an array literal:

```javascript
let a = ['dog', 'cat', 'hen'];

a.length;
=> 3
```

![Length](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia.giphy.com%2Fmedia%2F3o7btOtfwq4iFqCxb2%2Fgiphy.gif&f=1&nofb=1)

### Length method

The `length` method works in an interesting way in Javascript. It is always one more than the highest index in the array.

So `array.length` isn't necessarily the number of items in the array. Consider the following:

```javascript
let a = ['dog', 'cat', 'hen'];
a[100] = 'fox';
a.length; // 101
```

**Remember**: the length of the array is one more than the highest index.

### Getting data from an array

If you query a non-existent array index, you get `undefined`:

```javascript
let a = ['dog', 'cat', 'hen'];

a[90];
=> undefined
```

### Array Helper Methods

Arrays come with a number of methods. Here's a list of some popular helpers:

> Note: You might want to demonstrate a few of these.

- `a.toString()` - Returns a string with the `toString()` of each element separated by commas.

- `a.pop()` - Removes and returns the last item.

- `a.push(item1, ..., itemN)` - `Push` adds one or more items to the end.

- `a.reverse()` - Reverse the array.

- `a.shift()` - Removes and returns the first item.

- `a.unshift(item)` - Prepends items to the start of the array.

![Shift](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia.giphy.com%2Fmedia%2Fo5BzNDDFQnepi%2Fgiphy.gif&f=1&nofb=1)


Like scales on the guitar, or spices in a kitchen, the more Array Methods you are familiar with, the more you will be able to do with your code. Don't give yourself a headache trying to memorize all of them. With practice and repetition you will see the uses and abilities of each, and how best to find them to use.


### ES6
![...](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.sheknows.com%2Fwp-content%2Fuploads%2F2018%2F08%2Fellipsis_xr1tub.gif&f=1&nofb=1)

#### Spread Operator Syntax

ES6 introduced the spread syntax for dealing with cases when we want to generate new versions of Arrays and Objects in a clean, readable manner.

The basic intuition behind `...` is that it "spreads out" or "unpacks" all of the values in an Array or Object.

```javascript
const evens = [2, 4, 6];
const odds = [1, 3, 5];

const moreEvens = [...evens, 8, 10];

console.log(moreEvens);
```

<details>
    <summary>Output:</summary>
    
```
[ 2, 4, 6, 8, 10 ]
```

</details>

Without the `...` we would have gotten the following:

```
const evens = [2, 4, 6];
const odds = [1, 3, 5];

const moreEvens = [evens, 8, 10];

console.log(moreEvens);
```
<details>
    <summary>Output:</summary>
    
```
[ [ 2, 4, 6 ], 8, 10 ]
```

</details>

The spread syntax allows us to seamlessly integrate nested values with other elements in a single array.

The order is still preserved when spreading out multiple arrays.

We can easily use more than one spread operator in a single line:

```javascript
const evens = [2, 4, 6];
const odds = [1, 3, 5];

const nums = [...evens, ...odds, 8, 9, 10];

console.log(nums);
```

<details>
    <summary>Output:</summary>
    
```
[ 2, 4, 6, 1, 3, 5, 8, 9, 10 ]
```

</details>


## Lesson Recap
In this lesson, we learned all about JavaScript arrays and how they are used to store data.  We also touched on array methods and how they can be used to affect that data!

## Resources
 - [Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
