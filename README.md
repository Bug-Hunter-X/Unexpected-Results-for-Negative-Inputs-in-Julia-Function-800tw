# Julia Function Bug: Unexpected Results for Negative Inputs

This repository demonstrates a bug in a simple Julia function that produces unexpected results when given negative inputs. The function is intended to square the input, returning a positive result for positive inputs and zero for zero inputs; however, it fails to do so correctly for negative inputs.

## Bug Description

The function uses a conditional statement to check the input value.  While it correctly handles positive and zero inputs, the `else` block's calculation (`return -x^2`) incorrectly negates the square, resulting in a negative value when a positive value is expected.

## Solution

A correct implementation would simply square the absolute value of the input, ensuring a non-negative output. This is achieved in the `bugSolution.jl` file.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run the `bug.jl` file using the Julia interpreter.
4. Observe the unexpected output for the negative input.
5. Run the `bugSolution.jl` file to see the corrected output.