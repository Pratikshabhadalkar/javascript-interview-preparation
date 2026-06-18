# Synchronous vs Asynchronous Programming

## Synchronous Programming

Synchronous code executes one task at a time.

Each task must complete before the next task starts.

### Example

```javascript
console.log("Start");
console.log("Middle");
console.log("End");
```

Output:

```javascript
Start
Middle
End
```

## Asynchronous Programming

Asynchronous programming allows long-running operations to be handled without blocking the main thread.

Examples:
- API calls
- Timers
- Promises
- Event handlers

### Example

```javascript
console.log("Start");

setTimeout(() => {
    console.log("Timer");
}, 1000);

console.log("End");
```

Output:

```javascript
Start
End
Timer
```

## Why Do We Need Asynchronous Programming?

JavaScript is single-threaded.

Without asynchronous programming, operations such as API calls and timers would block the application and make it unresponsive.

## Interview Summary

- Synchronous code executes line by line.
- Asynchronous code handles time-consuming tasks without blocking the main thread.
- JavaScript uses asynchronous programming to keep applications responsive.
