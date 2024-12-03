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

FULL ADDER

![image](https://github.com/user-attachments/assets/ae426589-e30a-490c-9db9-3c7924597e5e)


FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/001000d0-901f-4498-bdf9-52905d860dc3)




**Program:**
**DEVELOPED BY: BALAJI KAMARAJ**
**REG NO : 24901218**


i)FULL ADDER
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

ii)FULL SUBTRACTOR
```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & (a ^ b )));
endmodule
```
**RTL Schematic**

FULL ADDER

![image](https://github.com/user-attachments/assets/cb40e153-44b9-4b9d-8705-08c11821dee7)



FUL SUBTRACTER

![image](https://github.com/user-attachments/assets/1c29a5e4-7732-441d-b90a-08f7de46ebfc)


**Output Timing Waveform**

FULL ADDER

![image](https://github.com/user-attachments/assets/4e89744e-6008-4e3b-9a07-c92a35c50ad4)



FULL SUBTRACTER

![image](https://github.com/user-attachments/assets/7f8497da-ed3f-45a3-8453-d5a72d803a8f)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
