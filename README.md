# React 18+ useEffect Missing Cleanup: setInterval without cleanup

This repository demonstrates a common error in React 18 and later versions: forgetting to include a cleanup function in `useEffect` when using `setInterval`.  This can lead to memory leaks and unexpected behavior.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The `setInterval` function in `bug.js` starts a timer that updates the counter every second. However, it lacks a cleanup function. This means that when the component unmounts, the interval continues to run, potentially causing memory leaks and other issues.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle `setInterval` within `useEffect`. A cleanup function is used to clear the interval when the component unmounts, ensuring that resources are properly released.