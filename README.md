# CS-223-Lab-4
This is an assignment given by Bilkent University in the cs 223 Digital Design course.

SystemVerilog code for Multifunction Register
 Reset operation will clear the outputs of all ip-ops on the rising edge of the clock (Q[3:0] = 0000). Reset input has priority over the other control inputs (s1s0).
 When s1s0 = 00 and the clock signal rises, each ip-op stores its own value and hence the register will retain its present content (Q3 ← Q3, Q2 ← Q2, Q1 ← Q1, Q0 ← Q0).
 When s1s0 = 01 and the clock signal rises, the register will perform a parallel load operation. Parallel load operation causes the register to get loaded with the external data inputs on the rising edge of the clock (Q3 ← D3,Q2 ← D2,Q1 ← D1,Q0 ← D0).
 When s1s0 = 10 and the clock signal rises, the register will perform a shift left operation. Shift left operation causes a left shift on the rising edge of the clock and shift_in input is shifted into the rightmost bit (lsb) of the register (Q3 ← Q2, Q2 ← Q1, Q1 ← Q0, Q0 ← shift_in).
 When s1s0 = 11 and the clock signal rises, the register will perform a shift right operation. Shift right operation causes a right shift on the rising edge of the clock and shift_in input is shifted into the leftmost bit (msb) of the register (Q3 ← shift_in, Q2 ← Q3, Q1 ← Q2, Q0 ← Q1).

SystemVerilog code for Binary-Coded Decimal Seven Segment Display in BASYS 3 
