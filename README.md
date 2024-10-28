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
1.) The C Code to find the sum of n numbers is the same code as used in Task 1.

![WhatsApp Image 2024-10-28 at 19 50 53_f950d1c7](https://github.com/user-attachments/assets/343cb4bc-f86e-468d-8e28-3917231c8d9b)


2.) Output using the RISC-V simulator.

![WhatsApp Image 2024-10-28 at 19 50 53_c40fed3f](https://github.com/user-attachments/assets/497c92c2-59ca-49eb-84c6-b91cd79c2517)


3.) Confirming the same using Spike 

![WhatsApp Image 2024-10-28 at 19 50 53_1744290e](https://github.com/user-attachments/assets/0c0261e0-a81a-470e-be3b-b8fdf751e66d)


This confirms that all the three methods give the same output.

# B. Write a simple C program for any simple application and compile with RISC-V GCC/SPIKE.














