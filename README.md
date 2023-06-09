# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
```
# Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
# Developed by: Mukesh V 
# RegisterNumber: 212222230086
```
``` verilog
HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

```
``` verilog
FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Output:
### HALF ADDER:

#### LOGIC SYMBOL
![ha1](https://user-images.githubusercontent.com/118707363/229346442-0d620524-5aae-4b33-9112-3cf56981c155.png)

#### RTL
![ha2](https://user-images.githubusercontent.com/118707363/229346445-b64d4ea0-a33b-4c68-b26e-c84a65e40454.png)

#### TIMING DIAGRAM
![ha3](https://user-images.githubusercontent.com/118707363/229346453-2ab65c4f-9f9f-416e-8c8f-b31573cce61e.png)

#### TRUTH TABLE 
![ha4](https://user-images.githubusercontent.com/118707363/229346461-c5600ab3-bed6-47eb-998e-ba3b8d2f5625.jpeg)

### FULL ADDER:
#### LOGIC SYMBOL
![fa1](https://user-images.githubusercontent.com/118707363/229346472-116b5565-0faa-4f1e-926b-add2be68a145.png)

#### RTL
![fa2](https://user-images.githubusercontent.com/118707363/229346480-75e7b9f1-4eda-46af-9365-a35313ab3bd7.png)

#### TIMING DIAGRAM
![fa3](https://user-images.githubusercontent.com/118707363/229346482-d6636bdd-0e77-4fa2-835d-467625b0ba92.png)

#### TRUTH TABLE
![fa4](https://user-images.githubusercontent.com/118707363/229346484-054156c3-67e0-4d9c-a592-340f7d95743e.jpeg)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.

