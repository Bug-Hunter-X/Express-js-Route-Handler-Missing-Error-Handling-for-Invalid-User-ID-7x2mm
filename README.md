# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking if it's actually a number.  This can lead to unexpected crashes or errors.

## Bug

The `bug.js` file contains the flawed code.  It attempts to find a user based on the provided ID, but it doesn't handle the case where the ID is not a valid integer.  This can cause a runtime error if a non-numeric ID is passed.

## Solution

The `bugSolution.js` file provides the corrected code. It includes checks to ensure that the `userId` is a number before attempting to use it.  Error handling is added to gracefully handle the case where a user is not found or the ID is invalid.