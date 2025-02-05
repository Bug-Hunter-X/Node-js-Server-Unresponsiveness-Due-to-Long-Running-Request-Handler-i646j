# Node.js Server Unresponsiveness Bug

This repository demonstrates a common issue in Node.js where a long-running operation in a request handler can cause the server to become unresponsive.  The bug is caused by blocking the event loop, preventing other requests from being processed.

## Bug

The `server.js` file contains a simple HTTP server with a request handler that simulates a long-running task (a 5-second delay).  During this delay, the server will not respond to any other requests.

## Solution

The `serverSolution.js` file provides a solution using asynchronous operations (Promises or async/await) to prevent the event loop from being blocked. This allows the server to continue handling other requests while the long-running task completes in the background.