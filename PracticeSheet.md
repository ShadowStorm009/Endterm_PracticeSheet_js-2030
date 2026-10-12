# JavaScript Practice Sheet

Practice questions for:

- Class 12: Introduction to JavaScript (data types, variables, basic operations)
- Class 13: Arrays, Strings and Functions
- Class 14: Execution Context in JS with Hoisting

## How to use

1. Attempt Part A (MCQs) without running any code, then check the answer key at the end of Part A.
2. Solve Part B (coding questions) on your own, then open the solution under each question to compare.
3. Test every solution with at least two inputs, including one edge case.

Solutions use only loops, conditions and plain functions.

## Contents

- [Part A: MCQs](#part-a-mcqs)
  - [Section 1: Intro to JavaScript](#section-1-intro-to-javascript)
  - [Section 2: Arrays, Strings and Functions](#section-2-arrays-strings-and-functions)
  - [Section 3: Execution Context and Hoisting](#section-3-execution-context-and-hoisting)
  - [Answer key](#answer-key-for-part-a)
- [Part B: Coding Questions](#part-b-coding-questions)
  - [Section 1: Basics](#section-1-basics)
  - [Section 2: Arrays](#section-2-arrays)
  - [Section 3: Strings](#section-3-strings)
  - [Section 4: Functions](#section-4-functions)
  - [Section 5: Execution Context and Hoisting](#section-5-execution-context-and-hoisting)

---

## Part A: MCQs

### Section 1: Intro to JavaScript

**Q1.** What does `console.log(typeof null)` print?

- A) "null"
- B) "undefined"
- C) "object"
- D) "number"

**Q2.** Which statement about `const` is true?

- A) A `const` variable can be reassigned later
- B) A `const` variable must be given a value when declared
- C) A `const` variable is hoisted and initialised to undefined
- D) A `const` variable cannot be used inside functions

**Q3.** What is the output of `console.log("5" + 3)`?

- A) 8
- B) "53"
- C) NaN
- D) Error

**Q4.** What is the output of `console.log("5" - 3)`?

- A) 2
- B) "53"
- C) NaN
- D) "2"

**Q5.** What does `console.log(5 == "5")` followed by `console.log(5 === "5")` print?

- A) true, true
- B) false, false
- C) true, false
- D) false, true

**Q6.** Which of these values is falsy?

- A) "0"
- B) []
- C) {}
- D) 0

**Q7.** What is printed?

```js
let x;
console.log(x);
```

- A) null
- B) 0
- C) undefined
- D) ReferenceError

**Q8.** What is the value of `10 % 3`?

- A) 3
- B) 1
- C) 0
- D) 3.33

### Section 2: Arrays, Strings and Functions

**Q9.** What does `arr.push(4)` return when `arr = [1, 2, 3]`?

- A) The array `[1, 2, 3, 4]`
- B) 4 (the new length)
- C) undefined
- D) 3

**Q10.** What is `arr.length` after this code runs?

```js
let arr = [10, 20, 30];
arr[5] = 60;
```

- A) 4
- B) 5
- C) 6
- D) 3

**Q11.** Which array method does NOT modify the original array?

- A) splice
- B) push
- C) pop
- D) slice

**Q12.** What does `[1, 2, 3].indexOf(2)` return?

- A) 2
- B) 1
- C) -1
- D) undefined

**Q13.** What does `"hello".slice(1, 3)` return?

- A) "he"
- B) "hel"
- C) "el"
- D) "ell"

**Q14.** What is printed?

```js
let s = "abc";
s[0] = "z";
console.log(s);
```

- A) "zbc"
- B) "abc"
- C) Error
- D) undefined

**Q15.** What does a function return if it has no `return` statement?

- A) null
- B) 0
- C) undefined
- D) An empty string

**Q16.** What does `"a,b,c".split(",")` return?

- A) "abc"
- B) ["a,b,c"]
- C) ["a", "b", "c"]
- D) ["a", ",", "b", ",", "c"]

### Section 3: Execution Context and Hoisting

**Q17.** What is printed?

```js
console.log(a);
var a = 5;
```

- A) 5
- B) undefined
- C) ReferenceError
- D) null

