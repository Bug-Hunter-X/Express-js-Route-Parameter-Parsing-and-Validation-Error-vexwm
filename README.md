# Express.js Route Parameter Parsing and Validation Error

This repository demonstrates a common error in Express.js applications where route parameters are not properly parsed and validated, leading to unexpected behavior or crashes.  The application attempts to access an array element using a string index instead of an integer, which may cause runtime errors or unexpected results.

## Bug Description

The `bug.js` file contains an Express.js route handler that retrieves a user from an array based on a route parameter (`id`).  The code lacks proper validation and type checking of the `id` parameter. This can lead to errors if the `id` is not a valid integer.

## Solution

The `bugSolution.js` file provides a solution by adding validation and type checking using `isNaN()` to ensure that the `id` parameter is a valid integer before attempting to access the user array. This prevents errors caused by invalid input.

## How to reproduce the bug

1. Clone the repository.
2. Run `npm install express` to install the Express.js package.
3. Run `node bug.js`.
4. Access the route with an invalid ID (e.g., `/users/abc`)

You will see that the original code crashes or behaves unexpectedly.

Running `node bugSolution.js` demonstrates the fix.