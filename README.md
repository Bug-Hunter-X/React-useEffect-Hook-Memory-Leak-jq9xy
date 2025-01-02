# React useEffect Hook Memory Leak

This repository demonstrates a common mistake when using the `useEffect` hook in React: forgetting to include a return statement for cleanup.  This can lead to memory leaks and unexpected behavior.

## The Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log a message when the component mounts. However, it is missing a return statement, which is crucial for cleaning up after the component unmounts.

## The Solution
The `bugSolution.js` file shows the corrected component.  A cleanup function is returned within the `useEffect` hook, ensuring that any side effects (in this simplified example, just the console log) are properly handled when the component unmounts.