**Q18.** What is printed?

```js
console.log(b);
let b = 5;
```

- A) 5
- B) undefined
- C) ReferenceError
- D) null

**Q19.** What is printed?

```js
foo();
function foo() {
  console.log("hi");
}
```

- A) hi
- B) undefined
- C) ReferenceError
- D) TypeError

**Q20.** What happens here?

```js
bar();
var bar = function () {
  console.log("hi");
};
```

- A) Prints hi
- B) ReferenceError: bar is not defined
- C) TypeError: bar is not a function
- D) Prints undefined

**Q21.** The JavaScript call stack follows which order?

- A) FIFO (first in, first out)
- B) LIFO (last in, first out)
- C) Random order
- D) Priority order

**Q22.** An execution context is created in which two phases?

- A) Parsing and compiling
- B) Memory creation and code execution
- C) Loading and unloading
- D) Declaration and deletion

**Q23.** What is printed?

```js
var x = 1;
function f() {
  console.log(x);
  var x = 2;
}
f();
```

- A) 1
- B) 2
- C) undefined
- D) ReferenceError

**Q24.** Function `a` calls `b`, and `b` calls `c`. Which function finishes and leaves the call stack first?

- A) a
- B) b
- C) c
- D) All at once

### Answer key for Part A

<details>
<summary>Show answers</summary>

| Q | Answer | Why |
| --- | --- | --- |
| 1 | C | `typeof null` is "object", a long-standing quirk of the language. |
| 2 | B | `const` must be initialised at declaration and cannot be reassigned. |
| 3 | B | With `+`, a string operand turns the operation into concatenation, giving "53". |
| 4 | A | `-` forces numeric conversion, so the result is the number 2. |
| 5 | C | `==` converts types (true), `===` does not (false). |
| 6 | D | 0 is falsy. The string "0", an empty array and an empty object are all truthy. |
| 7 | C | A declared but unassigned variable holds undefined. |
| 8 | B | `%` gives the remainder, which is 1. |
| 9 | B | `push` returns the new length of the array. |
| 10 | C | Assigning to index 5 makes the length 6, leaving empty slots at indexes 3 and 4. |
| 11 | D | `slice` returns a copy. `splice`, `push` and `pop` mutate the array. |
| 12 | B | `indexOf` returns the position of the first match, and 2 sits at index 1. |
| 13 | C | `slice(1, 3)` starts at index 1 and stops before index 3, giving "el". |
| 14 | B | Strings are immutable, so the assignment silently does nothing in non-strict mode. |
| 15 | C | A function without `return` gives back undefined. |
| 16 | C | `split(",")` breaks the string at each comma. |
| 17 | B | `var` is hoisted and initialised to undefined. |
| 18 | C | `let` is hoisted but sits in the temporal dead zone until its declaration line runs. |
| 19 | A | Function declarations are hoisted along with their body. |
| 20 | C | `bar` is hoisted as a `var` with value undefined, so calling it gives a TypeError. |
| 21 | B | The call stack is last in, first out. |
| 22 | B | Each execution context has a memory creation phase and then a code execution phase. |
| 23 | C | The local `var x` is hoisted inside `f` as undefined and shadows the global `x`. |
| 24 | C | The most recently called function, `c`, finishes first and is popped first. |

</details>

---

## Part B: Coding Questions

Tip: write each solution yourself first, then test with at least two inputs, including one edge case.

### Section 1: Basics

**C1. Variables and types.** Declare one variable of each type: number, string, boolean, undefined, null. Print each value along with its `typeof` result. Note which result surprises you.

<details>
<summary>Show solution</summary>

```js
let age = 21;
let name = "R";
let isStudent = true;
let city;
let nothing = null;

console.log(age, typeof age);             // 21 number
console.log(name, typeof name);           // R string
console.log(isStudent, typeof isStudent); // true boolean
console.log(city, typeof city);           // undefined undefined
console.log(nothing, typeof nothing);     // null object
```

The surprise is `typeof null`, which gives "object".

</details>

**C2. Even or odd.** Take a number and print whether it is even or odd using the `%` operator.

- Input: 7, Output: `7 is odd`

