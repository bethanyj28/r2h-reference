# Variable Types in JavaScript

JavaScript is known as a **weakly typed** language. This means that you do not need to declare the **type** of a variable, like `num`, `string`, or `boolean`.
Though you don't need to declare a type, it is still important to be aware of the various types to avoid unexpected errors. Since we reviewed numbers in a separate
file, we'll focus on other types.

## Boolean
A boolean value can only have one of two values: `true` and `false`. This is a really useful type that doesn't take up a lot of space since it can only be two values.
It is often used for comparison of two values.

### Examples
```js
let num1 = 100;
let num2 = 0;

console.log(num1 < num2); // false -> 100 is not less than 0
console.log(num1 >= num2); // true -> 100 is greater or equal to 0
console.log(num1 == num2); // false -> 100 is not equal to 0
```

## String
A **string** is simply a representation of words and characters. Strings behave like arrays in many languages, including JavaScript. There are several default methods
that can be used with Strings, which you can reference [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String). Strings can also be compared.
To declare strings, the value must be wrapped with `"var"`, `` `var` ``, or `'var'`.

### Examples
```js
let str = "cat";
console.log(str.charAt(1)); // a
console.log(str[1]); // a
console.log(str.toUpperCase()); // CAT
```

```js
let str1 = "cat";
let str2 = "bat";

console.log(str1 == str2); // false
console.log(str1 > str2); // true (b comes before c in the alphabet)
console.log(str1 + " and " + str2); // cat and bat
```

## Practice problems
What will the following print out?
```js
let str1 = "dog";
let str2 = "bog";

console.log(str1.charAt(2));
console.log(str2.toUpperCase());
console.log(str1 == str2);
console.log(str2 < str1);
```
