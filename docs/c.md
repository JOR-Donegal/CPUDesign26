# Pipelining

In our simple CPU models, an instruction ripples through the registers of the CPU, taking quite a few clock cycles to complete. Why not break up the activities required by an instruction into a number of steps and do each of these steps concurrently? Consider the steps an ordinary instruction might make (Fig 7). 

<figure>
<img src = "https://jor-donegal.github.io/CPUDesign26/images/table2.jpg">
<figcaption>Table 7. Flow of a single instruction .</figcaption>
</figure>

Now suppose we run one instruction after another through the stages. As one as an instruction had finished a stage, the next instruction can use the subsystems required by that stage!

<figure>
<img src = "https://jor-donegal.github.io/CPUDesign26/images/table3.jpg">
<figcaption>Table 8. Pipeline flow of a single instruction .</figcaption>
</figure>

At clock cycle 1

- Execute instruction 1. The first part of the cycle is the instruction fetch. 

At clock cycle 2

- Instruction 1 can move to the decoder
- Execute instruction 1. The first part of the cycle is the instruction fetch. 

At clock cycle 3

- Instruction 1 can move to reading operands from memory
- Instruction 2 can move to the decoder
- Execute instruction 3. The first part of the cycle is the instruction fetch. 

By the fifth clock cycle, 5 instructions are being simultaneously executed through hardware designed only for single processing. As you can imagine, this can massively enhance performance. A modern Intel processor may have up to 20 stages in its _pipeline_.