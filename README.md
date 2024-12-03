# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using Verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, the D latch operates with an enable signal. That means, the output of the D flip-flop is insensitive to the changes in the input, D except for the active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has a single input D and two outputs Qtt & Qtt’. The operation of the D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when the positive transition of the clock signal is applied instead of active enable. The following table shows the state table of the D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, the D flip-flop always Holds the information, which is available on data input, D of earlier positive transition of the clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of the D flip-flop is always equal to the data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers, and some of the counters.

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**PROGRAM**

Program for flip-flops and verify its truth table in quartus using Verilog programming. 
### Developed by: Pooja Sri B RegisterNumber: 24007629
```
module dflip(d,clk,q,qbar);
input d,clk;
output q,qbar;
wire w1,w2;
not(w1,d);
nand(w2,d,clk);
nand(w3,w1,clk);
nand(q,w2,qbar);
nand(qbar,q,w3);
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![WhatsApp Image 2024-10-24 at 11 11 08_74a3588b](https://github.com/user-attachments/assets/2ea46065-c901-4c0b-8711-34e8eabc86da)

**TIMING DIAGRAMS FOR FLIP FLOPS**
![WhatsApp Image 2024-10-24 at 11 16 26_44fcd80b](https://github.com/user-attachments/assets/894b38fa-744c-4a87-966a-230b9d4a3bf3)


**RESULTS**
implementation of D flipflop using Verilog is successful
