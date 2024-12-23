# React Native FlatList Performance Bug

This repository demonstrates a common performance issue in React Native's FlatList component when dealing with large datasets.  The bug causes slow scrolling and choppy performance due to unnecessary re-rendering of off-screen items.

## Bug Description

The provided `bug.js` file contains a FlatList component rendering a large dataset.  As you scroll, the performance degrades significantly. This is because FlatList, by default, re-renders all items, even those far off-screen.

## Solution

The `bugSolution.js` file demonstrates how to resolve this performance issue by optimizing FlatList's rendering behavior using the `removeClippedSubviews` and `initialNumToRender` props.  `removeClippedSubviews` instructs FlatList to remove items that are outside of the viewport, improving rendering efficiency.  `initialNumToRender` helps to improve initial render time by specifying the number of items to render on the initial mount.