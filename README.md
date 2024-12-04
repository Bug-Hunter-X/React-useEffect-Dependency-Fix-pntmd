# React Infinite Rendering Bug

This repository demonstrates a common React bug involving infinite rendering caused by an improperly used `useEffect` hook.  The `useEffect` hook, without a proper dependency array, causes the component to re-render endlessly, resulting in a browser crash.  The solution showcases the correct usage of dependency arrays to avoid this issue.

## Bug
The `bug.js` file contains a React component that increments a counter on button click. However, due to the absence of a dependency array in the `useEffect` hook, the component re-renders infinitely, triggering the console log repeatedly and eventually crashing the browser. 

## Solution
The `bugSolution.js` file provides a corrected version of the component. The `useEffect` hook now includes `[count]` as the dependency array, ensuring that the effect only runs when the value of `count` changes. This prevents the infinite rendering loop.

## How to Reproduce
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the infinite rendering in the browser console and the eventual browser crash (for the buggy version).
6. Compare the behavior with the fixed version in `bugSolution.js`.