<details>
<summary>Show solution</summary>

```js
let n = 7;
if (n % 2 === 0) {
  console.log(n + " is even");
} else {
  console.log(n + " is odd");
}
```

</details>

**C3. Temperature converter.** Convert a Celsius value to Fahrenheit using F = C x 9/5 + 32. Print the result using a template literal.

- Input: 100, Output: `100C is 212F`

<details>
<summary>Show solution</summary>

```js
let c = 100;
let f = c * 9 / 5 + 32;
console.log(`${c}C is ${f}F`); // 100C is 212F
```

</details>

**C4. Swap two variables.** Swap the values of `a` and `b`. Do it once with a temporary variable, then once with array destructuring.

<details>
<summary>Show solution</summary>

```js
// With a temporary variable
let a = 1;
let b = 2;
let temp = a;
a = b;
b = temp;
console.log(a, b); // 2 1

// With array destructuring
let x = 1;
let y = 2;
[x, y] = [y, x];
console.log(x, y); // 2 1
```

</details>

**C5. Coercion check.** Predict, then verify, the output of `"10" + 5`, `"10" - 5`, `"10" * "2"`, `true + 1`, and `Number("abc")`. Write one line explaining each result.

<details>
<summary>Show solution</summary>

```js
console.log("10" + 5);        // "105"
console.log("10" - 5);        // 5
console.log("10" * "2");      // 20
console.log(true + 1);        // 2
console.log(Number("abc"));   // NaN
```

- `+` with a string joins text, so 5 becomes "5".
- `-` and `*` only work on numbers, so the strings are converted.
- `true` becomes 1 in arithmetic.
- "abc" cannot be converted to a number, so the result is NaN.

</details>

### Section 2: Arrays

**C6. Sum and average.** Given an array of numbers, print the sum and the average.

- Input: [10, 20, 30, 40], Output: sum 100, average 25

<details>
<summary>Show solution</summary>

```js
let nums = [10, 20, 30, 40];
let sum = 0;
for (let i = 0; i < nums.length; i++) {
  sum += nums[i];
}
let average = sum / nums.length;
console.log(sum, average); // 100 25
```

</details>

**C7. Largest and smallest.** Find the largest and smallest values in an array without using `Math.max` or `Math.min`.

<details>
<summary>Show solution</summary>

```js
let arr = [4, 9, 1, 7];
let largest = arr[0];
let smallest = arr[0];
for (let i = 1; i < arr.length; i++) {
  if (arr[i] > largest) largest = arr[i];
  if (arr[i] < smallest) smallest = arr[i];
}
console.log(largest, smallest); // 9 1
```

</details>

**C8. Reverse an array.** Reverse an array without using the built-in `reverse()`. Do not modify the original array.

<details>
<summary>Show solution</summary>

```js
let arr = [1, 2, 3, 4];
let reversed = [];
for (let i = arr.length - 1; i >= 0; i--) {
  reversed.push(arr[i]);
}
console.log(reversed); // [4, 3, 2, 1]
console.log(arr);      // [1, 2, 3, 4] (unchanged)
```

</details>

**C9. Remove duplicates.** Given [1, 2, 2, 3, 4, 4, 5], produce [1, 2, 3, 4, 5].

<details>
<summary>Show solution</summary>

```js
let arr = [1, 2, 2, 3, 4, 4, 5];
let unique = [];
for (let i = 0; i < arr.length; i++) {
  if (!unique.includes(arr[i])) {
    unique.push(arr[i]);
  }
}
console.log(unique); // [1, 2, 3, 4, 5]
```

</details>

**C10. Loop and build.** From [1, 2, 3, 4, 5, 6], build a new array containing the squares of only the even numbers, using a `for` loop and `push`.

- Output: [4, 16, 36]

<details>
<summary>Show solution</summary>

```js
let nums = [1, 2, 3, 4, 5, 6];
let result = [];
for (let i = 0; i < nums.length; i++) {
  if (nums[i] % 2 === 0) {
    result.push(nums[i] * nums[i]);
  }
}
console.log(result); // [4, 16, 36]
```

</details>

**C11. Second largest.** Find the second largest number in an array of distinct numbers.

