# Logical Processors

Taking this idea a little further, we can get a CPU to act like it is two logical CPUs. Two separate _threads of execution_ can be multiplexed into the same CPU. Intel calls this technology _hyperthreading_. If you look at task manager on your laptop and check the performance tab, you'll see sockets, cores and logical processors.

- Socket: the physical silicon on the motherboard, a single chip on most laptops, multiple on servers.
- Core: inside that single chip, we can have multiple CPUs or _cores_ which can share resources on the chip, like cache memory.
- Logical Processors: using a technology like hyperthreading, give each physical core two threads of execution.

To be clear, two threads of execution into a single core does not give the same performance as two cores. Often it's quoted as a 40% increase in performance. Particularly in the world of virtualization hosts, we need to be cognizant of this. There are times when a hypervisor might be optimized by switching off hyperthreading.
