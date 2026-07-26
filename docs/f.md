# Micro-controllers

A vast amount of devices need simple, low power (in terms of both compute and consumption) controllers. Since the late 1970s controllers such as the _Peripheral Interface Controller_ (PIC) have been used for embedded systems and small systems control.  A modern PIC will be programmable with on board flash memory. Typically a PIC will be programmed in Basic, C or C++ and will have simple and widely available tools, code examples and application notes. 

In machine code, there are a very limited number of instructions (40-80) and they are all fixed in length. There is one accumulator register (W0) which holds the results of all the calculations. Oddly, the RAM used for data is also used for storing temporary values etc. This memory is used like it was a series of registers which map into RAM. Memory is mostly 8 bit although this varies with higher end PICs.

Programs are stored in a separate memory location, normally in flash RAM, so they are non-volatile.

There is a stack, but it is implemented in the hardware, separately.
