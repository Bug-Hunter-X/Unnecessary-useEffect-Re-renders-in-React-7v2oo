# Unnecessary useEffect Re-renders in React

This repository demonstrates a common React bug involving the `useEffect` hook.  The provided `MyComponent` unnecessarily re-renders the `useEffect` hook on every render, leading to performance problems and potentially unexpected behavior. The solution illustrates how to properly use the dependency array to optimize re-renders.

## Bug

The original `MyComponent` uses `useEffect` without specifying a dependency array or an empty array `[]`. This results in the effect running after every render, including the initial render.  This can cause unnecessary computations, log messages, or API calls. 

## Solution

The solution correctly uses a dependency array `[count]` to specify that the effect should only re-run when the value of the `count` variable changes. This prevents unnecessary re-renders and improves performance.  The solution also handles the case of having no dependencies, showing the correct way to handle this edge case.