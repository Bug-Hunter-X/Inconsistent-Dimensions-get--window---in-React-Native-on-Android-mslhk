# Inconsistent Dimensions.get('window') in React Native on Android

This repository demonstrates a bug in React Native where `Dimensions.get('window')` returns `undefined` or inaccurate dimensions on Android devices, particularly during app initialization and orientation changes. This leads to inconsistent layout behavior and rendering problems.

## Bug Description

The `Dimensions` API, used to access screen dimensions, sometimes returns incorrect or undefined values, especially on Android. This is inconsistent and makes it difficult to create responsive layouts.

## How to Reproduce

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Observe the initial layout and the layout after changing the screen orientation.  The layout might be incorrect or broken depending on the device and timing.

## Solution

The solution uses the `useEffect` hook and `Dimensions.addEventListener` to listen for changes in dimensions and updates the component state accordingly. This ensures the app uses correct dimensions even when the initial dimensions are inaccurate.