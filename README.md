# Express.js - Missing Response in Request Handler

This repository demonstrates a common error in Express.js applications: forgetting to send a response in a request handler.  This results in the server seemingly hanging or not responding to requests, even though the server starts successfully.

## Bug

The `bug.js` file shows an Express.js server that receives a request but fails to send back a response using `res.send()`, `res.json()`, or a similar method.  The server logs a message indicating that it receives the request, but the client will experience a timeout.

## Solution

The `bugSolution.js` file corrects the issue by adding `res.send('Hello from Express!')` to the request handler.  This sends a simple response to the client, resolving the problem.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory containing `bug.js`.
3. Run `node bug.js`.
4. Try making a request to `http://localhost:3000/`. You'll likely see a timeout or no response.
5. Repeat steps 2-4 with `bugSolution.js` to see the corrected behavior.