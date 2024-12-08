# React Native Dimensions API Orientation Change Issue

This repository demonstrates a bug in React Native where the `Dimensions` API doesn't immediately update its values when the device orientation changes. This leads to layout problems. The solution involves using the `Dimensions` API with `useEffect` and `onLayout` to ensure the layout is adjusted accordingly.

## Bug

The provided `bug.js` file shows how using `Dimensions.get('window')` directly within a component results in incorrect dimensions after an orientation change. The styles are calculated only once upon render and the component does not rerender even after the device orientation is changed. 

## Solution

The `bugSolution.js` file provides a solution that uses the `useEffect` hook and `onLayout` prop for proper dimension handling and update on orientation changes.