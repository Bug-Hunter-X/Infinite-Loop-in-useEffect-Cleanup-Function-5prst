# React 18 useEffect Cleanup Function Bug

This repository demonstrates a subtle bug that can occur in React 18 and later versions related to the cleanup function within the `useEffect` hook.  Missing a `return` statement in the cleanup function can lead to an unexpected infinite render loop.

## Bug Description

The `bug.js` file contains a component with a `useEffect` hook. The cleanup function is intentionally missing a `return` statement, leading to a continuous re-rendering cycle. This behavior is more likely to occur when dealing with asynchronous operations or complex state updates.

## Solution

The `bugSolution.js` file provides a corrected version of the component.  The solution involves ensuring that the cleanup function always includes a `return` statement, even if it doesn't perform any specific cleanup actions.  This adheres to React 18's stricter rules for cleanup functions, preventing the infinite render loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite rendering in the console and the browser.
5. Switch to `bugSolution.js` to see the corrected version.