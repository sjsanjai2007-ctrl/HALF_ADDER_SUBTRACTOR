Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

HALF ADDDER:

<img width="426" height="282" alt="outputonlinepngtools3" src="https://github.com/user-attachments/assets/6bd8953f-1666-4544-afc6-857c3ae70f60" />


HALF SUBTRACTOR:

<img width="242" height="148" alt="download" src="https://github.com/user-attachments/assets/b891f4b3-9ffa-4264-8863-05a22659edb1" />


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

**HALF ADDER:**

module exp2(sum, carry, a, b);
output sum;
output carry;
input a;
input b;
assign sum = a ^ b;
assign carry = a & b;
endmodule

**HALF SUBTRACTOR:**

module exp2(diff, borrow, a, b);
output diff;
output borrow;
input a;
input b;
assign diff = a ^ b;
assign borrow = ~a & b;
endmodule

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: SANJAI S J

RegisterNumber: 25007032

**RTL Schematic**

**HALF ADDER:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 155815" src="https://github.com/user-attachments/assets/9bb8e3d2-6892-440a-a0e9-0aa8a10c9643" />


**HALF SUBTRACTOR:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 160128" src="https://github.com/user-attachments/assets/299a9a16-ce5b-4517-ae0a-ca2f030520a6" />


**Output/TIMING Waveform**

**HALF ADDER:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 161137" src="https://github.com/user-attachments/assets/69c1e443-0100-4928-8150-b3eabab1ec15" />


**HALF SUBTRACTOR:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 161237" src="https://github.com/user-attachments/assets/7aaac347-da3a-4c0f-9806-2dff46186fa1" />


**Result:**

Program to design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming has been verified successfully.

