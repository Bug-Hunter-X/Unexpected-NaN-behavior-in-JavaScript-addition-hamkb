# Unexpected NaN Behavior in JavaScript Addition

This example demonstrates a common, yet subtle, error in JavaScript related to how it handles `NaN` (Not a Number) in arithmetic operations.

## The Problem

The `foo` function aims to add two numbers, handling potential `null` values. While `null` is handled correctly, adding `NaN` results in `NaN`, which can be unexpected in some situations.  JavaScript's loose typing and how it propagates `NaN` are the root cause.

## The Solution

The solution uses `isNaN()` to check for `NaN` before performing the addition. This prevents `NaN` from propagating and provides a more robust way to handle numerical inputs.