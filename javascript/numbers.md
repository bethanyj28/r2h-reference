# Numbers in JavaScript

## What's in a number?
In JavaScript, all numbers are 64 bit floating point. Let's break down what that means:

- 64-bit
This refers to the amount of data the variable can hold. The larger the number, the more space it takes up in the computer (this is due to the binary that it takes to represent the number). In JavaScript, the range of a number is -(2<sup>53</sup>-1) to (2<sup>53</sup>-1). You can access these numbers with `Number.MIN_VALUE` and `NUMBER.MAX_VALUE`

- floating point
This basically means that the number is a decimal. The reason it's such a big deal is because it's really complicated to express a number as a decimal to a computer, but you won't need to worry about that unless you really want to.

Because all numbers are floating point, these two values are the same:
```js
let num = 42;
let another_num = 42.0;
if num === another_num {
  console.log("it's the same thing") // this prints!
}
```

Also because numbers are floating point, they can only be accurate up to 15 digits:
```js
let x = 999999999999999;   // x will be 999999999999999
let y = 9999999999999999;  // y will be 10000000000000000
```

Additionally, floating point arithmetic is not always accurate:
```js
let x = 0.2 + 0.1;         // x will be 0.30000000000000004
```

## Using numbers
All arithmetic rules you learned in math also apply to numbers in JavaScript. This includes operations, orders of operations, and dividing by 0!

### Adding
Adding is as simple as:
```js
let a = 5;
let b = 10;
let c = a + b; // c is 15

let d = 5 + 15; // d is 20
```

One thing to be careful about is that `+` can mean different things depending on the *type* of the variables you're using. If you are using strings, then `+` is concatenation. For exampler:
```js
let a = 5;
let b = "10";
let c = a + b; // c is 510
```

### Subtracting
Similar to adding, subtraction is easy:
```js
let a = 5;
let b = 2;
let c = a - b; // c is 3
```

### Division
Division is not simple in all languages, but is relatively straightforward in JavaScript:
```js
let a = 10;
let b = 5;
let c = a / b; // c is 2
```

Just be careful about dividing by 0:
```js
let a = 100 / 0; // a is Infinity
let b = 100 / -0; // a is -Infinity
```

### Multiplication
Also pretty straightforward:
```js
let a = 10;
let b = a;
let c = a * b; // c is 100
```

### Modulo (AKA mod)
Mod might be something you haven't heard of before. It's kind of funny but ends up being very useful in certain situations! Essentially it divides two numbers and returns the remainder. For example:
```js
let a = 11;
let b = 5;
let c = a % b; // c is 1 because a / b = 2 remainder 1
```

## Incrementing numbers
You will learn later, but there are many times where you'll want to increment a number by a certain amount. Let's look at the example code below:
```js
let a = 0;
a = a + 10;
console.log(a); // 10
```
In this code, we incremented `a` by 10. This is fine and well, but there is a more common way that this is done using the **addition assignment** operator. This operator, `+=` makes it a little less verbose to increment a number. Using this operator, the above code turns into:
```js
let a = 0;
a += 10;
console.log(a); // 10
```
Which makes it a little easier to read.

Make sure that if you are trying to increment a number, the variable is of type number before using this operator! The `+=` operator means very different things for different data types (as we'll review later).

### Special case: incrementing by 1
Incrementing by 1 is _so common_ in JavaScript, that it has its own special syntax. It is called the **increment** operator, `++`. There are two ways to do this, **postfix** and **prefix**. 

#### Postfix increment
This will return the variable as is and then increment the variable. For example:
```js
let a = 1;
let b = a++;
console.log(a); // 2
console.log(b); // 1
```
Notice that `b` is 1, because it got assigned to the value of `a` _before_ `a` was incremented.

#### Prefix increment
This will increment the variable and then return it. For example:
```js
let a = 1;
let b = ++a;
console.log(a); // 2
console.log(b); // 2
```
Here you can see that `a` and `b` are both 2, because `a` was incremented before assigning to `b`.

### Decrementing?
All these principles also apply to subtraction. There is a **subtraction assignment** operator, `-=`, and a **decrement** operator, `--`.

## Comparing numbers
Comparing numbers is very important in programming. Let's say you were writing a program to determine if a person could buy a lotto ticket. You need to see if the person is older than 18. We can imagine something like this:
```js
let age = 16;
let lotto_age = 18;

if (age < lotto_age) {
  console.log("Sorry, too young!")
} else if (age >= lotto_age) {
  console.log("Here's your ticket!")
}
```
Notice the `<`, `>=` signs. They are as they seem, **less than** and **greater than or equal to**. There is also an equality operator, however we'll dive into that later.
