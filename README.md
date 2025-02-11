# Unhandled Request in Express.js Server

This repository demonstrates a common error in Express.js applications where the server receives requests but doesn't send back a response, leading to hanging requests and potential client-side errors.  The issue stems from omitting the `res.send()` or `res.json()` method within a route handler.

## Bug

The `bug.js` file contains an Express.js server with a route handler that logs a message upon receiving a request but doesn't send any data back to the client. This results in the client's request hanging indefinitely.

## Solution

The `bugSolution.js` file provides a corrected version of the server. The route handler now includes `res.send()` to send a simple 'Hello, world!' response, ensuring proper request handling and a complete HTTP response cycle.