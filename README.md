# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

Open Quartus Prime software and create a new project.
Create a new Verilog HDL file and enter the 4-bit ripple counter program.
Save the file and set the module as the top-level entity.
Compile the design and check for syntax errors.
Create a waveform file and apply clock and reset inputs for simulation.
Run functional simulation and verify the output timing diagram with the counter truth table.

**PROGRAM**
```
/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by: V G SAIRAIMA
 RegisterNumber:212225040359
*/
module t1 (a,b,c,d,clk,rst,t);
input clk,rst,t;
output a,b,c,d;
wire a,b,c,d;

Tflipflop T0(d,clk,rst,t);
Tflipflop T1(c,d,rst,t);
Tflipflop T2(b,c,rst,t);
Tflipflop T3(a,b,rst,t);
endmodule

module Tflipflop(q,clk,rst,t);
input clk,rst,t;
output reg q;
always @(posedge clk)
begin
if (!rst)
q <= 0;
else
q <= (t ? ~q : q);
end
endmodule
```
**RTL LOGIC FOR 4 Bit Ripple Counter**:
![image](https://github.com/VGSAIRAIMA/4-BIT-RIPPLE-COUNTER/blob/main/Screenshot%202026-03-24%20184240.png)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
![image](https://github.com/VGSAIRAIMA/4-BIT-RIPPLE-COUNTER/blob/main/Screenshot%202026-03-24%20184411.png)

**RESULTS**:Implemented  4 Bit Ripple Counter using verilog and validated their functionality using their functional tables.


