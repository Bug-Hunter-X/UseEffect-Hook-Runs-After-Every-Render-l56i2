# React useEffect Hook Runs After Every Render

This repository demonstrates a common error in React applications where the `useEffect` hook runs after every render due to a missing or incorrect dependency array.  This can lead to performance issues and unexpected behavior.

The `bug.js` file shows the problematic code. The `bugSolution.js` file demonstrates the corrected version with a properly defined dependency array.

## Problem

The `useEffect` hook in the initial example doesn't specify a dependency array.  This means it runs after every render, even if the dependencies haven't changed.

## Solution

To fix this, you need to pass an array of values that `useEffect` should depend on. If the values in the array haven't changed between renders, the effect won't run again. In this case, the `count` variable should be included in the dependency array. 