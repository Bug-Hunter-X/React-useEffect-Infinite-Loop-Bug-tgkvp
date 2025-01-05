# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## Bug Description
The `MyComponent` component uses `useEffect` to update a counter every second. However, the dependency array is empty (`[]`), meaning the effect runs after every render. This causes the `setCount` function to be called repeatedly, leading to an infinite loop. 

## Solution
The solution involves adding the `count` state variable to the dependency array. This ensures that the effect only runs when the `count` value changes.  This prevents the unnecessary re-renders and solves the infinite loop problem.