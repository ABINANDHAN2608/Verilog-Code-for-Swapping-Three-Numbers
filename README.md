# Verilog-Code-for-Swapping-Three-Numbers
## NAME: ABINANDHAN G
## REG NO: 212223060003
Aim
To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.

Apparatus Required
Vivado 2023.1 or equivalent Verilog simulation tool.

Procedure
Launch Vivado 2023.1:

Open Vivado and create a new project.
Write the Verilog Code for Swapping:

Write the Verilog code that swaps the values of three numbers (a, b, and c) using basic arithmetic or bitwise operations without using temporary variables.
Create the Testbench:

Write a testbench to simulate the swapping operation. The testbench should initialize three numbers, trigger the swapping module, and check if the values are swapped correctly.
Add the Verilog Files:

Add the Verilog module and the testbench file to the Vivado project.
Run Simulation:

Run the behavioral simulation in Vivado to verify the swapping operation.
Observe the Waveforms:

Examine the waveform to confirm that the values of the three numbers are swapped as expected.
Save and Document Results:

Capture the waveform output and include the results in your report for verification.

Verilog Code:
## blocking
```
module swap_three_numbers(input [7:0]a_in,
input[7:0]b_in,
input[7:0]c_in,
output reg[7:0]a_out,
output reg[7:0]b_out,
output reg[7:0]c_out);

//blocking
always @(*)
begin
a_out=b_in;
b_out=c_in;
c_out=a_in;
end
endmodule
```
OUTPUT:
![Screenshot 2025-04-12 143226](https://github.com/user-attachments/assets/10ea341f-96f8-44ba-9de8-3917c842fbf9)

## Non-Blocking
```
module swap_three_numbers(input [7:0]a_in,
input[7:0]b_in,
input[7:0]c_in,
output reg[7:0]a_out,
output reg[7:0]b_out,
output reg[7:0]c_out);
//non-blocking 
always @(*)
begin
a_out<=b_in;
b_out<=c_in ;
c_out<=a_in;
end
endmodule
```
OUTPUT:
![Screenshot 2025-04-12 143957](https://github.com/user-attachments/assets/21c60ee2-14fd-4cb0-9146-25b0c006a960)

## Blocking
```
module swap_three_numbers;
reg[3:0]a,b,c;
initial
begin
     a=4'd8;
     b=4'd7;
     c=4'd6;
     
     end 
always @(*)
begin
 a=b; 
 b=c;
 c=a;
 end 
 endmodule
```
 OUTPUT:
 ![Screenshot 2025-04-12 145312](https://github.com/user-attachments/assets/55db4ad6-6f84-4e66-b3ef-5b02aff40af3)

 ## Non-Blocking
 ```
module swap_three_numbers;
reg[3:0]a,b,c;
initial
begin
     a=4'd8;
     b=4'd7;
     c=4'd6;
     
     end 
always @(*)
begin
 a<=b; 
 b<=c;
 c<=a;
 end 
 endmodule
```
OUTPUT:
![Screenshot 2025-04-12 145544](https://github.com/user-attachments/assets/2bedb5ae-f073-4661-a6cd-8d0b8f972c58)


 






Conclusion:

In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated. The testbench verified the swapping operation, showing that the values of three input numbers (a, b, and c) were swapped correctly without the use of temporary variables. This experiment demonstrated the effectiveness of Verilog in implementing logical operations and control mechanisms such as swapping values. The simulation results confirm the correct functionality of the design.
