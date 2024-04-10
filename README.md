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
