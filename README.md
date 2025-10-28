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

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
<img width="447" height="490" alt="image" src="https://github.com/user-attachments/assets/0fed648c-309d-4dd5-b7f6-fe57dbef900e" />
<img width="585" height="329" alt="image" src="https://github.com/user-attachments/assets/434a69f3-c61b-4f41-9967-648017af2b18" />



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:  ARAVINDP.P
RegisterNumber: 212224240015

    module full_adder_subtractor (
    input  wire a,
    input  wire b,
    input  wire cin,
    input  wire bin,
    output wire sum,
    output wire carry,
    output wire DIFF,
    output wire BO
    );
    assign sum  = a ^ b ^ cin;
    assign carry = (a & b) | (b & cin) | (a & cin);
    assign DIFF = a ^ b ^ bin;
    assign BO = (~a & b) | (b & bin) | (~a & bin);
    endmodule



**RTL Schematic**
<img width="1122" height="854" alt="image" src="https://github.com/user-attachments/assets/44a1dadd-48be-4b14-815f-6e2320674501" />


**Output Timing Waveform**
<img width="1910" height="1124" alt="image" src="https://github.com/user-attachments/assets/0631bd59-2e49-41f8-91bc-6c217572e5fa" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



