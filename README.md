# Haskell Lazy Evaluation Bug

This repository demonstrates a subtle bug in Haskell related to lazy evaluation and infinite lists within `IO` actions. The program hangs because the `take` function never completes due to the lazy nature of list evaluation.

## Bug Description
The `bug.hs` file contains code that attempts to take 5 elements from an infinite list generated within an `IO` action using `forever`. This results in the program hanging indefinitely.

## Solution
The `bugSolution.hs` provides a corrected version that addresses this issue by properly managing the infinite list and forcing evaluation within a safe context.  This demonstrates the importance of understanding Haskell's lazy evaluation model and how to avoid infinite loops when working with `IO`.