# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the improper use of `setInterval` within the `useEffect` hook.  The issue results in a memory leak as the interval continues to run even after the component is unmounted, leading to performance degradation.

The `bug.js` file contains the faulty code, while `bugSolution.js` provides the corrected implementation.

**Problem:** The original code uses `setInterval` without a cleanup function within the `useEffect` hook. This means the interval continues running even when the component is unmounted, consuming resources and potentially leading to memory leaks.

**Solution:** The corrected version uses the cleanup function returned by `useEffect` to clear the interval when the component unmounts, thus preventing the memory leak.  This ensures that resources are released properly.
