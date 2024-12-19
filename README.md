# Node.js Server Hanging on Long Requests

This repository demonstrates a common issue in Node.js where the server hangs during long-running requests.  The problem stems from Node.js's single-threaded nature.  When a request initiates a long operation, it blocks the event loop, preventing the server from processing subsequent requests.

## Problem

The `server.js` file contains a simple HTTP server that simulates a long-running task (a 5-second delay).  During this delay, the server becomes unresponsive to new connections.

## Solution

The `serverSolution.js` file presents a solution that uses asynchronous operations to prevent blocking. It leverages asynchronous operations using the `setTimeout` function to simulate long-running processes without blocking the event loop.