# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Using Nand Operation:
module expfo(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

Using Nor Operation:
module expft(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
assign F = ~S;
endmodule

Developed by: Surendhar A
RegisterNumber:  22009022
*/
## RTL realization

## Output:
## RTL
![Screenshot_20230116_015419](https://user-images.githubusercontent.com/118352907/212631441-f54dc084-a0c8-4a88-887f-1c207200c58c.png)
![Screenshot_20230116_020926](https://user-images.githubusercontent.com/118352907/212634407-1fb33fa6-d1ea-4b74-8737-2f9bbdc62073.png)

Truth table:
![Screenshot_20230116_020057](https://user-images.githubusercontent.com/118352907/212632698-f008c372-f7ff-46a9-b5bb-8a8ced078ac9.png)
![Screenshot_20230116_020142](https://user-images.githubusercontent.com/118352907/212632788-8eccb794-ff7c-43e8-8691-f91dd2a81986.png)

## Timing Diagram
![Screenshot_20230116_020531](https://user-images.githubusercontent.com/118352907/212633613-ddf9058f-a4f8-421f-80e9-0591126983c9.png)
![Screenshot_20230116_021254](https://user-images.githubusercontent.com/118352907/212634986-12a40c87-82be-4dc3-924a-cd21efcc7f1c.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
