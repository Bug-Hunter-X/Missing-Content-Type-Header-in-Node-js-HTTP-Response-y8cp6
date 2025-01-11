# Missing Content-Type Header in Node.js HTTP Response

This repository demonstrates a common, yet easily overlooked, error in Node.js HTTP servers: omitting the `Content-Type` header in the response.  This can lead to unexpected behavior in the browser, such as incorrect content rendering or errors.

## The Bug

The `bug.js` file contains a simple HTTP server that responds with 'Hello, world!' but fails to specify the `Content-Type` header.  Browsers rely on this header to determine how to interpret the response.

## The Solution

The `bugSolution.js` file corrects the issue by adding the `Content-Type` header to the response, specifying `text/plain` to indicate that the response body is plain text.

## How to Reproduce

1. Clone this repository.
2. Run `node bug.js`.
3. Open your browser and navigate to `http://localhost:3000`. Observe that the browser may not display the text correctly, or may even show an error.
4. Run `node bugSolution.js`.
5. Navigate to `http://localhost:3000` again. Observe that the text 'Hello, world!' is displayed correctly.