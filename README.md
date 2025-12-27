AIM:

To implement JK flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

JK Flip-Flop

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

image<img width="716" height="452" alt="Screenshot 2025-12-27 133036" src="https://github.com/user-attachments/assets/f33e573d-4940-4f21-a1cb-2c41f1866029" />


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

image<img width="503" height="356" alt="Screenshot 2025-12-27 133112" src="https://github.com/user-attachments/assets/cea5ba8e-a97c-4c3f-aecf-6470e242bd80" />


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

image<img width="683" height="551" alt="Screenshot 2025-12-27 133143" src="https://github.com/user-attachments/assets/c5186de2-fa3c-4cd4-9764-0d390cfaac5f" />


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

image
<img width="718" height="253" alt="Screenshot 2025-12-27 133222" src="https://github.com/user-attachments/assets/0789108f-29e1-407d-bc9e-221f9a0c28f8" />

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

Procedure

Define Inputs/Outputs: Inputs: J (Set), K (Reset), c1k (clock); Outputs: q, qbar (~q).
Initialization: Set q = 0 and qbar = 1 at the start of the simulation.
JK Flip-Flop Logic: On posedge c1k, compute q
Complementary Output: Update qbar = ~q to maintain complementarity.
Testbench: Simulate with combinations of J, K, and c1k to verify JK Flip-Flop functionality.
PROGRAM

module exp7(J,K,c1k,q,qbar);
input J,K,c1k;
output reg q;
output reg qbar;
initial q=0;
initial qbar=1;
always @(posedge c1k)
begin
q=((J&(~q)))|((~K)&q);
qbar=~q;
end
endmodule
Developed by: J.SRI SARAN  RegisterNumber:25015592
RTL LOGIC FOR FLIPFLOPS image
<img width="1034" height="635" alt="Screenshot 2025-12-27 133308" src="https://github.com/user-attachments/assets/dd0e1544-30d4-48d5-96ac-c141b6d47be2" />

TIMING DIGRAMS FOR FLIP FLOPS image
<img width="1041" height="657" alt="Screenshot 2025-12-27 133341" src="https://github.com/user-attachments/assets/da4c8899-2ed6-4cb4-b1ac-77f3b92188a8" />


RESULTS;
THUS IT IS EXEXUTED AND UPDATED SUCEESFULLY.....
