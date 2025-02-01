# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: omitting a state variable from the dependency array.  This leads to an infinite loop because the effect runs on every render, causing a continuous update cycle.

## Bug Description
The `useEffect` hook is designed to perform side effects after a component renders.  However, if a variable used within the effect is not included in the dependency array, the effect will run on every render, even if the value hasn't actually changed. This often creates an infinite render loop.

## Solution
The solution involves correctly specifying all state variables and other dependencies within the `useEffect` dependency array.