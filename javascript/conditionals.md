# Conditionals

While coding, there will be times when you want to perform an action, but only if a certain condition is met. To do this, you need to use **conditionals**.
Conditionals allow you to compare values and execute code if the condition evaluates to **true**.

## `if` statement
An `if` statement lets you check a value and execute code if it evaluates to true. For example:

```js
function isOldEnoughToDrive(age) {
  if (age >= 16) {
    return true;
  }
  
  return false;
}
```

## `else if` statement
Sometimes you need to check multiple conditions within your code. This is where the `else if` statement comes into play. Let's pretend in our next example that 
anyone over the age of 80 isn't allowed to drive.

```js
function canDrive(age) {
  if (age < 16) {
    return false;
  } else if (age > 80) {
    return false;
  }
  
  return true;
}
```

## `else` statement
`else` acts like a default selection if the `if` condition wasn't met. For example:

```js
function canDrive(age) {
  let isOfAge;
  if (age < 16) {
    isOfAge = false;
  } else {
    isOfAge = true;
  }
  
  return isOfAge;
}
```

This also works with `else if` statements:
```js
function canDrive(age) {
  let isOfAge;
  if (age < 16) {
    isOfAge = false;
  } else if (age > 80) {
    isOfAge = false;
  } else {
    isOfAge = true;
  }
  
  return isOfAge;
}
```

## If, ands, or ors
In conditionals, you can use `&&` (and) and `||` (or) to chain expressions. This is helpful so you don't have massive blocks of code with `if`/`else if`s. For example:

```js
function canDrive(age) {
  let isOfAge;
  if (age < 16) || (age > 80) { // if age is less than 16 or greater than 80
    isOfAge = false;
  } else {
    isOfAge = true;
  }
  
  return isOfAge;
}
```

## `==` vs. `===`
You'll often see either two equals or three equals and they both mean similar but different things. `==` is
