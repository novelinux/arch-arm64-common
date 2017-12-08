# ARMV8

ARMv7与ARMv8的简要对比：
CPU	Core Version	Pipeline	DMIPS/MHz	Physical Memory Addresses
Cortex A7	ARMv7	In-Order	1.9	LPAE 40bits
Cortex A15	ARMv7	Out-of-Order	3.5	LPAE 40bits
Cortex A53	ARMv8	In-Order	2.3	40bits
Cortex A57	ARMv8	Out-of-Order	4.1	44bits

AArch64寄存器组：
Register	Special	Role in the procedure call standard
x0…x7           Parameter/result registers.
x8              Indirect result location register.
x9…x15          Temporary registers.
x16	IP0	The first intra-procedure-call scratch register (can be used by call veneers and PLT code); at other times may be used as a temporary register.
x17	IP1	The second intra-procedure-call temporary register (can be used by call veneers and PLT code); at other times may be used as a temporary register.
x18             The Platform Register, if needed; otherwise a temporary register.
x19…x28         Callee-saved registers.
x29	FP	The Frame Pointer.
x30	LR	The Link Register.
SP              The Stack Pointer.

AArch32寄存器组：
Register	Special	Role in the procedure call standard
r0…r3     Parameter/result registers.
r4…r8    r9(also as platform register)
r10,r11


Temporary registers.
r12	IP	The Intra-Procedure-call scratch register.
r13	SP	The second intra-procedure-call temporary register (can be used by call veneers and PLT code); at other times may be used as a temporary register.
r14	LR	The Platform Register, if needed; otherwise a temporary register.
r15	PC	Callee-saved registers.

ARMv8支持的数据类型：
Data Type	Length
Byte (B)	8 bits.
Halfword (H)	16 bits.
Word (S)
32 bits.
Doubleword (D)	64 bits.
Quadword (V)	128 bits.
