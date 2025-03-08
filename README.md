# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Imagine you are giving a brief lesson on Recursion to a relatively new programmer. In your lesson make sure to include the following:

- A formal definition of recursion (feel free to quote an official source like MDN)
- An example in code.
- An explanation of the code example.
- An explanation of the kinds of functions that are best solved using recursion.

### Response 1

Recursion is a concept in programming where a fuction calls itself to solve smaller instances of the problem. It is typically used to solve problems that can be broken down into simpler, smaller subproblems, with the function continuing to call itself until it reaches a base case, which is the condition where the recursion stops.

```javascript
const recursiveFunction = (num) => {
  if (num <= 0) return num; // base case

  return recursiveFunction(num - 1); // recursive call
};
```

The function above takes a number argument `num` and counts down from that number until reaches 0 and returns. Now let's break down what is happening line by line inside of our `recursiveFunction `, In the first line we're setting up a base case to stop our recursion from entering into an infinite loop of recursive calls, Yes it's pretty bad!... In this example we're going to return `num` if num's value is 0, otherwise we're going to return a recursive call and pass it `num - 1` as an argument, at some point depending on num's value, `num` will be equal to 0 so we'll return `num` and exit function.

## Prompt 2

Imagine you are giving a brief lesson on the Tree data structure to a relatively new programmer. In your lesson make sure to include the following:

- A formal definition of a Tree (feel free to quote an official source like MDN)
- Definitions for key terms like **root**, **leaf**, **depth**, and **height** as they relate to Trees
- An example in code.
- An explanation of the code example.

### Response 2

## Prompt 3

Any iterative function can be written recursively. Provide an example of an iterative function and the same function written recursively. Then, explain the benefits and/or drawbacks of each approach.

### Response 3

**Iterative Function**

```javascript
// takes an array and a value and return value's index position in the array if it exists
const findByValue = (array, value) => {
  for (let i = 0; i < array.length; i++) {
    // if value exists in array return current index
    if (array[i] === value) return i;
  }
  // if value is not found then it returns -1
  return -1;
};
```

**Recursive Function**

```javascript
// takes an array and a value and return value's index position in the array if it exists. Also has a parameter i that defaults to 0.
const findByValue = (array, value, i = 0) => {
  // if value exists in the array then return current index.
  if (array[i] === value) return i; //base case 1
  console.log(array[i]);
  // if i's value is equal to the length of array return -1
  if (i === array.length) return -1; //base case 2
  // recursive call
  return findByValue(array, value, i + 1);
};
```

Between these two cases for this type of problem we should go with the iterative approach. This is because Iteration uses a for loop, which is straightforward and typically more efficient in terms of performance. It doesn’t involve function calls and stack overhead and this is easy to understand, especially for developers who are more familiar with loops. It's clear in its flow, which can make debugging easier.

## Prompt 4

Depth-first-search is an algorithm of traversing through a tree that explores as far as possible along a single branch before backtracking and exploring other branches. The three approaches for depth-first-search are "inorder", "preorder", and "postorder".

Using this tree as an example, explain the differences between these three approaches, providing implementations of each (recursive or iterative, its up to you but one of them is definitely cleaner).

```

    A

/ \
 B C
/ \ \
D E F

```

### Response 4

```

```
