# React useEffect Cleanup Function Memory Leak

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a return function for cleanup when dealing with side effects like event listeners or subscriptions.

## The Bug
The `bug.js` file contains a component with a `useEffect` hook that logs a message to the console when the component mounts.  However, it's missing a return function to perform cleanup. This can result in memory leaks if the component unmounts before the side effect is properly cleaned up.

## The Solution
The `bugSolution.js` file provides the corrected version.  A return function is added to the `useEffect` hook. This function is responsible for removing any listeners or subscriptions to prevent memory leaks.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior when mounting and unmounting the component. The bug version shows the absence of cleanup, whereas the solution will demonstrate proper cleanup.