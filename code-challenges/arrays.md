# Code Challenges about Arrays - JavaScript

## Resources:

- [Techtonica Lesson about Arrays](https://github.com/Techtonica/curriculum/blob/main/javascript/javascript-2-array-functions.md)

## Motivation

Techtonica's JavaScript lessons set a solid foundation in JavaScript basics so we can use the language in more robust ways in later studies. Nevertheless, you want to practice problems that use arrays as a preparation for your technical interview.

## Objectives

Participants will be able to:

- Work each problem as a code challenge
- Work their solutions using functions
- Test their solutions with several test cases

## Things to Remember

Make sure that you know the answer to this questions:

  

- What do the methods `push()` and `pop()` do?

- How would you access the first and last item in an array?

- What does `arrayName.length` do?

- How would you index into the following array to get Cookie? 
`let dessertArray = [ ["Pie", 4], ["Cupcake”, 5], ["Cookie", 12] ];`

- What's the difference and similarities between `var`, `let` and `const`?

- What's the difference between parameters and arguments? Show an example.

- What is the difference between local scope and global scope?

### Problem Sets

Question | Test Cases | Solutions

#### Problem 1 -

Write a function that takes in an array and joins all elements of the array into a string.

Sample Solution:
```
// Javascript
function arrayToString(array) {

	return array.join(" ");

}

// Test Cases:
console.log(arrayToString(['Hello', 'World', 'How', 'Are', 'You'])); 
// Expected Output: "Hello World How Are You"
console.log(arrayToString(['l', 'Am', 'Learning', 'How', 'To', 'Code']));
// Expected Output: "l Am Learning How To Code"
console.log(arrayToString(['I', 'Love', 'Techtonica']));
// Expected Output: "I Love Techtonica"
```
#### Problem 2 -

Store a set of words in an array and display the contents both forward and backward.

Sample Solution:
```
// Javascript
function reverseArray(array) {

	return array.reverse();

}

// Test Cases:
console.log(reverseArray(['Hello', 'World', 'How', 'Are', 'You']));
// Expected Output: ['You', 'Are', 'How', 'World', 'Hello']

console.log(reverseArray(['l', 'Am', 'Learning', 'How', 'To', 'Code']));
// Expected Output: [“Code”, “To”, “How”, “Learning”, “Am”, “l”]

console.log(reverseArray(['I', 'Love', 'Techtonica']));
// Expected Output: [“Techtonica”, “Love”, “I”]
```

  

#### Problem 3 -

Given an array of ints, return true if one of the first 4 elements in the array is a 9. The array length may be less than 4.

Sample Solution:
```
// Javascript
function array_front9(array) {

	return array.slice(0, 4).includes(9);

}

// Test Cases:
console.log(array_front9([1, 2, 9, 3, 4]));
// Expected Output: true
console.log(array_front9([1, 2, 3, 4, 9]));
// Expected Output: false
console.log(array_front9([1, 2, 3, 4, 5]));
// Expected Output: false
```

#### Problem 4 -

Given an array of ints, return true if the sequence of numbers 1, 2, 3 appears in the array somewhere.

Sample Solution:
```
// Javascript
function array123(array) {

	return array.join("").includes("123");

}

// Test Cases:
console.log(array123([1, 1, 2, 3, 1]));
// Expected Output: true
console.log(array123([1, 1, 2, 4, 1]));
// Expected Output: false
console.log(array123([1, 1, 2, 1, 2, 3]));
// Expected Output: true
```
  

#### Problem 5 -

Given an array of ints, return the number of 9's in the array.

Sample Solution:
```
// Javascript
function array_count9(array) {

	return array.filter((num) => num === 9).length;

};

// Test Cases:
console.log(array_count9([1, 2, 9]));
// Expected Output: 1
console.log(array_count9([1, 9, 9]));
// Expected Output: 2
console.log(array_count9([1, 9, 9, 3, 9]));
// Expected Output: 3
```
 
#### Problem 6 -

  
Given an array of ints, return true if 6 appears as either the first or last element in the array. The array will be length 1 or more.

You must solve this in O(1) time, which means without looping through the array

Sample Solution:
```
// Javascript
function first_last6(array) {

	return array[0] == 6 || array[array.length -1] == 6;

}

// Test Cases:
console.log(first_last6([1, 2, 6]));
// Expected Output: true
console.log(first_last6([6, 1, 2, 3]));
// Expected Output: true
console.log(first_last6([13, 6, 1, 2, 3]));
// Expected Output: false
```
  

#### Problem 7 -

  

Given 2 arrays of ints, a and b, return true if they have the same first element or they have the same last element. Both arrays will be length 1 or more.

Sample Solution:  
```
// Javascript
function common_end(array1, array2) {

	return array1[0] == array2[0] || array1[array1.length -1] == array2[array2.length -1];

}

// Test Cases:
console.log(common_end([1, 2, 3], [7, 3]));
// Expected Output: true
console.log(common_end([1, 2, 3], [7, 3, 2]));
// Expected Output: false
console.log(common_end([1, 2, 3], [1, 3]));
// Expected Output: true
```

#### Problem 8 -

Given an array of ints with a length of 3, return a new array with the elements in reverse order.

Sample Solution:
```
// Javascript
function reverse3(array) {

	return array.reverse();

}

// Test Cases
console.log(reverse3([1, 2, 3]));
// Expected Output: [3, 2, 1]
console.log(reverse3([5, 11, 9]));
// Expected Output: [9, 11, 5]
console.log(reverse3([7, 0, 0]));
// Expected Output: [0, 0, 7]
```
  

#### Problem 9 -
Given 2 int arrays, a and b, each length 3, return a new array length 2 containing their middle elements.

Sample Solution:
```
// Javascript
function middle_way(arr1, arr2) {

	return [arr1[1], arr2[1]];

}

// Test Cases:
console.log(middle_way([1, 2, 3], [4, 5, 6]));
// Expected Output: [2, 5]
console.log(middle_way([7, 7, 7], [3, 8, 0]));
// Expected Output: [7,8]
console.log(middle_way([5, 2, 9], [1, 4, 5]));
// Expected Output: [2, 4]
```

#### Problem 10 -

Given an array of ints, return true if the array is length 1 or more, and the first element and the last element are equal.

Sample Solution:
```
// Javascript
function same_first_last(arr) {

	return arr.length >= 1 && arr[0] == arr[arr.length -1];

}

// Test Cases:
console.log(same_first_last([1, 2, 3]));
// Expected Output: false
console.log(same_first_last([1, 2, 3, 1]));
// Expected Output: true
console.log(same_first_last([1, 2, 1]));
// Expected Output: true
```