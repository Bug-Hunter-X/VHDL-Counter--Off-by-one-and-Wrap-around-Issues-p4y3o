# VHDL Counter Bug and Solution

This repository demonstrates a common error in VHDL counters and provides a corrected version.

## Bug
The original `counter.vhdl` file implements a simple counter. However, it has two potential problems:

1. **Off-by-one error:** The counter might not reach the maximum value before resetting (if used in a larger design with a limited clock cycle count).
2. **Wrap-around handling:** It doesn't explicitly define behavior when `internal_count` reaches 15; the result is implementation-defined, leading to unpredictable behavior.

## Solution
The fixed version in `counter_fixed.vhdl` addresses these issues using a `MOD` operator for proper wrapping, ensuring that the counter cycles correctly between 0 and 15.

## How to Use
1. Simulate both `counter.vhdl` and `counter_fixed.vhdl` using your preferred VHDL simulator (ModelSim, GHDL, etc.).
2. Observe the outputs to verify that the corrected version behaves as expected.