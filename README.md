# Unexpected Output in setTimeout Loop

This repository demonstrates a common JavaScript closure problem encountered when using `setTimeout` within a loop.  The expected behavior is to log numbers from 0 to 9, with a one-second delay between each.  However, due to how closures work in JavaScript, the loop completes before the `setTimeout` callbacks execute, and all callbacks will use the final value of `i` (which is 10). 

The `bug.js` file contains the code exhibiting the issue.  The `bugSolution.js` file provides a corrected version using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, thus preserving the correct value of `i`.