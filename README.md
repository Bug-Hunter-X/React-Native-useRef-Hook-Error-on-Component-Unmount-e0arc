# React Native useRef Hook Error on Component Unmount

This repository demonstrates a common error in React Native when using the `useRef` hook: attempting to access `ref.current` after the component has unmounted.  This often leads to unexpected behavior and crashes.  The solution provided uses the `useEffect` hook with cleanup to prevent this issue.

## Bug
The bug is present in `UnmountedRefBug.js`. The `MyComponent` uses `useRef` to store a reference to a timer. When the component unmounts, trying to clear the timer can cause this error if the component unmounted before the cleanup.