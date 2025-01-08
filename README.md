# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by omitting a dependency from the dependency array.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders.  If a value used within the effect changes between renders, it should be listed in the dependency array.  Failure to do so can cause unexpected behavior, including infinite render loops.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output.  You'll see that the count updates infinitely, resulting in a potential crash or performance issue.

## Solution

The solution involves ensuring that `count` is included in the dependency array of `useEffect`.  This ensures that the effect only runs when the `count` value actually changes.