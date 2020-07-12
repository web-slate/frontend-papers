### 1. Arity  
  1. Method returns number of arguments of function. Alternative is argument.length.
### 2. Anonymous
  1. Unnamed Function means Function cannot identified by its Name.
IIFE - Immediately Invoked Function Expression. Define and call Function.
### 3. Closure
  1. Inner Function. They are like Waiter in Restaurant
  1. Closures are like Waiters. Inside Restaurant may be many activity happens in Restaurant but we order and get meal from Waiters.
### 4. Currying / Function Currying
  1. Named after Haskell Curry. Using Multiple Functions with Single Arguments instead multiple arguments in Single Function.

  ```
    function add(a) {
      function addX(y) {
        return x + y;
      }

      return addX;
    }

    const add7 = add(7);
    console.log(add7(7)); // 14
    console.log(add7(3)); // 10
  ```

  ```
    connect(mapStatesToProps, mapDispatchToProps)(Component);
  ```

### 5. Strict Mode
Closure
Variable Hoisting
    Its a mechanism where variable declaration using var are hoisted/lifted to top of their scope.

Reduce Function
    Single to Multi Dimensional Array

### 6. setTimeout with For...loop
Due to Closure, below i will be closure when callback is called.

#### Issue
```
const count = [1, 2, 3, 4, 5];

for(var i=0;i < count.length; i++) {
  setTimeout(() => {
    console.log(count[i]);
  }, 1000);
}
```

#### Solution - Use `let` instead of var because let creates a separate scope of code block.
```
const count = [1, 2, 3, 4, 5];

for(let i=0;i < count.length; i++) {
  setTimeout(() => {
    console.log(count[i]);
  }, 1000);
}
```

#### Solution with var - Create separate Method `delay`.
```
const count = [1, 2, 3, 4, 5];

for(var i=0;i < count.length; i++) {
  delay(i)
}

function delay(i) {
  setTimeout(() => {
    console.log(count[i]);
  }, 1000);
}
```

#### Solution with var - Create anonymous Method.
```
const count = [1, 2, 3, 4, 5];

for(var i=0;i < count.length; i++) {
  (function (n) {
    setTimeout(() => {
      console.log(count[n]);
    }, 1000 * n);
  }(i));
}
```

### 7. Microtasks Queue
  1. (FIFO) Internal Queue of PromiseJOBS often referred as Microtask Queue.
  1. When promise ready, then/catch/finally handlers are put into queue.
  1. Promise handlers (then/catch/finally) always goes in to internal queue.
  1. Concept of microtasks closely tied with the eventloop and microtasks

#### In Below code, `end` will be executed first then `async end` will executed.
```
let promise = Promise.resolve();

promise.then(() => alert('async end'));

alert('end');
```

### 8. Promise Unhandled Rejection
This occurs when a promise error is not handled at the end of the Microtask.

```
 window.eventEventListener('unhandledrejection', event => alert(event.reason));
```

### 9. Event Loop
Browser and NodeJS execution flow is based on Event Loop.
Below is the Algorithm
  1. Execute Task when oldest Task queue to New.
  1. Sleep Until Task appears and wait for more task.
  1. Task enqueued when a new Task added.

### setImmediate vs setNextTick vs setTimeout
Basically all execute the callback after current event loop.

### Mutation - Its a side effect.
  1. Make code unpredictable.
  1. Harder to test
  1. Break time-travel debugging.
  1. Persistent, Immutable, Data Structures.

### Immutability.js Use
  Provides persistent immutable data structures.
  1. List
  1. Map
  1. Stack
  1. Ordered Map
  1. Set
  1. Ordered Set
  1. Record
