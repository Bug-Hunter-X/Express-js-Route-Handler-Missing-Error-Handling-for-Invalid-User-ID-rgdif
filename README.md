# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code attempts to parse a user ID as an integer without validating whether the input is actually a number. This can lead to unexpected behavior or crashes.

## Bug

The `bug.js` file contains the faulty code.  It fetches a user based on their ID from a `users` array.  However, if the `id` parameter is not a valid integer, `parseInt(userId)` will return `NaN`, leading to potential errors.  There's no handling for the case where a user with the given ID is not found.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes input validation and explicit error handling for when the ID is invalid or the user is not found.  The improved version handles potential errors gracefully and provides appropriate responses.