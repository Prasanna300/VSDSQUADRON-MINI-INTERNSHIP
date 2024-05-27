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
3. AND r8, r1, r3
Instruction Type: R-Type
Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]
Opcode: 0110011
Funct3: 111
Funct7: 0000000
Binary: 0000000 00011 00001 111 01000 0110011
Hex: 0x0030C2B3
4. OR r9, r2, r5
Instruction Type: R-Type
Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]
Opcode: 0110011
Funct3: 110
Funct7: 0000000
Binary: 0000000 00101 00010 110 01001 0110011
Hex: 0x005142B3
5. XOR r10, r1, r4
Instruction Type: R-Type
Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]
Opcode: 0110011
Funct3: 100
Funct7: 0000000
Binary: 0000000 00100 00001 100 01010 0110011
Hex: 0x0040A2B3
6. SLT r11, r2, r4
Instruction Type: R-Type
Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]
Opcode: 0110011
Funct3: 010
Funct7: 0000000
Binary: 0000000 00100 00010 010 01011 0110011
Hex: 0x004152B3
7. ADDI r12, r4, 5
Instruction Type: I-Type
Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | imm[31:20]
Opcode: 0010011
Funct3: 000
Immediate: 000000000101
Binary: 000000000101 00100 000 01100 0010011
Hex: 0x00520293
8. SW r3, r1, 2
Instruction Type: S-Type
Format: opcode[6:0] | imm[4:0] | funct3[14:12] | rs1[19:15] | rs2[24:20] | imm[11:5]
Opcode: 0100011
Funct3: 010
Immediate: 00010 (split into 00000 and 00010)
Binary: 000000 00010 00001 010 00011 0100011
Hex: 0x0020A023
9. SRL r16, r14, r2
Instruction Type: R-Type
Format: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]
Opcode: 0110011
Funct3: 101
Funct7: 0000000
Binary: 0000000 00010 01110 101 10000 0110011
Hex: 0x00273533
10. BNE r0, r1, 20
Instruction Type: B-Type
Format: opcode[6:0] | imm[11] | imm[4:1] | funct3[14:12] | rs1[19:15] | rs2[24:20] | imm[10:5] | imm[12]
Opcode: 1100011
Funct3: 001
Immediate: 00010100 (split into 00000, 0001, 010, and 0)
Binary: 0000000 00101 00000 001 00001 1100011
Hex: 0x01400063
