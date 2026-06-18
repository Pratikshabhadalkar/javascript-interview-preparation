# Temporal Dead Zone (TDZ)

## What is TDZ?

The Temporal Dead Zone (TDZ) is the period between entering a scope and declaring a variable with let or const.

During this period, the variable exists but cannot be accessed.

## Example

```javascript
console.log(age);

let age = 25;
```

Output:

```javascript
ReferenceError
```

Reason:
The variable `age` is in the Temporal Dead Zone until its declaration is reached.

## Another Example

```javascript
{
    console.log(city);

    const city = "Pune";
}
```

Output:

```javascript
ReferenceError
```

Reason:
`city` is in the TDZ before its declaration.

## Key Points

- TDZ applies to let and const.
- TDZ does not apply to var.
- Accessing a variable in the TDZ results in a ReferenceError.

## Interview Summary

The Temporal Dead Zone is the time between entering a scope and declaring a let or const variable. Accessing the variable during this period throws a ReferenceError.
