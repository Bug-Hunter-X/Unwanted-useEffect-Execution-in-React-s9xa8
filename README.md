# Unwanted useEffect Execution in React

This repository demonstrates a common React bug: an `useEffect` hook that runs more often than intended.  The `useEffect` hook is designed to perform side effects after render, but without proper dependency management, it can lead to unexpected behavior and performance issues. This example showcases the issue and its resolution.

## Bug
The provided `MyComponent` uses a `useEffect` hook to log the current count to the console. However, the effect runs on every render, leading to excessive console logging. This is inefficient and can be indicative of a more serious issue in complex applications.

## Solution
The solution is to specify the correct dependencies in the `useEffect`'s second argument - the dependency array. By including only `count` in this array, the effect will only run when the `count` variable changes, avoiding unnecessary re-executions.