<details>
<summary>Show solution</summary>

```js
let arr = [12, 35, 1, 10, 34];
let first = -Infinity;
let second = -Infinity;
for (let i = 0; i < arr.length; i++) {
  if (arr[i] > first) {
    second = first;
    first = arr[i];
  } else if (arr[i] > second) {
    second = arr[i];
  }
}
console.log(second); // 34
```

</details>

### Section 3: Strings

**C12. Reverse a string.** Reverse a given string.

- Input: "hello", Output: "olleh"

<details>
<summary>Show solution</summary>

```js
let str = "hello";
let reversed = "";
for (let i = str.length - 1; i >= 0; i--) {
  reversed += str[i];
}
console.log(reversed); // olleh
```

</details>

**C13. Palindrome check.** Check whether a string is a palindrome, ignoring letter case.

- Input: "Madam", Output: true

<details>
<summary>Show solution</summary>

```js
function isPalindrome(s) {
  let lower = s.toLowerCase();
  let rev = "";
  for (let i = lower.length - 1; i >= 0; i--) {
    rev += lower[i];
  }
  return lower === rev;
}
console.log(isPalindrome("Madam")); // true
```

</details>

**C14. Count vowels.** Count the vowels in a string.

- Input: "JavaScript", Output: 3

<details>
<summary>Show solution</summary>

```js
let str = "JavaScript";
let lower = str.toLowerCase();
let vowels = "aeiou";
let count = 0;
for (let i = 0; i < lower.length; i++) {
  if (vowels.includes(lower[i])) {
    count++;
  }
}
console.log(count); // 3
```

</details>

**C15. Capitalise each word.** Capitalise the first letter of every word in a sentence.

- Input: "learning javascript is fun", Output: "Learning Javascript Is Fun"

<details>
<summary>Show solution</summary>

```js
let sentence = "learning javascript is fun";
let words = sentence.split(" ");
let result = "";
for (let i = 0; i < words.length; i++) {
  let word = words[i];
  result += word[0].toUpperCase() + word.slice(1);
  if (i < words.length - 1) {
    result += " ";
  }
}
console.log(result); // Learning Javascript Is Fun
```

</details>

**C16. Character frequency.** Count how many times each character appears in a string and print the result.

- Input: "banana", Output: a: 3, b: 1, n: 2

<details>
<summary>Show solution</summary>

```js
let str = "banana";
let freq = {};
for (let i = 0; i < str.length; i++) {
  let ch = str[i];
  if (freq[ch]) {
    freq[ch]++;
  } else {
    freq[ch] = 1;
  }
}
console.log(freq); // { b: 1, a: 3, n: 2 }
```

This uses a plain object as a tally. If objects are not covered yet in class, treat this as a stretch question.

</details>

### Section 4: Functions

**C17. Two ways to write a function.** Write an `add(a, b)` function as a function declaration and as a function expression. Call both.

<details>
<summary>Show solution</summary>

```js
function add(a, b) {
  return a + b;
}

const addExpr = function (a, b) {
  return a + b;
};

console.log(add(2, 3));     // 5
console.log(addExpr(2, 3)); // 5
```

</details>

**C18. Prime check.** Write a function `isPrime(n)` that returns true or false.

- Input: 7, Output: true. Input: 12, Output: false

<details>
<summary>Show solution</summary>

```js
function isPrime(n) {
  if (n < 2) return false;
  for (let i = 2; i * i <= n; i++) {
    if (n % i === 0) return false;
  }
  return true;
}
console.log(isPrime(7));  // true
console.log(isPrime(12)); // false
```

</details>

**C19. Factorial.** Write a function `factorial(n)`. Do it once with a loop and once with recursion.

- Input: 5, Output: 120

<details>
<summary>Show solution</summary>

```js
// Loop
function factorialLoop(n) {
  let result = 1;
  for (let i = 2; i <= n; i++) {
    result *= i;
  }
  return result;
}

// Recursion
function factorialRec(n) {
  if (n <= 1) return 1;
  return n * factorialRec(n - 1);
}

console.log(factorialLoop(5)); // 120
console.log(factorialRec(5));  // 120
```

