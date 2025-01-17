# Incorrect State Update in React Functional Component

This repository demonstrates a common error in React functional components: incorrectly updating state by directly using the previous state value within the state update function. This can lead to unexpected behavior or incorrect updates.

## Bug Description

The bug is in the `incrementCount` function. It attempts to increment the `count` state by directly using the `count` variable inside `setCount`. Because the `setCount` function is asynchronous, the use of the old value may lead to lost updates or stale closure issues.

## Solution

The solution utilizes the functional update form of `setCount` which ensures use of the latest state value before performing the increment operation. The new state is calculated based on the previous state via a function passed to setCount.