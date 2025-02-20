# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The `useEffect` hook, when used improperly, can lead to an infinite render loop, causing the application to become unresponsive.

The bug is caused by missing dependencies in the dependency array of useEffect.  This causes the effect to re-run after every render, creating a cycle of re-renders. 

The solution involves adding the relevant state variable to the dependency array so the effect only runs when that specific variable changes.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console and the unresponsive application.

## Solution

The solution is provided in `bugSolution.js`, adding 'count' to the useEffect dependency array.