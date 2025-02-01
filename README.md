# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js applications: blocking the event loop with a long-running synchronous operation, leading to an unresponsive server.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Bug
The server in `bug.js` performs a 5-second CPU-bound task synchronously within the request handler. This prevents the event loop from processing other requests, resulting in an unresponsive server during this period.

## Solution
The `bugSolution.js` file demonstrates how to refactor the code to use asynchronous operations. This allows the event loop to continue processing other requests while the long-running task is performed in the background.