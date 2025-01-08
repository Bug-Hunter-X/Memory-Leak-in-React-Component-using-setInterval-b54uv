# React setInterval Memory Leak

This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file shows the incorrect implementation, while `bugSolution.js` provides the corrected version.

**Problem:** The original code sets up an interval using `setInterval` but fails to clear the interval when the component unmounts. This leads to the interval continuing to run even after the component is no longer needed, causing a memory leak.

**Solution:** The solution adds a cleanup function to the `useEffect` hook. This function uses `clearInterval` to stop the interval when the component is unmounted, preventing the memory leak.