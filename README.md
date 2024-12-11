# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running operation in the request handler blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The server simulates a long-running operation (a 5-second CPU-bound loop). During this time, the event loop is blocked, preventing the server from handling new requests or responding to existing ones.  This leads to unresponsiveness and potentially a poor user experience.

## Solution

The solution involves using asynchronous operations (e.g., `setTimeout` or promises) to avoid blocking the event loop.  This allows the server to continue processing other requests while the long-running operation completes in the background.