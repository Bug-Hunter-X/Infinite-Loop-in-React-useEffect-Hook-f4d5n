# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: creating an infinite loop within the `useEffect` hook.  The bug occurs because the state is updated within the effect, causing a continuous re-render and triggering the effect again, infinitely.

## Bug Description
The `useEffect` hook's dependency array is missing. Adding `count` to the dependency array fixes the issue. It's essential that any value used within the useEffect that's modified from the component should be included as a dependency, otherwise it'll run in every render.