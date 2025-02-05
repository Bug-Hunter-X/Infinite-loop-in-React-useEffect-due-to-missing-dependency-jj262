# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the `useEffect` hook's dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  If a dependency is missing from the dependency array, the effect will run on every render, potentially leading to an infinite loop if the effect modifies state which triggers a re-render.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console and the browser's behavior.

## Solution
The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` variable changes.