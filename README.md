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

![image](https://github.com/user-attachments/assets/b09e7332-958e-4e84-9f53-7affd2357d9c)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/user-attachments/assets/ca8e58aa-8470-42ed-8d58-e2f5effe7f02)

**Figure -1 FULL SUBTRACTOR**

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER

![image](https://github.com/user-attachments/assets/4d112be1-6902-42f6-a80f-d6ffa1814c34)

FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/affd2a74-295b-48dc-b7c5-3e2de75db7d3)




**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**
```
Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Yuuvasri R
RegisterNumber: 25003422
```
**Full Adder**

```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule

```
**Full Subtractor**
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule

```

**RTL Schematic**
**Full Adder**

<img width="1920" height="809" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/5a6f0aae-bf33-4b60-b872-cba734afd4ec" />

**Full Subtractor**
<img width="1920" height="681" alt="Screenshot (103)" src="https://github.com/user-attachments/assets/6a5acbe3-6474-451e-a268-c03cc0cd6556" />


**Output Timing Waveform**
**Full Adder**

<img width="1920" height="864" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/9facdfaf-f4de-47df-8080-6ba6f76c5ea9" />

**Full Subtractor**
<img width="1920" height="904" alt="Screenshot (104)" src="https://github.com/user-attachments/assets/97f0765c-b03b-40bc-bfbf-cd0723200221" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



