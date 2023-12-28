# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Prabha.C 
RegisterNumber:212222110032

Half subtractor:
module halfsubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A^B);
assign Borrow = (~A&B);
endmodule

Full subtractor:
module fullsub(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (A^B^C);
assign Borrow = (~A&(B^C)|(B&C));
endmodule 
*/

## Output:
## Logic gates:
# FULL SUBTRACTOR:
![full subtractor](https://user-images.githubusercontent.com/120194155/235298698-ef98cf58-88f9-4fbf-ae4a-da76f96f17d9.png)
# HALF SUBTRACTOR:
![half subtractor](https://user-images.githubusercontent.com/120194155/235298711-fdab7374-c9da-45ba-bb81-2c1efdd67354.png)

## Truthtable
# FULL SUBTRACTOR:
![full sub truthtable](https://user-images.githubusercontent.com/120194155/235299003-f556801e-9005-4b08-b877-404c85a46bba.png)
# HALF SUBTRACTOR:
![half sub truth table](https://user-images.githubusercontent.com/120194155/235298749-f728792e-18a4-4a35-86fd-42cae187453f.png)

##  RTL realization
# FULL SUBTRACTOR:
![full sub RTL](https://user-images.githubusercontent.com/120194155/235298821-0041eeb0-ca0f-49dd-aae5-e8f9f2836c91.png)
# HALF SUBTRACTOR:
![half sub RTL](https://user-images.githubusercontent.com/120194155/235298831-36c6246e-3d77-4d57-a490-0ef321f7a7a1.png)

## Timing diagram 
# FULL SUBTRACTOR:
![full sub dia](https://user-images.githubusercontent.com/120194155/235298943-82da7ae4-f2ab-4fe2-bc9f-c0603a60ff5e.png)
# HALF SUBTRACTOR:
![half sub dia](https://user-images.githubusercontent.com/120194155/235298858-a423d026-a863-4262-89a5-f645a58fe3e5.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
