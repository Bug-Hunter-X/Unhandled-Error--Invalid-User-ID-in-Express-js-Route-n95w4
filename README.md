# Unhandled Error: Invalid User ID in Express.js Route

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input. Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for potential errors (e.g., non-numeric input). This can lead to crashes or unexpected behavior.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides a corrected version with robust error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install express` to install the necessary dependencies.
3. Run `node bug.js`.
4. Send a request to `/users/abc` (or similar invalid ID).  Observe the error.
5. Run `node bugSolution.js` and repeat step 4.  Notice the improved error handling.

## Solution

The solution involves adding checks to ensure the `userId` is a valid number before attempting to use it.  This prevents crashes and provides a more user-friendly response for incorrect input.