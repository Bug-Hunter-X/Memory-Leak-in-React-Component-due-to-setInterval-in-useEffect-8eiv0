# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications: a memory leak caused by the improper use of `setInterval` within the `useEffect` hook.  The issue arises when the `setInterval` is not properly cleaned up when the component unmounts, leading to continued updates even after the component has been removed from the DOM.

## Bug Description:
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts, resulting in a memory leak. This leak occurs because the interval continues to run in the background even after the component is no longer needed.

## Solution:
The `bugSolution.js` file provides a corrected version of the component.  It uses the return value of `useEffect` to clear the interval using `clearInterval` when the component is unmounted, effectively preventing the memory leak.

## How to run the examples:
1. Clone the repo: `git clone https://github.com/yourusername/react-useeffect-interval-leak.git`
2. Navigate to the directory: `cd react-useeffect-interval-leak`
3. Install dependencies: `npm install`
4. Run the buggy version: `npm start` (Look for the memory leak in your browser's developer tools)
5. Run the fixed version: `npm start` (Replace buggy version with the fixed version)
