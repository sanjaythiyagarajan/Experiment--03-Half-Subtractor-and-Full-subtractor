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

STEP 1: Use module project name(input,output) to start the Verilog programmming.

STEP 2: Assign inputs and outputs using the word input and output respectively.

STEP 3: Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

STEP 4: Use each output to represnt onre for differnce and the other for borrow.

STEP 5: End the verilog program using keyword endmodule

## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SANJAY T
RegisterNumber: 212222110039 

```
## HALF SUBTRACTOR
module ex4(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule

## FULL SUBTRACTOR
module exp04(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference = (a^b^bin);
assign borrow =(~a&b)|(~(a^b)&bin);
endmodule
*/
```
## Output:

## Truthtable

HALF SUBTRACTOR

![WhatsApp Image 2023-09-08 at 09 25 20](https://github.com/sanjaythiyagarajan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119409242/3f8e40f9-70eb-498a-b870-b00bb5dab7a3)


FULL SUBTRACTOR

![WhatsApp Image 2023-09-08 at 09 25 20](https://github.com/sanjaythiyagarajan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119409242/2073c7e8-522e-4375-b878-221d9bf9381d)


##  RTL realization

HALF SUBTRACTOR

 ![half sub 004](https://github.com/sanjaythiyagarajan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119409242/0c1f62f7-89b0-42c7-917a-32bb0a9b6298)


FULL SUBTRACTOR

![full sub 004 rtl](https://github.com/sanjaythiyagarajan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119409242/f354c942-3836-49d3-ae71-980fda2fe386)


## Timing diagram 

HALF SUBTRACTOR

![half sub  004](https://github.com/sanjaythiyagarajan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119409242/3b1cdf11-7a54-4e55-b249-51179d0a6010)


FULL SUBTRACTOR

![full sub 004](https://github.com/sanjaythiyagarajan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119409242/c6b0d7af-8cf0-4506-b288-b74210200237)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
