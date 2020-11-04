# Declaring Variables

In JavaScript, there are three ways to initialize variables: using `var`, `let`, and `const`.

## var

The *var* statement declares a function-scoped or globally-scoped variable, optionally initializing it to a value. There really is no reason to use `var` anymore and should instead use `let` or `const`, since those are more specific.

### Example
```
var x = 1;

if (x === 1) {
  var x = 2;

  console.log(x); // expected output: 2
}

console.log(x); // expected output: 2
```

## let
The *let* statement initializes a variable within the scope that can be changed or updated.

### Example
```
let x = 1;

if (x === 1) {
  let x = 2;

  console.log(x); // expected output: 2
}

console.log(x); // expected output: 1
```

## const
The *const* statement initializes a variable within the scope that cannot be reassigned or redeclared.

### Example
```
const number = 42;

console.log(number); // expected output: 42
number = 99; // expected output: TypeError: invalid assignment to const `number'
```

## Declaring vs. Initializing vs. Assigning
These three phrases are often used interchangeably since the differences between them are very small. However, it is worth talking about the differences!

### Declaring
*Declaring* a variable happens when you type out `let var1` or `const var2` or even `var var3`. This lets the computer know that you want to utilize this name to reference a value of some type within a particular scope. There are two ways to declare a variable:

```
let myVar1; // declares myVar1 and initializes it to Undefined
let myVar2 = 5; // declares myVar2 and initializes it to 5
```

We'll get to what initializing means..... now!

### Initializing
*Initializing* a variable is when the variable is created and given a value. As shown in the example above, you can give a value to a variable when you declare it _or_ you can let the interpreter (the tool that translates your code into binary) assign the value to `Undefined`.

### Assigning
*Assigning* a variable is when you give it a value. This can happen when you declare it (AKA initialization) or anytime you use the `=` after declaring it. Like so:
```
let myVar1 = 42; // declares and assigns myVar1 to the value 42 (this is the same thing as initializing)

myVar1 = 43; // reassigns the variable myVar1 to 43
```

## Checking for understanding

1. What is the difference between `let` and `const`?
2. What will print in the following block of code?
```
let x = 50;

x = 43;

console.log(answer) // what does this print?
```
3. What will happen in the following block of code?
```
const answer = 42;

answer = 42 * 100;
```
4. Choose the right words in the following sentence for what is happening in this block of code.
```
let myVar = 999;
myVar = 1000;
```
`myVar` is (declared/initialized/assigned). It is then (declared/initialized) to the value of 999. Finally, it is (declared/initialized/assigned) the value of 1000.
