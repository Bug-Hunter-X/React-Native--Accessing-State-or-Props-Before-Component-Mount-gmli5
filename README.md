# React Native: Accessing State or Props Before Component Mount

This repository demonstrates a common error in React Native: attempting to access a component's state or props before it has fully mounted.  This often results in unexpected behavior or errors.  The `bug.js` file contains the problematic code, while `bugSolution.js` shows a corrected version.

## Problem

The issue arises when asynchronous operations or initializations are performed before the component's lifecycle methods (`componentDidMount`, `constructor`) have fully completed.  This can lead to `undefined` or `null` values when attempting to access props or state.

## Solution

The corrected code in `bugSolution.js` utilizes asynchronous operations safely within `componentDidMount` and ensures proper handling of loading states to prevent errors.  It also demonstrates the use of `useEffect` hook in functional components to address similar issues.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the application using your preferred React Native environment.
4. Observe the behavior of both the problematic and corrected components.