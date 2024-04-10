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
```

### 2. Combining Arrays

Combine an array or add value to an array.

```javascript
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
```

### 3. Combining Objects

Combine Object or add value to Object.

```javascript
let obj1 = {name: "Sakshi", age: 24, title: 'Salesforce Developer'};
let obj2 = {name: "Shweta", age: 26, title: 'Salesforce Consultant', score: 87};
let obj3 = {...obj1, ...obj2}; // if want any extra properties from one of the objects then use this method
console.log(obj3); // {name: Shweta, age: 26, title: 'Salesforce Consultant', score: 87}

// Note: Extra properties of obj2 will be displayed because here obj2 is given priority.
```

### 4. Creating New Shallow Copy of Array and Objects
```javascript
var ar = ['A','G', 'M'];
ar.push('N'); // Use to add elements to the end of an array
console.log(ar); //['A', 'G', 'M', 'N']

var ar1 = ar; // Assigning ar to ar1
ar1.push('Vikas'); // Use to add elements to the end of an array
console.log(ar); // ['A', 'G', 'M', 'N', 'Vikas']
console.log(ar1); // ['A', 'G', 'M', 'N', 'Vikas']

/* Here we can see that both Objects & arrays work as a reference. So when we are updating a value
in the array (ar1) it automatically updates the value in the array (ar).
That's why array (ar) is printing Vikas and array (ar1) as well as printing Vikas.*/

/* So that's the problem with the push method, when we add a new element in one array it reflects in two arrays.
To avoid the above issue we can use the following*/

var ar = ['A','G', 'M'];
var ar1 = [...ar];
ar1.push('Vikas');
console.log(ar); // ['A', 'G', 'M']
console.log(ar1); // ['A', 'G', 'M',  'Vikas']

/* Note: Shallow copy only works at one level. For two level data structures, we can convert your object into the
Stringify format first (JSON.stringify(objar)) and then convert it again into an object using "json.parse"
JSON.parse(JSON.stringify(objar)) as mention below:*/

var objar = [         // Array with Objects
   {name: "Vikash"},
   {name: "Rahul"}
];
var objar1 = JSON.parse(JSON.stringify(objar));
objar1[0].name = 'Hero';
console.log(objar1); //Output {name: 'Hero'} {name: 'Rahul'}
console.log(objar); //Output {name: 'Vikash'} {name: 'Rahul'}

/*Please make sure to copy this Markdown content into your README.md file in your GitHub repository.
Let me know if you need any further assistance or modifications!*/
```
