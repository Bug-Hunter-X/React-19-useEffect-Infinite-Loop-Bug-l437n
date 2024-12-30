# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common bug in React 19 involving infinite loops within the `useEffect` hook.  The bug arises from improper dependency management within the `useEffect`'s dependency array, leading to the effect running repeatedly and causing performance issues or application crashes.

## Bug Description

The provided `bug.js` demonstrates a simple counter component where the `useEffect` hook attempts to increment a state variable on every render.  Because the `count` variable is not included in the dependency array, the effect is always triggered, creating an infinite loop. This is a common mistake when using `useEffect` for side effects that depend on state values.

## Solution

The `bugSolution.js` file offers a corrected version. The `count` variable is added to the dependency array which ensures that the `useEffect` hook only runs when `count` changes. This prevents the infinite loop and solves the bug.

## How to Reproduce

1. Clone this repository.
2. Navigate to the `bug` directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.  Observe the error message or infinite render loop.
5. Navigate to the `bugSolution` directory.
6. Run `npm install` to install dependencies.
7. Run `npm start` to start the development server. This will show a working version without the infinite loop.

This example showcases a critical aspect of React's state management and dependency handling in the `useEffect` hook.  Always ensure that you correctly specify the dependencies to avoid performance problems and unintended behavior.