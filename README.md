# Tcl Unexpected Comparison Behavior

This repository demonstrates an uncommon bug related to unexpected comparison behavior in Tcl.  The issue is in the `badproc` procedure. While seemingly simple, it showcases a potential pitfall for developers not fully aware of Tcl's nuances regarding value comparison.

## Bug Description
The `badproc` procedure is intended to return 1 if the input `x` is 0, and 0 otherwise.  However, due to how Tcl handles string and numeric comparisons, it may not always produce the expected results, especially if the input is not explicitly treated as a number.

## How to Reproduce
1. Clone this repository.
2. Run `tclsh bug.tcl`. Observe the unexpected output.
3. Run `tclsh bugSolution.tcl`. Observe the corrected behavior.

## Solution
The solution demonstrates the use of explicit numeric comparison using the `==` operator with careful type consideration to ensure reliable results in all cases. 

This example highlights the importance of understanding Tcl's type system and its implications for comparisons and control flow.