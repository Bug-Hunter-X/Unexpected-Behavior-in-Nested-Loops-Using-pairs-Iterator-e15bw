# Lua Nested Loops and pairs Iterator Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when used in nested loops with tables containing non-integer keys.  The bug involves unexpected behavior or potential infinite loops due to the way `pairs` iterates over tables.

## Bug Description
The `pairs` iterator in Lua, when used recursively in nested loops on tables with mixed key types, can exhibit unexpected iteration order or even infinite loops.  This is because the order `pairs` iterates over keys isn't always consistent for tables with non-integer keys.

## How to Reproduce
1. Clone this repository.
2. Run the `bug.lua` script.
3. Observe the unexpected output or potential infinite loop.

## Solution
The `bugSolution.lua` script provides a corrected approach. It demonstrates techniques to handle this situation robustly. The solution might involve using a different iteration method or explicitly managing the iteration order.