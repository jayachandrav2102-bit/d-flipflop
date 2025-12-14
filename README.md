AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables


SOFTWARE REQUIRED:

Quartus prime

THEORY

A D Flip-Flop is a sequential circuit that captures the value of the data input (D) at the rising or falling edge of the clock (CLK) and holds it until the next clock edge.


Input: D (Data), CLK (Clock)

Outputs: Q (Current state), Q’ (Complement of Q)

The output Q follows D only at the triggering clock edge.

Useful for data storage, registers, and memory elements.


Procedure

1.Open your Verilog IDE (Xilinx ISE/Vivado).

2.Create a new project and add a Verilog module named d_flipflop.

3.Declare inputs D and CLK, and outputs Q and Q’.

4.Implement the flip-flop behavior using an always block triggered by posedge CLK.

5.Compile and synthesize the design.

6.Simulate using a testbench to apply different D inputs and observe Q and Q’.

7.Verify that Q changes to D only at the clock edge.


PROGRAM:
~~~
module d_ff (
    input  wire clk, rst, D,
    output reg  Q
);
    always @(posedge clk or posedge rst) begin
        if (rst)
            Q <= 1'b0;   // Reset
        else
            Q <= D;      // Capture D at clock edge
    end
endmodule

Developed by:JAYACHANDRA V
RegisterNumber:25017587 */
~~~


RTL LOGIC FOR FLIPFLOPS

TIMING DIGRAMS FOR FLIP FLOPS

RESULTS:

 Thus the D flipflop using verilog and validating their functionality using their functional tables is implemented and verified.
