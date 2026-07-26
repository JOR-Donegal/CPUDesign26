# Micro-architecture

By now, you should have an appreciation of the complexity of a modern processor. You are probably wondering how you could get this much functionality out of gates and flip flops. This is all so complex, you would imagine the need for a little computer inside the CPU to run the CPU? Believe it or not, this is (sort of!) the case.

The instruction decoder and control unit of complex microprocessors have programme code stored in it to tell it how to use its logic to run the CPU. This is called _microcode_. As programmers, we do not generally get access to this level and we certainly don’t get to change the code. In fact the code is stored in Read Only Memory or ROM, which cannot be written to.

Mostly!

Modern processors have utilities that allow the microcode to be rewritten. Beware, here be dragons!!

Problems with some versions of processor from 2022 onwards have resulted in Intel publishing utilities to specifically update the microcode in the processor.
