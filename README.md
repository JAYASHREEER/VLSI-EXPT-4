# VLSI-EXPT-4
# SIMULATION AND SYNTHESIS SR, JK, T, D, FLIP FLOP COUNTER DESIGN USING VIVADO
## AIM :
       To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO
## APPARATUS REQUIRED : VIVADO 2023.2
## PROCEDURE :
STEP:1 Start the Vivado, Select and Name the New project.<br>
STEP:2 Select the device family, device, package and speed.<br>
STEP:3 Select new source in the New Project and select Verilog Module as the Source type.<br>
STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it.<br>
STEP:5 Select the Behavioural Simulation in the Source Window and click the check syntax.<br>
STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.<br>
## SR FLIP FLOP:
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/1029c59f-21ba-4978-bdf4-93f0510a2545)
## PROGRAM :
module sr_ff(clk,q,rst,s,r);<br>
input s,r,clk,rst; <br>
output reg q;<br>
always@(posedge clk)<br>
begin if(rst==1) q=1'b0;<br> 
else begin<br>
case({s,r})<br> 
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=1'bx;<br>
endcase<br> 
end<br> 
endmodule
## OUTPUT: 
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/921af2d7-c7b0-4842-a250-af75cebab437)

## JK FLIP FLOP :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/b2da2efb-f73b-43ae-8a89-c106eb35cc2d)
## PROGRAM :
module jk_ff(clk,q,rst,j,k);<br>
input j,k,clk,rst;<br> 
output reg q;<br>
always@(posedge clk)<br>
begin if(rst==1) <br>
q=1'b0;<br>
else begin<br>
case({j,k})<nbr> 
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br> 
2'b11:q=~q;<br> 
endcase<br>
end<br> 
endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/043f78c4-566b-4c34-b033-10849c7a004b)

## T FLIP FLOP :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/08491943-9453-4e7d-958b-c847f82b9af2)
## PROGRAM :
module t_ff(clk,q,rst,t);<br>
input t,clk,rst;<br> 
output reg q;<br> 
always@(posedge clk<br>) 
begin if(rst==1) <br>q=1'b0;<br> else if(t==0)<br> q=q;<br> else<br>
q=~q;<br> 
end<br> 
endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/e14f60ca-26c0-4f48-9507-f7a2ddb8d149)

## D FLIP FLOP :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/6277a127-0aea-41bd-bba9-5bbd41a4c440)
## PROGRAM :
module d_ff(clk,q,rst,d);<br>
input d,clk,rst;<br>
output reg q;<br> 
always@(posedge clk)<br>
begin<br>
if(rst==1)<br> 
q=1'b0;<br>
else<br> q=d;<br>
end<br> endmodule<br>
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/c23e8684-f469-4925-9f0f-01c1b72152c8)

## MOD 10 COUNTERR :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/048676d5-db25-4750-8231-696abb87f270)
## PROGRAM :
module mod_10(clk,rst,out);<br> 
input clk,rst;<br>
output reg[3:0]out;<br> 
always@(posedge clk)<br>
begin if(rst==1|out==9) <br>
out=4'b0;<br>
else<br>
out=out+1;<br>
end<br>
endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/76db017c-fe86-43ba-b69f-d62577dd4793)

## UPO DOWN COUNTER :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/dac62a99-31fb-4561-bc0f-3e0ae8676b14)

## PROGRAM :
module updown_counter(clk,rst,ud,out);<br> 
input clk,rst,ud;<br>
output reg[3:0]out;<br> 
always@(posedge clk)<br> 
begin if(rst==1) out=4'b0;<br> 
else if (ud==1) out=out+1;<br> 
else if(ud==0) out=out-1;<br> 
end<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-4/assets/166278992/279bf052-67e8-4f31-a246-691c246aad85)

## RESULT :
 Thus, the simulation and synthesis of SR,JK,T,D FLIPFLOP,COUNTER DESIGN using VIVADO .











