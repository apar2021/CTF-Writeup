# Bit-O-Asm-2 : Reverse Engineering 

This challenge requires use to figure out value of the eax register at the very end of the function. 

https://play.picoctf.org/practice/challenge/392?category=3&page=3

## Break Down of the Assembly Dump 

<img width="382" height="198" alt="image" src="https://github.com/user-attachments/assets/60dfcd79-3c0e-4a0e-8ce8-d18f6ee45c05" />

In this scenario, we are given an assembly dump. 

However, we have to find the value of eax register at the very end of the program execution. 

From a very quick look at the dump, we can see that it is written in Intel syntax for x86-64 architecture. 
**<+0>:     endbr64**  ->  This line is an indirect branch. **Not very important**

**<+4>:     push   rbp**  -> This line moves rbp into stack and starts us off. 

**<+5>:     mov    rbp,rsp** -> RBP register points to the top of the stack (RSP is a register that points to the top of the stack)

**<+8>:     mov    DWORD PTR [rbp-0x14],edi** -> The value of the EDI register is also stored at memory location [rbp - 20 bytes]. 

**<+11>:    mov    QWORD PTR [rbp-0x20],rsi** -> The value of the RSI register is also stored at memory location [rbp - 32 bytes] 

**<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a** -> The value 0x9fe1a is now stored at memory location [rbp-0x4]

**<+22>:    mov    eax,DWORD PTR [rbp-0x4]** -> EAX register now stores the value located at the memory location [rbp-0x4]

**Hmmm, we might be done here.. Let's see..**

**<+25>:    pop    rbp** -> We have now reached the end of the program... 

**Let's see the value of EAX register. Okay, it stores hexadecimal 0x9fe1a which is decimal value: 654874. picoctf{654874} is the answer**

