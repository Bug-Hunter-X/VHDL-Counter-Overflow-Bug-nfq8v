# VHDL Counter Overflow Bug
This repository demonstrates a common bug in VHDL: integer overflow in a counter.  The `buggy_counter.vhd` file contains code for a counter that is prone to overflow.  The `fixed_counter.vhd` provides a corrected version.

## Bug Description
The original code uses an `integer` type for the counter without explicit bounds checking. When the counter reaches its maximum value (15), incrementing it causes an overflow, leading to unpredictable behavior.  This is a subtle bug that can be hard to track down in larger designs.

## Solution
The corrected code in `fixed_counter.vhd` addresses the overflow issue by explicitly handling the case where the counter reaches its maximum value. This prevents unpredictable behavior and ensures the counter wraps around correctly.