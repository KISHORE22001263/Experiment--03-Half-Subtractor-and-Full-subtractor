DEVELOPED BY: KISHORE.B  

REFERENCE NO. : 22001263
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

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
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
# HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference=(a^b);
assign borrow=(~a&b);
endmodule


#FULL SUBTRACTOR:

module FULLSUBTRACTOR(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign borrow=(~a&(b^c)|(b&c));
assign difference=(a^b^c);
endmodule

# LOGIC GATES:
<img width="162" alt="210804152-d3067756-db97-49b6-81f9-859224ab815e" src="https://user-images.githubusercontent.com/121484538/211005834-9ab7b20e-60e4-4196-8e91-8e09692359af.png">
<img width="145" alt="210804186-b2fd26ff-4908-4580-b064-b49bb33c4b6b" src="https://user-images.githubusercontent.com/121484538/211005853-0807d73b-6748-4b7a-a87b-1ff66ab76ea6.png">
<img width="153" alt="210804437-c8289936-6877-4420-ac8e-b6de9497de25" src="https://user-images.githubusercontent.com/121484538/211005875-2c0761c1-f830-449d-a495-f603bbc019b4.png">
<img width="157" alt="210804204-908a6987-8a7f-449d-b33b-42b08166e0d9" src="https://user-images.githubusercontent.com/121484538/211005893-7c890340-a169-4f50-8837-ce6a74e5c0d2.png">


## Output:


## Truthtable :

- # HALF SUBTRACTOR:
![210802334-f7ee77a0-38db-4917-986a-e0c154cd17a8](https://user-images.githubusercontent.com/121484538/211006126-b8043633-d3ab-4043-915d-7fdfe47736a0.jpg)



- # FULL SUBTRACTOR:
![210806829-e8faa983-2648-444c-8290-2b1082744d52](https://user-images.githubusercontent.com/121484538/211006155-a46e33d2-0cf8-4338-8734-22ec26bafa5f.jpg)


##  RTL realization:
 # HALF SUBTRACTOR:
 
 ![Screenshot_20230105_083709](https://user-images.githubusercontent.com/121484538/211006455-c31f53dd-d285-404e-b460-f68da2ea8302.png)

 
 
 # FULL SUBTRACTOR:
 
 ![Screenshot_20230106_050155](https://user-images.githubusercontent.com/121484538/211006503-e97b1a80-4e5c-433b-894f-38a25c9493bd.png)



## Timing diagram :

# HALF SUBTRACTOR:

![Screenshot_20230105_083926](https://user-images.githubusercontent.com/121484538/211006674-8f444baf-a7e8-4c8e-81c1-be7d17684d06.png)


# FULL SUBTRACTOR:


![Screenshot_20230105_085101](https://user-images.githubusercontent.com/121484538/211006708-fd67f153-1548-4387-81e8-adb07cc0d789.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
