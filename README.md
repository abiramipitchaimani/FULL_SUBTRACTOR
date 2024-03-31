# FULL_SUBTRACTOR
## AIM:
To simulate and synthesis Half adder using Xilinx ISE.
## APPARATUS REQUIRED: 
Xilinx 14.7 Spartan6 FPGA
## PROCEDURE: 
### STEP:1 
Start the Xilinx navigator, Select and Name the New project.
### STEP:2 
Select the device family, device, package and speed. 
### STEP:3 
Select new source in the New Project and select Verilog Module as the Source type.
### STEP:4 
Type the File Name and Click Next and then finish button. Type the code and save it. 
### STEP:5 
Select the Behavioral Simulation in the Source Window and click the check syntax. 
### STEP:6 
Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.
### STEP:7 
Select the Implementation in the Sources Window and select the required file in the Processes Window.
### STEP:8 
Select Check Syntax from the Synthesize XST Process. Double Click in the Floorplan Area/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained.
### STEP:9 
In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.
### STEP:10 
Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here.
### STEP:11 
Load the Bit file into the SPARTAN 6 FPGA
### STEP:12 
On the board, by giving required input, the LEDs starts to glow light, indicating the output.

# Truth Table and Circuit Diagram
![image](https://github.com/RESMIRNAIR/FULL_SUBTRACTOR/assets/154305926/351addef-f7bb-4862-9817-616a41b4c882)
# FORMULA:
![image](https://github.com/RESMIRNAIR/FULL_SUBTRACTOR/assets/154305926/906152b8-63bc-4f70-9132-6b6b4420b22d)

![image](https://github.com/RESMIRNAIR/FULL_SUBTRACTOR/assets/154305926/7d480140-153a-4a7e-a6d2-5323c6bd4974)

# PROGRAM
```
Developed By :P.ABIRAMI
Register Number:212222060006
```
```
module full_sub(a,b,c,diff,borrow);
  input a,b,c;
  output diff,borrow;
  wire w1,w2,w3,w4,w5;
  xor g1(w3,a,b);
  xor g2(diff,c,w3);
  and g3(w2,b,w1);
  and g4(w5,w4,c);
  not g5(w1,a);
  not g6(w4,w3);
  nor g7(borrow,w5,w2);
endmodule
```
# OUTPUT:
![Screenshot 2024-03-17 204656](https://github.com/abiramipitchaimani/FULL_SUBTRACTOR/assets/163704307/3a180327-1bf0-412b-a666-ecb6afecddd8)

# RESULT:
Hence, the stimulation and synthesis of a full subractor was run successfully by using Xilinx ISE.



