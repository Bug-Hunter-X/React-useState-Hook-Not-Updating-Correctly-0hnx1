# React useState Hook Unexpected Behavior

This repository demonstrates a subtle bug related to the `useState` hook in React. When the increment button is clicked, the counter doesn't always increment by two.  This is because of how state updates are handled in React's functional components. 

## Problem
The issue lies within the `handleClick` function. Calling `setCount` multiple times in quick succession leads to unexpected behavior because React batches state updates.  Only the final update is applied, skipping intermediate ones.