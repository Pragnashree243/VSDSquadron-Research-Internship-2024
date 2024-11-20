# VSDSquadron-Research-Internship-2024
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.

# Details:-
Name - Pragnashree R

College - B.M.S College of Engineering, Bengaluru, Karnataka

GitHub link - https://github.com/Pragnashree243/VSDSquadron-Research-Internship-2024.git

# TASK 1:-

# Installation of RISC-V toolchain using VDI. Uploading the snapshot of compiled C code and RISC-V Objdmp.

# Installation:
A. Oracle Virtual machine.
  
![image](https://github.com/user-attachments/assets/21cb7746-e6fc-4363-8fbb-34f04ed8928f)

B. Gedit editor.

![image](https://github.com/user-attachments/assets/adab033c-001e-4c47-9888-78349677231a)

# Steps:
1.) Open Gedit and write the C code to find the sum of n numbers.

![Screenshot 2024-10-23 090141](https://github.com/user-attachments/assets/fcfc198a-404e-4c55-be0d-7c49b32ed1d9)

2.) Compile the above code using gcc and get the output.

![Screenshot 2024-10-23 090441](https://github.com/user-attachments/assets/4f45de72-635c-4d57-81c4-25feb0c44e11)

3.) Now, compile and run the same code using the RISC-V Simulator and search for main using the command: "riscv64-unknown-elf-objdump -d sum.o | less" and then type out "/main".

![image](https://github.com/user-attachments/assets/4a6963d1-359d-4fe8-b52c-248cf67cf203)

4.) Changing it from O1 to Ofast.

![image](https://github.com/user-attachments/assets/300dda3d-c4d4-4cd1-be49-d681e7101f3f)

5.) Search for main usin the commands: "riscv64-unknown-elf-objdump -d sum.o | less" and then type out "/main".

![image](https://github.com/user-attachments/assets/4e0c5aec-e313-4f9a-818b-e40158f97dc8)

# TASK 2:-

# Performing SPIKE Simulation and Observation with -O1 anf -Ofast. Debugging a simple C code with Interactive Debugging Mode using Spike and Uploading snapshot of compiled C code, RISC-V Objdmp.

# A. SPIKE Simulation and Observation with -O1 anf -Ofast. Upload snapshot of compiled C code, RISC-V Objdmp.

# What is SPIKE in RISC-V?

- A RISC-V ISA is a simulator, enabling the testing and analysis of RISC-V programs without the need for actual hardware.

- Spike is a free, open-source C++ simulator for the RISC-V ISA that models a RISC-V core and cache system. It can be used to run programs and a Linux kernel, and can be a starting point for running software on a RISC-V target.

# What is pk (Proxy Kernel)?

- The RISC-V Proxy Kernel, pk , is a lightweight application execution environment that can host statically-linked RISC-V ELF binaries.
  
- A Proxy Kernel in the RISC-V ecosystem simplifies the interaction between complex hardware and the software running on it, making it easier to manage, test, and develop software and hardware projects.     

# STEPS:
1.) The C Code to find the sum of n numbers is the same code as used in Task 1. Following the instructions as shown below in the snapshot, we can observe the same output when 'gcc' command or 'spike' command is used.

![Screenshot 2024-10-29 122735](https://github.com/user-attachments/assets/8d75a4b5-b431-4165-ab6e-ce52164f0501)

![Screenshot 2024-10-29 133317](https://github.com/user-attachments/assets/cee810d3-e4da-409d-90e6-bacb17bf0d8b)


2.) Enter the below given instructions and debug using SPIKE:

- riscv64-unknown-elf-objdump -d sum1ton.o | less
  ( here -d is given for Debug)

![Screenshot 2024-10-29 133549](https://github.com/user-attachments/assets/6cc23c7b-2f7b-473f-ae8d-f40b7e7c3119)

![WhatsApp Image 2024-10-29 at 14 00 56_33507c4b](https://github.com/user-attachments/assets/d9d4f619-e706-4705-9bf1-3dc4ee1dbd93)


# B. Write a simple C program for any simple application and compile with RISC-V GCC/SPIKE.


# TASK 3:-

# RISC-V Instruction Types (R,I,S,B,U,J):

The RISC-V instruction set architecture (ISA) defines several types of instructions, each with a specific format. Below is a summary of the main instruction types:

![image](https://github.com/user-attachments/assets/e9b6a795-6e82-4ea6-9feb-129a8dc1bc9b)


1.) R-Type (Register-Register):

- Purpose: Used for operations that involve two source registers and one destination register.

- Fields:

- opcode: Operation code
- rd: Destination register
- func3: Function modifier
- rs1: Source register 1
- rs2: Source register 2
- func7: Function modifier (additional)

- Example: add x1, x2, x3

2.) I-Type (Immediate):

- Purpose: Used for operations with one source register and an immediate value, including loads.

- Fields:

- opcode: Operation code
- rd: Destination register
- func3: Function modifier
- rs1: Source register
- imm[11:0]: Immediate value

- Example: addi x1, x2, 10

3.) S-Type (Store):

- Purpose: Used for store instructions, which write a register's value to memory.

- Fields:

- opcode: Operation code
- imm[11:5]: Immediate value (upper 7 bits)
- func3: Function modifier
- rs1: Source register (base address)
- rs2: Source register (data to store)
- imm[4:0]: Immediate value (lower 5 bits)
  
- Example: sw x2, 0(x1)

4.) B-Type (Branch):

- Purpose: Used for conditional branch instructions.

- Fields:

- opcode: Operation code
- imm[12]: Immediate value (bit 12)
- imm[10:5]: Immediate value (bits 10 to 5)
- func3: Function modifier
- rs1: Source register 1
- rs2: Source register 2
- imm[4:1]: Immediate value (bits 4 to 1)
- imm[11]: Immediate value (bit 11)
  
- Example: beq x1, x2, label

5.) U-Type (Upper Immediate):

