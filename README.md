# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common closure-related issue in JavaScript when using `setTimeout` within a loop.  The incorrect output occurs because the callback function within `setTimeout` doesn't capture the value of `i` at the time of its creation but rather references the variable `i` itself.  By the time the `setTimeout` functions execute, the loop has already completed, and `i` has its final value.

The `bug.js` file shows the buggy code, and `bugSolution.js` provides a corrected version using `let` or an immediately invoked function expression (IIFE).