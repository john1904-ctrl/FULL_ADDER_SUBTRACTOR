NAME: M.JOHNPALL

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

**Truthtable**
Full Adder:
![image](https://github.com/user-attachments/assets/87349b01-447e-46b6-920e-9cb74dd5703c)

Full Subtractor:
![image](https://github.com/user-attachments/assets/7c2851f6-5a0d-42e9-911c-f1897c4fae5e)

**Procedure**

Open Quartus Software
Create a New Project
Create a New Design File
Compile the Program
Generate RTL Schematic
Create Nodes for Inputs/Outputs
Generate Timing Diagram
Simulate Different Input Combinations
Save Your Work

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: SATHISH KUMAR M
RegisterNumber: 212224230256
*/
```
```
Full Adder: 

module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

Full Subtractor:

module fullsub(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule
```

**RTL Schematic**

**FULL ADDER**

![fulladd](https://github.com/user-attachments/assets/064ba51f-d2f4-4f6c-a501-7a08f4c9d1d8)

**FULL SUBTRACTOR**

![fullsub](https://github.com/user-attachments/assets/b94e2f1d-e91b-4915-b291-3a7317304b46)

**Output Timing Waveform**

Full Adder:
![fulladdtime](https://github.com/user-attachments/assets/5f747bd0-5c99-4bcc-a99e-2c7fdb9240c7)

Full Subtrator:
![fullsubtime](https://github.com/user-attachments/assets/d79b2e5c-480b-41a7-ba39-1ab9b3473dad)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



