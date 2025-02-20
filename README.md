# React Native: undefined is not an object (evaluating 'this.state.data')

This repository demonstrates a common error in React Native applications: attempting to access component state or props before the component has fully mounted.  This often happens when fetching data asynchronously within `componentDidMount`.

## Problem

The `bug.js` file showcases a component that fetches data and displays it.  However, if the component unmounts before the data fetch completes, or if you try to access `this.state.data` before it's populated, you'll encounter the error: `undefined is not an object (evaluating 'this.state.data')`.

## Solution

The `bugSolution.js` file provides a solution using the `useEffect` hook and a conditional rendering approach to handle potential undefined state during the data fetching process.  This ensures that the application gracefully handles the asynchronous data retrieval without causing runtime errors.

## How to Run

1. Clone this repository.
2. `cd` into the project directory.
3. Run `npm install`.
4. Run `npx react-native run-android` (or `npx react-native run-ios`).

Observe the difference in behavior and error handling between the two examples.