# Number crunching

Even after 50 years, the principle of operation for an Intel or AMD CPU should be recognizable from the simple descriptions in my earlier notes. To finish this technology introduction, I want to talk about some of the enhancements that have been used to speed up and generally improve the performance of processors.

And then the law of unintended consequences kicks in. In recent years, some of the most intractable vulnerabilities in PC hardware were introduced by these enhancements.

## Floating Point Calculations

As we have described a CPU, it is a general purpose machine for calculating numbers and manipulating numbers which could represent things like characters. You should have covered _ASCII_ and _Unicode_ in one of my other modules, if you don’t remember, do an internet search on those terms now. However the registers in a CPU are of a fixed size; in modern processors either 32 or 64 bits wide. That means the smallest and biggest numbers we can describe are limited by the size of the register. 

- What is the biggest _integer_ you can describe in a 32 bit register?  
- What is the biggest _signed integer_ you can describe in a 32 bit register?

If you don’t remember, do an internet search on those terms now.

You should understand _scientific notation_, if you are rusty, revise independently. If I want to express the number one thousand in scientific notation, I can write it as 1 x 10^3^. If I want to write 1/1000 in scientific notation I can write it as 1 x 10^-3^. Before we go on, make sure you remember all this! If you don’t remember, do an internet search on those terms now. The principle of scientific notation is that we split a number into a _fraction_ and an _exponent_.

<figure>
<img src = "https://jor-donegal.github.io/CPUDesign26/images/table1.jpg">
<figcaption>Table 1. Floating point examples .</figcaption>
</figure>

We can describe very big and very small numbers in the computer in exactly the same way. Imagine we have a 32 bit register to describe numbers; we call this _single precision floating point_. We could store the fraction part of the number in the first 24 bits and the exponent in the last 8. The exponent must be signed so only 7 digits could be used to represent numbers and our exponent could range from -127 to +128 (why?). _Double precision floating point_ uses 64 bits where 53 digits are used for the fraction and 11 bits are used for the exponent. Giving one bit for the sign, that gives us an exponent range of -1022 to + 1023. We can now describe very large and very small numbers.

The floating point examples given here refer to the IEEE version of floating point. There are variations out there and you may find floating point data which does not match the description above!

## Co-processors

But a CPU is a general purpose computing device, it was never designed to cope with these very large numbers. It was designed for _signed integer values_, not floating point. Early PCs did their floating point calculations in a slow and cumbersome way. The chip manufacturers developed special chips specifically to do floating point; these were called co-processors. So for example, the 8086 processor could have an 8087 _co-processor_ installed beside it to enhance its number crunching capabilities.

By the 1990s, the chip manufacturers had begun to integrate the co-processor onto the same silicon die as the processor. From the 80486DX onwards, the processor in most personal computers has included the co-processor. If you check the block diagram of any modern CPU, your will find a floating-point unit.
