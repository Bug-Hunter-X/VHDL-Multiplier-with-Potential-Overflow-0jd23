# VHDL Multiplier with Potential Overflow

This repository demonstrates a potential overflow issue in a simple VHDL multiplier. The original code performs multiplication of two UNSIGNED vectors without explicitly handling potential overflow conditions. The fixed version addresses this by using a larger result vector to accommodate the maximum possible product.

## Bug Description
The `multiplier.vhdl` file contains a VHDL implementation of an 8-bit unsigned multiplier.  The multiplication of two 8-bit numbers can result in a number that requires up to 16 bits to represent accurately. If the result exceeds 15 bits, an overflow occurs, leading to an incorrect result. 

## Solution
The `multiplier_fixed.vhdl` addresses the overflow issue by increasing the width of the `product` signal to accommodate the maximum possible output of the multiplication. This ensures that all possible results are accurately represented.

## How to use
1. Compile and simulate the original and fixed versions of the multiplier using your favorite VHDL simulator (e.g., ModelSim, GHDL, etc.). 
2. Compare the simulation results to verify that the fixed version correctly handles all cases, including those with potential overflow.
