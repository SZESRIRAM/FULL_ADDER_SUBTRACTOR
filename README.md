# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**\
Full adder\
<img width="518" height="463" alt="image" src="https://github.com/user-attachments/assets/cc33b606-37a9-470f-84a6-5edcd3c09d7f" />

Full Subtractor\
<img width="300" height="179" alt="image" src="https://github.com/user-attachments/assets/c1ee7417-21df-4480-99f9-65c8b8e1d623" />


**Procedure**\
Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

Write the detailed procedure here

**Program:**\
```
module EXP4(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
wire a0;
not(a0,a);
assign sum = a ^ b ^ cin;
assign carry = (a & b) | (b & cin) | (a & cin);
assign DIFF = a ^ b ^ cin;
assign BO = (a0 & b) | (a0 & cin) | (b & cin);
endmodule
```
**RTL Schematic**\
<img width="648" height="562" alt="image" src="https://github.com/user-attachments/assets/b28eaf36-5c8b-4ae2-95f6-a83a40f2da10" />


**Output Timing Waveform**\
<img width="1917" height="1021" alt="image" src="https://github.com/user-attachments/assets/9bbaab7e-17fc-411d-8095-603881016360" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



