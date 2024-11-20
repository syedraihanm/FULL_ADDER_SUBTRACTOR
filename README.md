# EXP4:FULL ADDER AND SUBTRACTOR

Name: Syed Mohamed Raihan M

Reg no: 24900516

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

**Full Adder**



**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**

**Full Adder**

module fulladder(a,b,c,sum,carry); input a,b,c; output sum,carry; wire w1,w2,w3; assign sum=a^b^c; assign w1=a&b; assign w2=a&b; assign w3=a&b; assign carry=w1|w2|w3; endmodule

**Full Subtractor**

module fullsub(a,b,bin,diff,borr); input a,b,bin; output diff,borr; wire w1,w2,w3,w4,w5,w6; xor g1(diff,a,b,bin); and g2(w4,w2,b); and g3(w5,w1,b); and g4(w6,b,bin); or g5(borr,w4,w5,w6); endmodule



**RTL Schematic**

**Full Adder**

![WhatsApp Image 2024-11-20 at 13 38 09_9c8d1b8e](https://github.com/user-attachments/assets/ea926f66-4f4a-4eb1-88ff-c1fcf4425d43)



**Full Subtractor**

![Screenshot 2024-11-20 143600](https://github.com/user-attachments/assets/fdc04733-762a-43a9-b1eb-8a69f0782396)


**Output Timing Waveform**


**Full Adder**

![Screenshot 2024-11-20 193448](https://github.com/user-attachments/assets/bb3d99e0-bad2-4b3d-afdc-b482ae998d22)



**Full Subtractor**

![Screenshot 2024-11-20 120226](https://github.com/user-attachments/assets/065bb84b-44f8-446d-854b-da408c476587)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



