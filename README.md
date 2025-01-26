# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications: a missing dependency in the `useEffect` hook.  This can lead to unexpected behavior, such as infinite loops or incorrect updates. 

The `bug.js` file shows the incorrect implementation. The `bugSolution.js` file provides the corrected version.

## Bug Description
The useEffect hook in `bug.js` is missing the `count` variable in its dependency array. This means the effect runs on every render, causing an infinite loop as `setCount` triggers a re-render.

## Solution
The solution is adding `count` to the dependency array. This ensures that the effect only runs when the `count` value changes.