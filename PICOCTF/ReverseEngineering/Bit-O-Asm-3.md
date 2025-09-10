# Bit-O-Asm-3: Finding Value of EAX Register Now..

This challenge requires use to figure out value of the eax register at the very end of the assembly dump.

https://play.picoctf.org/practice/challenge/393?category=3&page=3

## Breakdown of the Assembly Dump 

**Hmmm, same kind of reverse engineering that we saw in Bit-O-Asm-2**

**Ooh, hint for this challenge says that "Not everything in this disassembly listing is optimal."**

**Something to think about while going through this challenge here...**

Let's break down the assembly dump now. 

<img width="407" height="277" alt="image" src="https://github.com/user-attachments/assets/aefec354-92a4-40a4-872e-bd4059960fa7" />

**<+0>:     endbr64** -> Not important here. We are not jumping to anything else

**<+4>:     push   rbp** -> RBP is pushed onto the stack 

**<+5>:     mov    rbp,rsp** -> RBP points to a memory location at the top of the stack

**<+8>:     mov    DWORD PTR [rbp-0x14],edi** -> The value of the EDI register is also stored at memory location [rbp - 20 bytes].

**<+11>:    mov    QWORD PTR [rbp-0x20],rsi** -> The value of the RSI register is also stored at memory location [rbp - 32 bytes]

**<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a** -> The value of 0x9fe1a is now stored at memory location [rbp - 12 bytes]

**<+22>:    mov    DWORD PTR [rbp-0x8],0x4** -> The value of 4 is now stored at memory location [rbp-8 bytes]

**<+29>:    mov    eax,DWORD PTR [rbp-0xc]** -> EAX is now stores the value of 0x9fe1a or 65874. 

**<+32>:    imul   eax,DWORD PTR [rbp-0x8]** -> **New Assembly instruction now seen here.. Imul (Signed Multiply) means 0x9fe1a * 0x4**
EAX now stores the value of 654874 * 4 or 2619496... 

**<+36>:    add    eax,0x1f5** -> Now, we add 501 or 0x1f5 to what is stored in the EAX register which now equals **2619997**

**<+41>:    mov    DWORD PTR [rbp-0x4],eax** -> The value of the EAX register is now stored at [rbp - 4 bytes]

**<+44>:    mov    eax,DWORD PTR [rbp-0x4]** -> EAX register is set equal to the EAX register **What a shocker..**

**<+47>:    pop    rbp** -> We are done and RBP is popped off. 

EAX register now stores the value : 2619997.. **Flag is picoctf{2619997}**

