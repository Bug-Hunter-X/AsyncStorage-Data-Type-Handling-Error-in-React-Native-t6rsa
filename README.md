# AsyncStorage Data Type Handling Error in React Native

This repository demonstrates a common error in React Native when using AsyncStorage to store and retrieve data of types other than strings.  AsyncStorage only supports storing strings, so attempting to store objects directly can lead to unexpected behavior and runtime errors if not handled correctly.

The `bug.js` file shows the problematic code, and `bugSolution.js` provides a corrected version that properly handles object serialization and deserialization using `JSON.stringify` and `JSON.parse`.

## Steps to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app (requires a React Native environment).
4. Observe the error in `bug.js` and the correct behavior in `bugSolution.js`.

## Solution

Always use `JSON.stringify()` to convert objects to strings before storing them in AsyncStorage, and `JSON.parse()` to convert the retrieved string back into a JavaScript object.