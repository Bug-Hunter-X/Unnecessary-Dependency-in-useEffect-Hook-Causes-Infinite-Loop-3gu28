# Unnecessary Dependency in useEffect Hook Causes Infinite Loop

This example demonstrates a common issue in React applications where an unnecessary dependency in the useEffect hook leads to an infinite loop. 
The `useEffect` hook with no dependencies (empty array `[]`) runs only once after the initial render. Adding a dependency (in this case `count`) causes the effect to run whenever the dependency changes. In this example it causes infinite rerenders.

## How to Reproduce

1.  Clone this repository.
2.  Run `npm install` to install the necessary dependencies.
3.  Run `npm start` to start the development server.
4. Observe the infinite loop in the browser console.

## Solution

The solution involves correctly specifying the dependencies for the `useEffect` hook.  Only include variables that, when changed, should trigger the effect. In this case, only `count` is needed.