</details>

**C20. Default parameters.** Write `greet(name)` that prints `Hello, Guest` when no name is passed, and `Hello, <name>` otherwise.

<details>
<summary>Show solution</summary>

```js
function greet(name = "Guest") {
  console.log("Hello, " + name);
}
greet();     // Hello, Guest
greet("R");  // Hello, R
```

</details>

**C21. One function calling another.** Write `square(n)` that returns n times n. Then write `sumOfSquares(a, b)` that calls `square` to return a squared plus b squared.

- Example: `sumOfSquares(3, 4)` gives 25

<details>
<summary>Show solution</summary>

```js
function square(n) {
  return n * n;
}

function sumOfSquares(a, b) {
  return square(a) + square(b);
}

console.log(sumOfSquares(3, 4)); // 25
```

</details>

### Section 5: Execution Context and Hoisting

For each snippet below, write the output first, then run it. Then write two lines explaining what happened in the memory creation phase and the code execution phase.

**C22.**

```js
console.log(a);
var a = 10;
console.log(a);
```

<details>
<summary>Show solution</summary>

Output: `undefined`, then `10`.

- Memory creation phase: `a` is created and set to undefined.
- Code execution phase: the first log prints undefined, then `a` becomes 10, and the second log prints 10.

</details>

**C23.**

```js
greet();
function greet() {
  console.log("Hello");
}
```

<details>
<summary>Show solution</summary>

Output: `Hello`.

- Memory creation phase: the whole function `greet` is stored in memory, body included.
- Code execution phase: the call on line 1 works because the function already exists.

</details>

**C24.**

```js
var x = 1;
function outer() {
  console.log(x);
  var x = 2;
  function inner() {
    console.log(x);
  }
  inner();
}
outer();
console.log(x);
```

<details>
<summary>Show solution</summary>

Output: `undefined`, then `2`, then `1`.

- Inside `outer`, the local `var x` is hoisted and set to undefined, so the first log prints undefined and does not see the global `x`.
- After `x = 2` runs, `inner` looks up `x`, finds the one in `outer`, and prints 2.
- The last log is outside any function, so it prints the global value 1.

</details>

**C25. Fix the bug.** The code below throws an error. Explain why, then fix it in two different ways.

```js
console.log(total);
let total = 50;
```

<details>
<summary>Show solution</summary>

Why it fails: `let total` is hoisted but sits in the temporal dead zone until its declaration line runs, so reading it earlier throws a ReferenceError.

Fix 1: move the log below the declaration.

```js
let total = 50;
console.log(total); // 50
```

Fix 2: declare first, log, then assign (prints undefined, with no error).

```js
let total;
console.log(total); // undefined
total = 50;
```

</details>

**C26. Call stack trace.** For the code below, write the order in which functions are pushed onto and popped off the call stack, and the final printed output.

```js
function one() {
  console.log("one start");
  two();
  console.log("one end");
}
function two() {
  console.log("two start");
  three();
  console.log("two end");
}
function three() {
  console.log("three");
}
one();
```

<details>
<summary>Show solution</summary>

- Printed output, in order: `one start`, `two start`, `three`, `two end`, `one end`.
- Stack, from the global context at the bottom: push `one`, push `two`, push `three`, pop `three`, pop `two`, pop `one`.
- `three` finishes first because the stack is last in, first out.

</details>

**C27. Write your own.** Create one snippet that shows `var` hoisting, one that shows the temporal dead zone with `let`, and one that shows a function expression failing when called early. Explain each in one sentence.

<details>
<summary>Show solution</summary>

```js
// var hoisting
console.log(v); // undefined
var v = 1;

// temporal dead zone with let
console.log(l); // ReferenceError
let l = 1;

// function expression called early
sayHi(); // TypeError: sayHi is not a function
var sayHi = function () {
  console.log("hi");
};
```

- `var v` is hoisted and set to undefined, so reading it early gives undefined.
- `let l` is hoisted but locked until its declaration line, so reading it early throws.
- `sayHi` is hoisted as a `var` holding undefined, and calling undefined is a TypeError.

Note: run these one at a time, since the ReferenceError and TypeError stop the script.

</details>