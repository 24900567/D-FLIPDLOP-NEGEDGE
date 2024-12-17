# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

/* write all the steps invloved */
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: DHINESH S RegisterNumber: 24900567
*/
```
module D_ff (D, Clk,Q,Qbar);
input D,Clk;
output Q,Qbar;
wire w1,w2,w3;
not (w1,D);
nand(w2,D,Clk);
nand(w3,w1,Clk);
nand(Q,w2,Qbar);
nand(Qbar,Q,w3);
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-12-17 114236](https://github.com/user-attachments/assets/e1000e4e-176b-4aea-b0dd-661ee40050ad)


**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-17 114248](https://github.com/user-attachments/assets/3734e662-663e-428b-8e70-72261f4f9078)


**RESULTS**
Thus the code executed successfully for D-FlipFlop.
