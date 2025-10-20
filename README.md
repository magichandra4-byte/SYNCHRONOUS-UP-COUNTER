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

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:vedha.M
RegisterNumber:25012201
*/UP COUNTER module ex11(out,clk,rst); input clk,rst; output reg [3:0]out; always @ (posedge clk) begin if(rst) out<=0; else out <= out+1; end endmodule DOWN COUNTER module ex12(out,clk,rst); input clk,rst; output reg [3:0]out; always @ (posedge clk) begin if(rst) out<=0; else out <= out-1; end endmodule

**RTL LOGIC UP COUNTER**
![WhatsApp Image 2025-10-10 at 10 44 10_527a8f3b](https://github.com/user-attachments/assets/9d94ee33-91a7-40e2-b0ae-386c645fbab9)
<img width="1207" height="592" alt="image" src="https://github.com/user-attachments/assets/a24763d9-fb66-4349-b136-18c3a4518813" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1317" height="343" alt="image" src="https://github.com/user-attachments/assets/e323a85f-143d-417e-b3b7-ddee52ee7d1a" />
<img width="1313" height="317" alt="image" src="https://github.com/user-attachments/assets/81b2c888-1c0a-4ebc-ad57-02c05454e6c0" />

**TRUTH TABLE**

**RESULTS**Thus the OUTPUT's of Synchronous and Asynchronous counter are verified by syntheswizing and simulating the VERILOG code.
