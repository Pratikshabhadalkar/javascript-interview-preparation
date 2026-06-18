# Event Loop

## What is the Event Loop?

The Event Loop is a mechanism that allows JavaScript to handle asynchronous operations even though JavaScript is single-threaded.

It continuously checks whether the Call Stack is empty and moves ready callbacks from the queue to the Call Stack for execution.

## Components of the Event Loop

### 1. Call Stack

The Call Stack keeps track of functions currently being executed.

### 2. Web APIs

The browser provides Web APIs for handling:

- setTimeout
- fetch API calls
- Event listeners

### 3. Callback Queue

Completed asynchronous tasks are placed in the Callback Queue.

### 4. Event Loop

The Event Loop checks whether the Call Stack is empty.

If it is empty, it moves callbacks from the queue to the Call Stack.

## Example

```javascript
console.log("Start");

setTimeout(() => {
    console.log("Timer");
}, 0);

console.log("End");
```

Output:

```javascript
Start
End
Timer
```

## How It Works

1. "Start" is pushed to the Call Stack and executed.
2. setTimeout is sent to Web APIs.
3. "End" is executed.
4. The timer callback enters the Callback Queue.
5. The Event Loop checks if the Call Stack is empty.
6. The callback is moved to the Call Stack.
7. "Timer" is printed.

## Interview Summary

JavaScript is single-threaded, but it can handle asynchronous operations using Web APIs, the Callback Queue, and the Event Loop. The Event Loop continuously checks whether the Call Stack is empty and moves ready callbacks to the Call Stack for execution.
