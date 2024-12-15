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
![Screenshot 2024-12-15 133652](https://github.com/user-attachments/assets/6ae772da-1a41-4e76-99bb-c926f7415bdc)

![Screenshot 2024-12-15 133711](https://github.com/user-attachments/assets/c8549738-868e-4298-ae43-0007d6b8c1b3)

**Procedure**

Write the detailed procedure here

**Program:**
```
module fulladder(a, b, cin, sum, carry); input a, b, cin; output sum, carry;
 assign sum = ( (a ^ b) ^ cin ); assign carry = ( (a & b) | ( cin & (a ^ b) ) ); endmodule


 module fullsub(a,b,bin,difference,borrow); input a,b,bin; output difference,borrow;
 assign difference = (a ^ b)^bin; assign borrow= ( a & b) | ( bin & ((a ^ b )));
 endmodule
```

**RTL Schematic**

![Screenshot 2024-12-15 133840](https://github.com/user-attachments/assets/d23273c3-5673-4d84-aff4-661322d44f38)

![Screenshot 2024-12-15 133854](https://github.com/user-attachments/assets/c797c4fd-0d41-42c3-9d43-8eac81889f81)


**Output Timing Waveform**

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



