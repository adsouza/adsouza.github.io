# How computers work

Before learning about software it is worth having at least a basic grasp of the hardware on which it runs. 
The following model of modern general-purpose digital computers will serve as helpful context as you get acquainted with the craft of software development.

At the highest level of abstraction any such computer consists of a central processing unit (CPU) paired with dedicated primary data storage hardware called main memory. 
The CPU can access any part of this memory at random so it is often called random-access memory (RAM). 
This memory is generally very fast but requires a constant source of electricity to retain data, which means it gets reset (wiped clean) upon losing power. 
Aside from main memory, the CPU contains a relatively small set of even faster temporary storage locations called registers, which are analogous to working memory in humans.

The CPU is also connected to the outside world via additional hardware that can feed it with data (input) or accept data for delivery (output). 
Typical examples of input hardware are touch-sensors, cameras, microphones, keyboards & mice. 
Typical examples of output hardware are display screens, speakers & printers. 
There are also examples of hardware that handle both input & output, either for long-term data storage (e.g. flash memory) or for transmission over a network (e.g. wifi or cellular) to other computers.

The core of any such computer (including smartphones) is a controller (in the CPU) that relentlessly repeats the following cycle until it is powered off:
1. Fetch an instruction from memory.
1. Interpret (decode) the instruction.
1. Execute the instruction, which itself may have up to 3 steps:
    1. Load data from memory into a register if needed.
    1. Perform an arithmetic or logic operation on data in registers, which may have the effect of changing the value of a register.
    1. Store the result of the operation into memory if needed.
1. Checking to see if any input hardware wants attention (i.e. an interrupt), in which case it must be handled appropriately before the next cycle can begin.

Now read about [computational thinking](computational-thinking.md).
