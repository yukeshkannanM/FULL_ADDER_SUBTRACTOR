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
FULL ADDER:

<img width="464" height="203" alt="image" src="https://github.com/user-attachments/assets/1c8f1558-5890-460a-89ce-8be93a555f68" />

FULL SUBTRACTOR
<img width="455" height="475" alt="image" src="https://github.com/user-attachments/assets/cc440300-723d-4dc6-a527-6c5d798fd56c" />



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using
Verilog programming.

i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule


**RTL Schematic**
FULL ADDER:
<img width="1234" height="426" alt="image" src="https://github.com/user-attachments/assets/97f56040-a6c7-4f5d-8602-e64094752420" />

FULL SUBTRACTOR
<img width="1285" height="335" alt="image" src="https://github.com/user-attachments/assets/a3d1d24b-6cda-45fe-afcb-9be12a290d93" />

**Output Timing Waveform**
FULL ADDER:
<img width="1305" height="314" alt="image" src="https://github.com/user-attachments/assets/c3713f56-9465-40b5-b6d4-606de4651484" />
FULL SUBTRACTOR:
<img width="1306" height="275" alt="image" src="https://github.com/user-attachments/assets/1af3db45-444c-4302-aed3-ac8b135c343b" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



