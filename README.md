# HALF_ADDER_SUBTRACTOR

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

![half adder TT](https://github.com/user-attachments/assets/56f31c10-0056-4cc8-b9d0-c340b4028644)

![half subtractor TT](https://github.com/user-attachments/assets/5fd3727a-5496-40d9-ad80-94613a414be0)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Developed by:M. LEENA SHREE RegisterNumber:25018414 */

HALF ADDER
``` 
module half_adder (
    input  wire a,
    input  wire b,
    output wire sum,
    output wire carry
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule
```

HALF  SUBTRACTOR
```
module half_subtractor (
    input  wire a,
    input  wire b,
    output wire diff,
    output wire borrow
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = (~a) & b;  // Borrow when a < b

endmodule
```

**RTL Schematic**

HALF ADDER

![half adder ](https://github.com/user-attachments/assets/1bdd7eab-d75f-4e44-9b45-df471468579f)

HALF  SUBTRACTOR

![half subtractor](https://github.com/user-attachments/assets/1c7fbc02-25df-411a-ad26-5ab523b3620b)

**Output/TIMING Waveform**

HALF ADDER

![Half adder](https://github.com/user-attachments/assets/0a445001-86cf-4b11-97ea-1e2374b6ab3e)

HALF  SUBTRACTOR

![Half subtractor wave](https://github.com/user-attachments/assets/669b6f4d-21ff-4d3f-88b0-350dd6bd244b)


**Result:**

The Half Adder and Half Subtractor circuits were constructed and their output waveforms and truth tables were verified successfully.
