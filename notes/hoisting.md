# Hoisting

## What is Hoisting?

Hoisting is JavaScript's behavior of moving declarations to the top of their scope before code execution.

## Example with var

```javascript
console.log(name);

var name = "Pratiksha";
```

Output:

```javascript
undefined
```

Reason:
`var` is hoisted and initialized with `undefined`.

## Example with let

```javascript
console.log(age);

let age = 25;
```

Output:

```javascript
ReferenceError
```

Reason:
`let` is hoisted but remains in the Temporal Dead Zone (TDZ).

## Example with const

```javascript
console.log(city);

const city = "Pune";
```

Output:

```javascript
ReferenceError
```

Reason:
`const` is hoisted but remains in the Temporal Dead Zone (TDZ).

## Interview Summary

- Hoisting moves declarations to the top of their scope.
- var is hoisted and initialized with undefined.
- let and const are hoisted but cannot be accessed before declaration due to the TDZ.
