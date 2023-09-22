# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure
Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.
Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
Analyze and Fix Errors:*

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.
6.*Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

### 
Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: sivaram R
RegisterNumber:  212222100050
## HALF ADDER
```
module Experiment03(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
## FULL ADDER
```
module EX03(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
### RTL
## HALF ADDER:
![HALF ADDER](https://github.com/sivaram-R/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/121165794/f77b79a7-cc0a-46b9-a4aa-699ce0cf2ea0)
## FULL ADDER:
![FULL ADDER](https://github.com/sivaram-R/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/121165794/5a433ae4-2b57-4d17-af44-710b1623cca3)

### TRUTH TABLE 
## HALF ADDER:
![HALF TT](https://github.com/sivaram-R/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/121165794/1c4f44c1-bb76-4799-85e8-5ce93bc154ce)
## FULL ADDER:
![FULL TT](https://github.com/sivaram-R/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/121165794/ea267b18-45ab-4e86-bb0e-47ca30887e7b)

### OUTPUT
## HALF ADDER:
![HALF OP](https://github.com/sivaram-R/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/121165794/ba511ec4-85ae-4e29-85ba-dda83a9fa474)
## FULL ADDER:
![FULL OP](https://github.com/sivaram-R/Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/121165794/284ca748-8f20-453e-adfb-e63a9ef1ccb4)

### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
