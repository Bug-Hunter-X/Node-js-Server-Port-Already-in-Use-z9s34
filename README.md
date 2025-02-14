# Node.js Server Port Already in Use

This repository demonstrates a common error encountered when developing Node.js applications: the failure to start a server because the specified port is already in use.  The provided solution includes error handling to gracefully manage this scenario.

## Problem

When you attempt to start a Node.js HTTP server on a port that's already occupied by another process (e.g., another server, or a different application using the same port), the server will fail to start. The error message isn't always explicit, making it difficult to diagnose the root cause.

## Solution

The solution involves adding error handling to the server's `listen()` method.  This allows the application to catch the `EADDRINUSE` error and handle it appropriately (e.g., log an informative message, attempt a different port, or exit gracefully).