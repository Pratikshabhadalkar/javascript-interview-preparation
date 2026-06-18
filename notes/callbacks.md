# Callbacks

## What is a Callback?

A callback is a function that is passed as an argument to another function and is executed after a specific task has been completed.

## Example 1

```javascript
function greet(callback) {
    console.log("Hello");
    callback();
}

function sayBye() {
    console.log("Bye");
}

greet(sayBye);
```

Output:

```javascript
Hello
Bye
```

Here, `sayBye` is the callback function because it is passed as an argument to `greet`.

## Example 2

```javascript
function completeTask(callback) {
    console.log("Task Completed");
    callback();
}

function notifyUser() {
    console.log("Notification Sent");
}

completeTask(notifyUser);
```

Output:

```javascript
Task Completed
Notification Sent
```

## Example 3

```javascript
function greetUser(name, callback) {
    console.log("Hello " + name);
    callback();
}

greetUser("Pratiksha", function() {
    console.log("Welcome!");
});
```

Output:

```javascript
Hello Pratiksha
Welcome!
```

## Real-World Example

```javascript
button.addEventListener("click", handleClick);
```

In this example, `handleClick` is a callback function that executes when the button is clicked.

## Why Callbacks Are Used

Callbacks allow JavaScript to execute code after a task has completed, especially in asynchronous operations such as:

- API calls
- Timers
- Event handling

## Interview Summary

A callback is a function passed as an argument to another function and executed later when a specific task is completed.
