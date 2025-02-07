# Express.js JSON Body Parsing Issue

This repository demonstrates a common issue encountered when working with JSON request bodies in Express.js applications.  The problem arises when the client omits or provides an incorrect `Content-Type` header in the request.  This leads to `req.body` remaining empty, causing unexpected behavior in the server.

## Bug Description

The provided Express.js application attempts to parse a JSON request body using `express.json()`. However, if the client doesn't set the `Content-Type` header correctly (to `application/json`), the middleware fails to parse the request body, resulting in an empty `req.body` object.

## Solution

The solution involves explicitly setting the `Content-Type` header in the client's request. Alternatively, robust error handling can be implemented on the server to gracefully handle missing or invalid headers and respond with appropriate error messages.