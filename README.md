# Unhandled Exception in Async Callback Crashes Node.js Server

This repository demonstrates a common error in Node.js applications: unhandled exceptions within asynchronous callbacks causing the server to crash.  The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version using error handling.

## Problem

The `bug.js` server simulates an asynchronous operation. If a random number is greater than 0.5, an uncaught `Error` is thrown, abruptly terminating the server.

## Solution

The `bugSolution.js` file demonstrates proper error handling.  It uses a `try...catch` block within the asynchronous callback to gracefully handle potential errors, preventing the server from crashing.  This ensures the server remains responsive even during unexpected events.  Appropriate logging is also included to help diagnose issues.