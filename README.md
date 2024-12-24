# Off-by-one error in TypeScript

This repository demonstrates a common off-by-one error in TypeScript for loops. The code attempts to iterate over an array, but the loop condition is incorrect, causing an error.

## Bug

The `printArray` function iterates over an array using a for loop. The loop condition `i <= arr.length` is incorrect, as arrays are zero-indexed. The correct condition should be `i < arr.length`. This leads to an attempt to access an element beyond the bounds of the array, resulting in an error.

## Solution

The solution is to change the loop condition to `i < arr.length`. This ensures that the loop iterates through all the elements of the array without attempting to access an element that does not exist.

## How to reproduce

1. Clone this repository.
2. Open `bug.ts` and run the code using a TypeScript compiler (like tsc). 
3. You will see an error indicating an array index out of bounds.
4. Open `bugSolution.ts` and run the code. This will print the array correctly.