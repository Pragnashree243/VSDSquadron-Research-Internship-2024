# VSDSquadron-Research-Internship-2024
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.

# Details:-
# Name - Pragnashree R
# College - B.M.S College of Engineering, Bengaluru, Karnataka

# TASK 1:-

# Installation of RISC-V toolchain using VDI. Uploading the snapshot of compiled C code and RISC-V Objdmp.

# Installation:
- Oracle Virtual machine.
  
![image](https://github.com/user-attachments/assets/21cb7746-e6fc-4363-8fbb-34f04ed8928f)

- Gedit editor.

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