- Purpose: Used for instructions that operate with a large immediate value.

- Fields:

- opcode: Operation code
- rd: Destination register
- imm[31:12]: Immediate value
  
- Example: lui x1, 0x10000

6.) J-Type (Jump):

- Purpose: Used for jump instructions with a large immediate value.

- Fields:

- opcode: Operation code
- rd: Destination register
- imm[20]: Immediate value (bit 20)
- imm[10:1]: Immediate value (bits 10 to 1)
- imm[11]: Immediate value (bit 11)
- imm[19:12]: Immediate value (bits 19 to 12)
- Example: jal x1, label

# 32-bit Instruction Codes in RISC-V Instruction Type Format for 15 Unique Instructions:

1.) addi x1, x2, 10

- Instruction Format: I-type
- Binary Encoding: 000000000010 00010 000 00001 0010011
- 32-bit Instruction Code: 0x00210093

2.) li x5, 0x0

Instruction Format: I-type (using addi x5, x0, 0x0)
Binary Encoding: 000000000000 00000 000 00101 0010011
32-bit Instruction Code: 0x00000293

3.) lui x10, 0x20000

- Instruction Format: U-type
- Binary Encoding: 00100000000000000000 01010 0110111
- 32-bit Instruction Code: 0x20000537

4.) mv x1, x2

- Instruction Format: I-type (using addi x1, x2, 0)
- Binary Encoding: 000000000000 00010 000 00001 0010011
- 32-bit Instruction Code: 0x00010093

5.) sw x5, 0(x10)

- Instruction Format: S-type
- Binary Encoding: 0000000 00101 01010 010 00000 0100011
- 32-bit Instruction Code: 0x0050a023
  
6.) lw x5, 0(x10)

- Instruction Format: I-type
- Binary Encoding: 000000000000 01010 010 00101 0000011
- 32-bit Instruction Code: 0x0000a283

7.)jal x0, 0x100

- Instruction Format: J-type
- Binary Encoding: 00000000000100000000 00000 1101111
- 32-bit Instruction Code: 0x0000086f

8.) beq x1, x2, label

- Instruction Format: B-type (assuming offset is 0x4)
- Binary Encoding: 000000 00010 00001 000 00010 1100011
- 32-bit Instruction Code: 0x00210063

9.) bne x1, x3, label

- Instruction Format: B-type (assuming offset is 0x4)
- Binary Encoding: 000000 00011 00001 001 00010 1100011
- 32-bit Instruction Code: 0x00310063

10.) slli x5, x1, 1

- Instruction Format: I-type
- Binary Encoding: 0000000 00001 00101 001 00001 0010011
- 32-bit Instruction Code: 0x00109093

11.) srli x6, x2, 2

- Instruction Format: I-type
- Binary Encoding: 0000000 00010 00110 101 00010 0010011
- 32-bit Instruction Code: 0x0022b093

12.) and x3, x4, x5

- Instruction Format: R-type
- Binary Encoding: 0000000 00101 00100 111 00011 0110011
- 32-bit Instruction Code: 0x005201b3

13.) or x2, x3, x4

- Instruction Format: R-type
- Binary Encoding: 0000000 00100 00011 110 00010 0110011
- 32-bit Instruction Code: 0x004181b3

14.) sub x3, x5, x2

- Instruction Format: R-type
- Binary Encoding: 0100000 00010 00101 000 00011 0110011
- 32-bit Instruction Code: 0x402282b3

15.) xor x1, x2, x3

