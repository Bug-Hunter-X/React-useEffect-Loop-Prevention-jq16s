# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency array.  The `useEffect` hook, without a dependency array, runs after every render, leading to uncontrolled re-renders and potentially crashing the application.

## Bug Description

The `bug.js` file contains a component with a `useEffect` hook that logs the current count.  Because there is no dependency array (`[]`), the effect runs after every render, causing an infinite loop. Each log triggers a re-render, which triggers the effect again, creating a cycle.

## Solution

The `bugSolution.js` file shows the corrected version. By adding `[count]` as the dependency array, the effect only runs when the `count` variable changes. This breaks the infinite loop and makes the component behave as expected.