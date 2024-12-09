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

/* 1.Type the Verilog program in Quartus Prime to implement the 4-bit Serial-In Serial Out
(SISO) Shift Register. 2.Compile and run the program to ensure the design is error-free.
3.Generate the RTL schematic to visualize the cascading D flip-flop connections and
save it for documentation. 4.Create nodes for the serial input (SI), clock (CLK), and serial
output (SO) to observe the shifting process during simulation. 5.Simulate the design for
different input serial data patterns and observe the timing diagrams. */

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:Ryan David Prasad RegisterNumber:24004080
*/
module ripple( input wire clk, // Clock input output reg [3:0] count // 4-bit counter
output ); // Counter logic always @(posedge clk) begin if (count == 4'b1111) // Reset
when count reaches 15 count <= 4'b0000; else count <= count + 1; // Increment count
end endmodule // Testbench module RippleCounter_tb; // Inputs reg clk; // Outputs
wire [3:0] count; // Instantiate the counter RippleCounter uut( .clk(clk), .count(count) ); //
Clock generation initial begin clk = 0; forever #5 clk = ~clk; // Toggle clock every 5 time
units end RTL LOGIC FOR 4 Bit Ripple Counter TIMING DIGRAMS FOR 4 Bit Ripple
Counter // Stimulus initial begin // Wait for a few clock cycles #10;
// Display header $display("Time | Count"); $display("-----------------");
// Functional table testing // Increment count 16 times and display the count repeat (16)
begin #5; // Wait for one clock cycle $display("%4d | %b", $time, count); end
// End simulation $finish; end endmodule

**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/5c739818-0c6a-4521-bbd6-76f048ee50b0)
![image](https://github.com/user-attachments/assets/d2445070-9803-4d05-84f2-be3847088692)


**RTL LOGIC FOR 4 Bit Ripple Counter**

![image](https://github.com/user-attachments/assets/d8f48368-ab4f-43fb-8f0e-be0fa4593be3)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![image](https://github.com/user-attachments/assets/a89571e2-bbce-4614-8f3d-38b83d0b0b82)

**RESULTS**
Thus, the 4-bit Ripple Counter was successfully implemented, and its
functionality was validated using the truth table.
