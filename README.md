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

**Procedure**

Write the detailed procedure here

**Program:**

module f1_logic(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(c&a);
endmodule


module f2_logic(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&b)|(~(a^b)&c);
endmodule

**RTL Schematic**
<img width="1920" height="1080" alt="f1" src="https://github.com/user-attachments/assets/6ee569d9-994f-478f-bcab-4b9a4bf8fb97" />


<img width="1920" height="1080" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/1877325f-4e21-4908-a574-c053f2d18bfa" />


**Output Timing Waveform**

<img width="1920" height="1080" alt="f1 (2)" src="https://github.com/user-attachments/assets/573613e1-7598-4bfd-9111-460db423b9e1" />

<img width="1920" height="1080" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/ff635df6-401a-4455-b11d-a47f64b4e1b6" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



