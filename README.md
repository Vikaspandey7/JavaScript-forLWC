# Spread Operator in JavaScript

The spread operator in JavaScript is represented by three dots in a row (...) and it serves to unpack elements from arrays, objects, or iterable objects.

## Usages of Spread Operator

### 1. Expanding String

Convert string into a list of arrays.

```javascript
let greeting = "Hello";
let str = [...greeting];
console.log(str); // ['H', 'e', 'l', 'l', 'o']
console.log(str[2]); // l
console.log(str[4]); // o

### 2. Combining Arrays
Combine an array or add value to an array.

let arr1 = ['Apple', 'Google'];
let arr2 = ['Amazon', 'Microsoft'];
let result = [...arr1, ...arr2, ' '];
console.log(result); // ['Apple', 'Google', ' ', 'Amazon', 'Microsoft']

// Adding value to an array
let arr = ['A', 'G', 'M'];
let arrs = [...arr, 'Vikas'];
console.log(arrs); // ['A', 'G', 'M', 'Vikas']
let result = ['Shweta', ...arr, 'Vikas'];
console.log(result); // ['Shweta', 'A', 'G', 'M', 'Vikas']
