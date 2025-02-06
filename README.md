# Unhandled Promise Rejection in Express.js Asynchronous Route Handler

This repository demonstrates a common error in Express.js applications: neglecting to properly handle errors within asynchronous route handlers.  Failing to handle such errors can lead to unhandled promise rejections, causing the server to crash or silently fail without providing informative error messages.

## Problem

The `bug.js` file showcases an Express.js route handler that performs an asynchronous operation. However, it only catches errors within the `.catch()` block.  This only logs the error to the console, failing to send an appropriate response to the client or handle the error gracefully.

## Solution

The `bugSolution.js` file demonstrates the correct approach.  It properly handles errors by sending an error response to the client, providing information about the failure without crashing the application.  This ensures a more robust and user-friendly application.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install express` to install Express.js.
4. Run `node bug.js` and observe the behavior.  Note that if an error occurs, it might only be logged to the console without proper application-level handling.
5. Then run `node bugSolution.js` and see the improved error handling.