- Instruction Format: R-type
- Binary Encoding: 0000000 00011 00010 100 00001 0110011
- 32-bit Instruction Code: 0x003100b3

# TASK 4:-

# By making use of RISC-V Core: Verilog Netlist and Testbench, perform an experiment of Functional Simulation and observe the waveforms

NOTE: Since the designing of RISCV Architecture and writing it's testbench is not the part of this Research Internship, so we will use the Verilog Code and Testbench of RISCV that has already been designed. The reference GitHub repository is : iiitb_rv32i          link 

# Steps to perform functional simulation of RISCV:

# GTKWAVE Generation Process:

Follow the steps given below to generate the waveform using Verilog code and GTKWAVE.

# 1.) Clone the Repository.

Clone the RISC-V Verilog repository using the 'git clone' command.

git clone https://github.com/vinayrayapati/rv321        link

# 2.) Navigate to the Cloned Directory.

Change the directory to the cloned repository.

cd rv321

# 3.) Compile the Verilog Code and Testbench.

Run the following iverilog command to compile the Verilog code and testbench.

'iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v'

# 4.) Simulate the Verilog Code.

After compiling, simulate the Verilog code by running the compiled file.

'./iiitb_rv321'

![image](https://github.com/user-attachments/assets/de532545-1035-4bf0-8d33-11eb84ab2bd1)


# 5.) Open the Waveform in GTKWAVE.

Once the simulation generates the .vcd (Value Change Dump) file, you can visualize the waveform in GTKWAVE.

'gtkwave iiitb_rv321.vcd'

It will open the new window of GTKWAVE.

![image](https://github.com/user-attachments/assets/3dfff2e2-e29e-4ac7-a74d-99791048a8e7)


Tap the 'iiitb_rv32i_tb' in the 'SST' section.

![image](https://github.com/user-attachments/assets/3cbd47e0-d7c9-4465-8bc2-f45b032b6eb9)


Now, drag the command in the same way presented under 'time' section.

![image](https://github.com/user-attachments/assets/c3933625-84aa-43fe-aae0-551c5036cd66)


Select the instructions from EX_MEM_IR[31:0] to present the instructions used in Task 3 and Analysing the Output Waveform of various instructions that we have covered in TASK-3.

# Instruction 1 : ADD r1, r1, r2

![values stored in two different registe](https://github.com/user-attachments/assets/bc020bf1-4840-4837-9d89-38c06cec98bc)


# Instruction 2 : SUB r3, r1, r2 

![Values stored in two different register](https://github.com/user-attachments/assets/1ae337fd-7d59-45a5-b357-3289e1235056)


# Instruction 3 : AND r2, r1, r3

![Untitled design](https://github.com/user-attachments/assets/0d56993f-a4b1-49dc-84a8-72ac4f1ea19c)


# Instruction 4 : OR r8, r2, r5 

![Untitled design (1)](https://github.com/user-attachments/assets/32ef522d-dfd1-4dca-b265-659528c0fd69)


# Instruction 5 : XOR r8, r1, r4 

![Your paragraph text](https://github.com/user-attachments/assets/5fb26807-d7c6-4d95-bbd6-855fbd14c0e3)


# Instruction 6 : SLL r15, r11, r2 

![Your paragraph text (1)](https://github.com/user-attachments/assets/f0aeb7ce-a088-43dd-a54c-5e4887a4af6c)


# Instruction 7 : SLT r10, r2, r4 

![32 bits instruction](https://github.com/user-attachments/assets/edc69fdb-279c-430b-84a8-8279564fb6e4)

  
To conclude : The output waveform for the list of instructions are obtained in GTKWAVE.

# TASK 5 :-

# Bluetooth Automated Smart Access Using VSDSquadron Mini RISC-V Development Board 

# Project Overview :

In an era where technology is intricately woven into the fabric of our everyday existence, the idea of a smart home has transitioned from science fiction to a practical reality. At the heart of this evolution is the “Bluetooth Automated Smart Access” system, a perfect fusion of ease, security, and cutting-edge technology. By harnessing the power and capabilities of a VSD Squadron Mini board, a Bluetooth module, and a servo motor, this innovation offers functional solutions to common challenges, redefining how we engage with and control our home environments.

Bluetooth automated smart access can be utilized in a wide range of applications, from controlling water taps to managing lighting and appliances, smart door and security applications and for enhancing efficiency and simplifying everyday tasks across diverse environments.

This project presents a groundbreaking solution for controlling and monitoring door access, utilizing a combination of a servo motor, Bluetooth module, push-button, and onboard LED. The core functionality of the system revolves around its ability to respond to Bluetooth commands, which activate a precise open-close mechanism. Upon receiving a signal, the Bluetooth module prompts the VSD Squadron Mini to engage the servo motor, triggering the door’s movement. By integrating this technology, the system offers a seamless, hands-free experience that enhances both security and convenience, making access control simpler and more efficient.

With the ability to be controlled directly from a smartphone via Bluetooth, this system offers intuitive and convenient access management. The onboard LED serves as a visual indicator, ensuring users receive clear feedback on the system’s status. This project highlights the powerful role of IoT technology in revolutionizing home security and automation, providing a seamless blend of efficiency and ease of use.

# Components Required for the project :

1.) VSD Squadron Mini RISC-V board

2.) Bluetooth HC-05 Module

3.) Servo Motors (SG90)

4.) Micro USB Cable

5.) Jumper Wires

THe VSD Squadron Mini RISC-V board is powered by CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set, optimized for high-performance computing with support for 2-level interrupt nesting and supports 24MHz system main frequency in the product function. Bluetooth HC-05 Module (Pins PD6, PD7, PC7, GND, 3.3V) enables wireless communication between the system and the user’s smartphone for remote control and the Bluetooth module’s State pin indicates connection status. Servo Motor (Pin PC6) acts as the locking mechanism, which is controlled by the microcontroller. The Onboard LED displays the system status, indicating the locked or unlocked states. The jumper wires are used to connect the different parts of a circuit. These wires help in easily linking the VSD Squadron Mini RISC-V board, Bluetooth HC-05 Module and the Servo Motor.

# Circuit Connection for Bluetooth Automated Smart Access :

In this circuit setup, the VSD Squadron Mini controls the servo motor using the PC6 pin for the servo signal, while the motor’s power is supplied through 5V for VCC and grounded via GND. The Bluetooth module communicates with the microcontroller through its PD6 pin for RXD and PD7 for TXD, with PD7 connected to a 5V logic level. The Bluetooth module is powered by the 3.3V pin, which is connected to the microcontroller’s 3.3V output, and grounded via the GND pin. The PC7 pin from the microcontroller is used to monitor the Bluetooth State pin, which indicates the connection status of the Bluetooth module. Lastly, the LED_BUILTIN onboard LED is used for status indication, providing visual feedback on the system’s state.

# Table for Pin connection :

![Screenshot 2024-11-16 163056](https://github.com/user-attachments/assets/7391e659-fd79-4bd6-899d-05c52be0e69e)

# Pinout Diagram for Bluetooth Automated Smart Access :

![image](https://github.com/user-attachments/assets/2966ee17-8251-4750-9ca6-b5e6924cf9eb)

# TASK 6 :-

# Demonstration Of Project :

# Working Code : 

![Screenshot 2024-11-19 135135](https://github.com/user-attachments/assets/e780555b-9ab8-4a7d-a49a-fce5398d5871)

![Screenshot 2024-11-19 135203](https://github.com/user-attachments/assets/0c875f9f-9498-4bd8-904b-06cbd7f2705d)

![Screenshot 2024-11-19 135235](https://github.com/user-attachments/assets/bb90359b-eb86-4e91-91d3-9d888607180b)

![Screenshot 2024-11-19 135251](https://github.com/user-attachments/assets/24553766-3635-4648-965e-3d9fc30ed8c9)

# Project Image :

![Screenshot 2024-11-19 221519](https://github.com/user-attachments/assets/41ddcd5f-8a82-42d7-8543-fb5b075df270)

# Project Video :

https://drive.google.com/file/d/1qGuSV-Rf6FaNDQuBi1085Og8bacgfmGA/view?usp=drivesdk

# Conclusion :

This project demonstrates the integration of Bluetooth HC-05 Module with the VSDSquadron RISC-V MIni board to control the smart doors and alert the user through the onboard LED indicator. 
This setup showcases how the RISC-V architecture and embedded systems handle real-world home security making the system user-friendly and reliable.

# ACKNOWLEDGEMENT

I would like to express my sincere gratitude to VLSI System Design for providing me with the opportunity to intern with them. I would also like to express my special thanks to my mentor Mr.Kunal Ghosh for guiding and supporting and clearing any doubts that I had throughout this internship. This internship has been an invaluable experience, allowing me to learn deeply about the VSD Squadron RISC-V Mini Board and significantly strengthened my understanding of ARM (Advanced Risc Machine) course that I had learnt in my 4th semester of engineering. I was able to apply what I had learnt in the classroom to the tasks that we were assigned, along with learning many new concepts on digital chip design by delving deep into Embedded systems, RISC-V architecture and VLSI design under the guidance of dedicated mentors.

I am thankful for the support and knowledge imparted to me during this journey. I look forward to applying the lessons learned here in my continued pursuit of excellence in engineering.

