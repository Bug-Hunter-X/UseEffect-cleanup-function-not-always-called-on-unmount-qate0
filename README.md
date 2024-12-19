# React useEffect Cleanup Not Called on Unmount

This repository demonstrates a scenario where the cleanup function in React's `useEffect` hook might not be called properly when a component unmounts.  This can lead to memory leaks or other unexpected behavior.

## The Problem
The `useEffect` hook in the example code is designed to update a counter, logging messages to the console. The cleanup function should log a message upon unmounting the component. However, under certain conditions, such as rapid component re-renders or navigation changes, the cleanup might not always execute.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs. You might not always see the cleanup message when you rapidly click or navigate away. 

## Solution
The provided solution uses a combination of techniques to ensure cleanup happens reliably.