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

/* write all the steps invloved */

**PROGRAM**
module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(!rstn)
     out<=0;
   else 
     out <= out+1;
end
endmodule

Developed by : VISHAL.R
RegisterNumber : 24900248

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: RegisterNumber:24900248
*/

**RTL LOGIC UP COUNTER**
![392217643-def6b99e-094b-480e-a0a7-790ed62a9180](https://github.com/user-attachments/assets/7fd832d4-8c78-45a0-8bf3-d73567abe939)


**TIMING DIAGRAM FOR IP COUNTER**
![392217703-ec6eced3-c2d0-422c-85b9-51c03f267de2](https://github.com/user-attachments/assets/a63b3747-c6d4-4485-a09a-345ebf6e2ff6)


**TRUTH TABLE**
![392217731-003ea65e-7a92-4b8f-bae2-d52903ec2603](https://github.com/user-attachments/assets/a0466e64-b78b-4d70-ab69-e0458b567bc0)


**RESULTS**
