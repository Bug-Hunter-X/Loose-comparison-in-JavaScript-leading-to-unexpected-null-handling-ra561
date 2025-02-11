# JavaScript Loose Comparison Bug

This repository demonstrates a common JavaScript bug related to loose comparison (==) and its unexpected behavior when dealing with null values.  The bug arises from the incorrect usage of loose equality, leading to inaccurate results in certain conditional checks.

## Bug Description
The `foo` function intends to handle three cases: `null`, negative numbers, and non-negative numbers.  However, the use of loose comparison (`==`) in the `if (x == null)` check leads to an unexpected result when a value of `0` is passed.  This is because `0` is considered loosely equal to `null` in JavaScript, leading to the function returning `0` instead of `1`.  Strict comparison (`===`) should be used instead.

## Solution
The solution involves replacing the loose comparison (`==`) with strict equality (`===`). This ensures that the function correctly differentiates between `null` and `0`. 