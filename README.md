# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
##1.Hardware – PCs, Cyclone II , USB flasher
##2.Software – Quartus prime
## Theory:
# Introduction:
1.Logic gates are the basic building blocks of any digital system.

2.Logic gates are electronic circuits having one or more than one input and only one output.

3.The relationship between the input and the output is based on a certain logic.

4.Based on this, logic gates are named as - AND gate,OR gate,NOT gate,NAND gate,NOR gate,XOR gate,XNOR gate

5.AND gate: The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

6.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B

7.NOT gate The NOT gate is an electronic circuit that produces an inverted version of the input at its output. It is also known as an inverter. If the input variable is A, the inverted output is known as NOT A. This is also shown as A' or A with a bar over the top, as shown at the outputs. Y= A'

8.NAND gate This is a NOT-AND gate which is equal to an AND gate followed by a NOT gate. The outputs of all NAND gates are high if any of the inputs are low. The symbol is an AND gate with a small circle on the output. The small circle represents inversion. Y= (AB)’

9.NOR gate This is a NOT-OR gate which is equal to an OR gate followed by a NOT gate. The outputs of all NOR gates are low if any of the inputs are high. The symbol is an OR gate with a small circle on the output. The small circle represents inversion. Y= (A+B)’

Ex-OR gate The 'Exclusive-OR' gate is a circuit which will give a high output if either, but not both of its two inputs are high. An encircled plus sign (⊕) is used to show the Ex-OR operation. Y= A⊕B

Ex-NOR gate The 'Exclusive-NOR' gate circuit does the opposite to the EX-OR gate. It will give a low output if either, but not both of its two inputs are high. The symbol is an EX-OR gate with a small circle on the output. The small circle represents inversion. Y= A⊕B
## Procedure:
1.Connect the supply (+5V) to the circuit.
2.Switch ON the main switch.
3.Press the switches for inputs “A” and “B”.
4.The switch is ON state when 1 is pressed.
5.The switch is OFF state when 0 is pressed.
6.If the output is 1, then the bulb glows.
7.Check all the gates following the same procedure.
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Anandhamoorthy.k
RegisterNumber: 212222100004

module EX2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire X1,X2,X3,X4,X5;
assign X1=(~A)&(~B)&(~C)&(~D);
assign X2=(A)&(~C)&(~D);
assign X3=(~B)&(C)&(~D);
assign X4=(~A)&(B)&(C)&(D);
assign X5=(B)&(~C)&(D);
assign F1=X1|X2|X3|X4|X5;
endmodule
```
## Truth Table:
![Screenshot 2023-09-12 235611](https://github.com/AnandhamoorthyKarthikeyan/Experiment--02-Implementation-of-combinational-logic-/assets/119475998/97f37b87-46ba-4dbb-8b3e-edffe81ae039)
## RTL realization:
![Screenshot 2023-09-12 235724](https://github.com/AnandhamoorthyKarthikeyan/Experiment--02-Implementation-of-combinational-logic-/assets/119475998/27dd8160-848d-43ac-aef1-c128c1b6a845)
## Output:
![Screenshot 2023-08-26 094619](https://github.com/AnandhamoorthyKarthikeyan/Experiment--02-Implementation-of-combinational-logic-/assets/119475998/3bb7671d-e767-4a81-8c51-783a0174a55c)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
