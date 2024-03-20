# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable

**Full Adder**

![image](https://github.com/karthik-2106/FULL_ADDER_SUBTRACTOR/assets/150319557/164c9b6d-f3b3-4e1e-984f-377556318da3)

**Full Subtractor**

![image](https://github.com/karthik-2106/FULL_ADDER_SUBTRACTOR/assets/150319557/dcb521e7-c899-4e7f-a6d7-0c45949cb65d)

## Procedure:
```
Full Adder
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit.
3.The circuit consists of XOR, AND, and OR gates.
4.Compile the design, verify its functionality through simulation.
5.Implement the design on the target device and program it.

Full Subtractor**
1.Follow the same steps as for the full adder.
2.Draw the full subtractor circuit using schematic design.
3.The circuit includes XOR, AND, OR gates to perform subtraction.
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: KARTHIKEYAN M
RegisterNumber: 212223110020
```
**Full Adder**
```
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule
```
**Full Subtractor**
```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```

## RTL Schematic

![image](https://github.com/karthik-2106/FULL_ADDER_SUBTRACTOR/assets/150319557/7dbda114-2b20-4447-9a97-45fb0e337088)

## Output Timing Waveform:

**Full Adder**
![image](https://github.com/karthik-2106/FULL_ADDER_SUBTRACTOR/assets/150319557/4f8b9399-2398-47ab-8a7c-a32aa4923fed)

**Full Subtractor**
![image](https://github.com/karthik-2106/FULL_ADDER_SUBTRACTOR/assets/150319557/43b8911f-b98c-425e-be89-0692ba163d84)

## Result:
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



