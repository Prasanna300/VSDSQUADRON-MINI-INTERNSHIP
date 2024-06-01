# VSDQUADRON-MINI-INTERNSHIP

# TASK 1

 C based Lab  and RISC-V based lab Complete exact steps on your machine. Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo.
 WE can the run these commands using VDI too which has preinstalled softwares in virtual box.
Give command to open the C program in terminal

*        $ leafpad sum1ton.c &
![WhatsApp Image 2024-05-23 at 22 53 02_e0b446c8](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/7a059d42-ac76-452d-9ec4-237279f3e7de)

*     $ gcc sum1ton.c
  
*      $ ./a.out


![WhatsApp Image 2024-05-23 at 23 05 12_ad1ef314](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/fccacc4c-14f3-4af2-a267-a4050f0083f2)

*  $ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

  ![WhatsApp Image 2024-05-23 at 22 51 23_019a2bdd](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/3b2d8ef1-9f00-4b4a-a3b4-637fac83aae7)

   *     $ riscv64-unknown-elf-objdump -d sum1ton.o
  
 *     $ riscv64-unknown-elf-objdump -d sum1ton.o | less


![WhatsApp Image 2024-05-23 at 22 51 23_91f99058](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/dd79a76d-4b5a-4296-bb99-32cd8b59c73a)




# TASK - 2



RISCV INSTRUCTIONS 

In RISC-V, an instruction is a binary-encoded operation that a processor can execute. Each instruction specifies an operation and the operands involved. RISC-V instructions are designed to be simple and efficient, following the principles of Reduced Instruction Set Computing (RISC).

MAIN COMPONENTS OF RISCV INSTRUCTIONS:

Opcode: Specifies the operation to be performed.
Operands: The data to be used in the operation, which can include registers, immediate values, or memory addresses.
Funct3 and Funct7: These fields provide additional specification for the instruction, helping to distinguish between different operations that share the same opcode.


INSTRUCTION TYPES:

1. R-Type (Register) Instructions
   
Used for arithmetic and logical operations.
 *      $Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

2. I-Type (Immediate) Instructions
   
Used for arithmetic operations with immediate values and load instructions.
*      $Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | imm[31:20]

3. S-Type (Store) Instructions
   
Used for store operations to memory.
*      $Format: opcode[6:0] | imm[4:0] | funct3[14:12] | rs1[19:15] | rs2[24:20] | imm[11:5]

4. B-Type (Branch) Instructions
   
Used for conditional branch operations.
*     $Format: opcode[6:0] | imm[11] | imm[4:1] | funct3[14:12] | rs1[19:15] | rs2[24:20] | imm[10:5] | imm[12]

  5. U-Type (Upper Immediate) Instructions
     
Used for instructions that build 32-bit constants and for address calculation.
*      $Format: opcode[6:0] | rd[11:7] | imm[31:12]

  6. J-Type (Jump) Instructions

Used for jump operations.
*      $Format: opcode[6:0] | rd[11:7] | imm[20|10:1|11|19:12]

SOME  RISCV INSTRUCTIONS :

add: Adds two registers.
addi: Adds a register and an immediate value.
sub: Subtracts two registers.
lw: Loads a word from memory to a register.
sw: Stores a word from a register to memory.
beq: Branches if two registers are equal.
bne: Branches if two registers are not equal.
jal: Jumps and links, storing the return address.
jalr: Jumps and links using a register.




ADD r6, r2, r1


SUB r7, r1, r2

AND r8, r1, r3

OR r9, r2, r5

XOR r10, r1, r4

SLT r11, r2, r4

ADDI r12, r4, 5

SW r3, r1, 2

SRL r16, r14, r2

BNE r0, r1, 20

BEQ r0, r0, 15

LW r13, r1, 2

SLL r15, r1, r2


FOR THESS INSRUCTIONS
1. ADD r6, r2, r1
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 000

Funct7: 0000000

Binary: 0000000 00001 00010 000 00110 0110011

Hex: 0x002102B3



2. SUB r7, r1, r2
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 000

Funct7: 0100000

Binary: 0100000 00010 00001 000 00111 0110011

Hex: 0x402081B3


4. AND r8, r1, r3
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 111

Funct7: 0000000

Binary: 0000000 00011 00001 111 01000 0110011

Hex: 0x0030C2B3


5. OR r9, r2, r5
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 110

Funct7: 0000000

Binary: 0000000 00101 00010 110 01001 0110011

Hex: 0x005142B3


6. XOR r10, r1, r4 
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 100

Funct7: 0000000

Binary: 0000000 00100 00001 100 01010 0110011

Hex: 0x0040A2B3


7. SLT r11, r2, r4
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 010

Funct7: 0000000

Binary: 0000000 00100 00010 010 01011 0110011

Hex: 0x004152B3


8. ADDI r12, r4, 5
Instruction Type: I-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | imm[31:20]

