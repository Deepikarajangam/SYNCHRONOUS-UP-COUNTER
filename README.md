### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved  
Compile and run the program.
Generate the RTL schematic and save the logic diagram.
Create nodes for inputs and outputs to generate the timing diagram. 
For different input combinations generate the timing diagram.
*/

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:R.DEEPIKA RegisterNumber:24900220

```
module suc(clk,rst,q);
input clk,rst;
output[2:0]q;
reg[2:0]q;
always@(posedge clk)
    if(~rst==0)
      q<=3'b0;
		else
		q<=q+1'b1;
		endmodule
```
*/

**RTL LOGIC UP COUNTER**

![image](https://github.com/user-attachments/assets/77a08539-8689-4b74-9f8c-840648013004)




**TIMING DIAGRAM FOR IP COUNTER**

![image](https://github.com/user-attachments/assets/466574aa-0caa-4a70-9961-a37056d2866d)



**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/663a1d0d-3b66-4aa6-a7d5-0eddd777fad7)


**RESULTS**
Therefore Synchronous counter In always @ method using verilog and validating their functionally using their functional tables is verify.
