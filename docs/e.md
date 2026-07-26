# RISC

So far on this module we have looked at the technologies used in workstations, servers and laptops.
For the past forty years, this market has been controlled by Intel and a few additional players like AMD.
The are _Complex Instruction Set Computers_ (CISC).

_Reduced Instruction Set Computers_ (RISC) is a processor design using simple hardware and highly optimized instruction sets.
They are faster per instructions, physically smaller and simpler and as a result, more power efficient.
But for anything complex, you write code, rather than using instructions executed in hardware.

When we look into the actual execution of instructions in a processor, we can identify empirically (by experimentation and real data) which instructions are used most, which take most processor time. A processor is a number cruncher, so you would guess that arithmetic logic instructions would be executed most?

Wrong!

A processor spends more time shifting data in and out of memory than doing anything else. The second most common thing for it to do is to control the flow of program execution. Optimization techniques such as _pipelining_ and _caching_ are intended to optimize this.  

_Reduced Instruction Set_ or RISC processors were first defined in a 1980 paper [1] and early experimentation with RISC in Berkeley exposed some of the characteristics of this model.
 
- Processors were kept as simple as possible with fixed instruction sets or fixed length. 
- Instructions which process data only operate on registers, not on memory, speeding up and simplifying processing.
- There are many registers, typically thirty two. This was far in excess of the handful of registers in a typical CISC processor.
- Instruction decoding is hard wired. CISC processors were so complex, they required microcode in the core to assist decoding.
- There is a concentration of optimization strategies like pipelines.

The emergent properties of this strategy were that die sizes were much smaller, with fewer transistors in a smaller silicon chip. This resulted in less power consumption, a shorter development time, and for a range of complex reasons, better performance and reduced costs.
 
## Advanced RISC Machines (ARM) processors

Acorn Computer Ltd. (Cambridge, England) developed the first commercial RISC chip in the mid-1980s, the ARM processor [2]. They have an interesting business model. They develop the instruction sets, tools and specifications and then license the production of chips to large silicon foundries. 

ARM is now the most widely used instruction set worldwide. Early chips shipped were 32 bit; but from 2011, a 64 bit version (ARMv8) has been available. The ARM contains all the components for a computer on a single silicon die; it is therefore a _System on a Chip_ or SoC. The instruction set design is what we would expect from RISC. Instructions are simple and most instructions execute in a single clock-cycle. If you want to work with an ARM based system, a Raspberry PI is a cheap and easy solution. You can load a full copy of Linux (the standard is a derivative of Debian Linux).

The cost of a board like the Raspberry Pi is about €50-€200, depending on memory etc.

[1] Patterson, D.A. and Ditzel, D.R., 1980. The case for the reduced instruction set computer. ACM SIGARCH Computer Architecture News, 8(6), pp.25-33.

[2] Furber, S.B., 2000. ARM system-on-chip architecture. Pearson Education.