Opcode: 0010011

Funct3: 000

Immediate: 000000000101

Binary: 000000000101 00100 000 01100 0010011

Hex: 0x00520293


9. SW r3, r1, 2
Instruction Type: S-Type


Format: opcode[6:0] | imm[4:0] | funct3[14:12] | rs1[19:15] | rs2[24:20] | imm[11:5]

Opcode: 0100011

Funct3: 010

Immediate: 00010 (split into 00000 and 00010)


Binary: 000000 00010 00001 010 00011 0100010

Hex: 0x0020A023


10. SRL r16, r14, r2
Instruction Type: R-Type


Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

Opcode: 0110011

Funct3: 101

Funct7: 0000000

Binary: 0000000 00010 01110 101 10000 0110011

Hex: 0x00273533

# TASK 3

IVERILOG:-Icarus Verilog, commonly referred to as IVerilog, is an open-source Verilog simulation and synthesis tool. It supports a wide range of Verilog standards and is used for designing and testing digital circuits

GTKWAVE:- GTKWave is an open-source waveform viewer used for visualizing simulation results from digital circuit designs. It is commonly used in conjunction with simulation tools like Icarus Verilog
1. STEP 1 : To install verilog

   *      $ sudo apt install iverilog
   ![WhatsApp Image 2024-05-31 at 22 52 51_ebeaf265](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/1d9e4cc9-b8c1-48ab-be5b-911335533d6a)

2. STEP 2: TO INSTALL GTKWAVE
   *     $sudo apt install iverilog gtkwave
     
  ![WhatsApp Image 2024-05-31 at 22 55 38_aea4ab17](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/03f7e19b-0902-4fe9-a071-97d3d8256e79)

  3. STEP 3 : cloning
*      $git clone https://github.com/prasanna300/vsdsquadron-mini-internship
*      $ cd vsdsquadron-mini-internship
  ![WhatsApp Image 2024-05-31 at 22 58 40_11eb65db](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/b39a658f-aa91-4d5d-95cd-74637bda90ce)

4. STEP 4: SIMULATION
   *     $ iverilog -o vsdsquadron-mini-internship prasanna_rv32i.v prasanna_rv32i_tb.v
*      $ ./vsdsquadron-mini-internship
  **![WhatsApp Image 2024-05-31 at 23 02 08_05c94f69](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/c8964939-154f-4953-9803-07d98fbd2a8c)
**

5.STEP 5: WAVEFORM
*     $gtkwave prasanna_rv32i.vcd
![WhatsApp Image 2024-05-31 at 23 02 08_847af15d](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/3a2c250b-6ed3-4287-97fb-6498dd288ba3)


FOLLOWING INSTRUCTIONS:

1.ADD r6, r2, r1

2.SUB r7, r1, r2

3.AND r8, r1, r3

4.OR r9, r2, r5


5.XOR r10, r1, r4




6.SLT r11, r2, r4

7.ADDI r12, r4, 5

8.SW r3, r1, 2

9.BEQ r0, r0, 15

*     $1..ADD r6, r2, r1
  ![WhatsApp Image 2024-05-31 at 23 06 56_85388c6c](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/093f8c68-6345-4fc8-8ff5-9f232fcb4fa9)
  
*     $2.SUB r7, r1, r2
  ![WhatsApp Image 2024-05-31 at 23 07 55_d559889f](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/45fced2e-dfb5-49f3-9781-81c86d4623ea)

*     $3.AND r8, r1, r3
  ![WhatsApp Image 2024-05-31 at 23 09 40_85ba2e1c](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/336475e8-a4d0-4caf-bdfd-1cbe8e093bd1)

*      $4.OR r9, r2, r5
*  ![WhatsApp Image 2024-05-31 at 23 11 30_28aa124a](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/530660fe-747b-40c5-a13b-6ce6e6c57f79)

*     $5.XOR r10, r1, r4

![WhatsApp Image 2024-05-31 at 23 13 21_04791019](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/6578aeea-5e01-4ee7-8d33-741ae22172dc)

*      $6.SLT r11, r2, r4
![WhatsApp Image 2024-05-31 at 23 14 05_63fdc7b5](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/d7914001-099f-4a7f-9790-998e1a1d8c8e)

  *      $7.ADDI r12, r4, 5
   ![WhatsApp Image 2024-05-31 at 23 14 51_3ab4b444](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/a59d0ce4-236b-4f22-8dd0-5fb11ce5f341)

*     $8.SW r3, r1, 2
* ![WhatsApp Image 2024-05-31 at 23 16 00_0c27c5ae](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/c51ad0d6-fd91-482b-873f-16eb6d321da4)
*      $9.BEQ r0, r0, 15
 ![WhatsApp Image 2024-05-31 at 23 17 16_e51090d2](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/cee40666-8ae2-4a0d-ae03-c5c9a416821c)

   



