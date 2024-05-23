# VSDQUADRON-MINI-INTERNSHIP

# TASK 1

 C based Lab  and RISC-V based lab Complete exact steps on your machine. Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo.

*        $ leafpad sum1ton.c &
![WhatsApp Image 2024-05-23 at 22 53 02_e0b446c8](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/7a059d42-ac76-452d-9ec4-237279f3e7de)

*     $ gcc sum1ton.c
  
*      $ ./a.out


![WhatsApp Image 2024-05-23 at 23 05 12_ad1ef314](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/fccacc4c-14f3-4af2-a267-a4050f0083f2)

*  $ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

  ![WhatsApp Image 2024-05-23 at 22 51 23_019a2bdd](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/3b2d8ef1-9f00-4b4a-a3b4-637fac83aae7)

   * $ riscv64-unknown-elf-objdump -d sum1ton.o
  
 * $ riscv64-unknown-elf-objdump -d sum1ton.o | less


![WhatsApp Image 2024-05-23 at 22 51 23_91f99058](https://github.com/Prasanna300/VSDSQUADRON-MINI-INTERNSHIP/assets/167746764/dd79a76d-4b5a-4296-bb99-32cd8b59c73a)

