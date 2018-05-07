# System Architecture

## Von Neumann architecture
The Von Neumann architecture was propesed by John vom Neumann in 1945.
In the Von Neumann architecutre, both instructions and data were stored in memory, as aposed to the previous computer that required rebuilding between the running of different programs.

The Von Neumann architecure consists of several registers. These are as follows

* MAR (Memory Address Register)
    * stores the address of the next item to be read from / written to  memory
    * this can be data or an instruction
* MDR (Memory Data Register)
    * stores the data that has just been read / about to be written to / from memory
    * when read is data or instruction
* PC (Program Counter)
    * Stores the address of the next instruction to be executed
* Accumulator
    * Stores ALU results (math / logic)

## common CPU components
The CPU consists on many components. Three of these are the ALU, CU and Cache.

### The ALU
The ALU (or Arithmic Logic Unit) is the part of the CPU that perfoms calcualtions (mathmatical and logical). It can compare values, to see if they are equal, can check if a value equals zero, and can also add, subtract, multiply and divide.

### The CU
The CU (or Control Unit) gets instruction from memory and the decodes them. It then tells the rest of the CPU what to do in order to complete the instrucion. If an instruction is to add numbers, it will make the ALU do this.

### Cache 
Cache is fast of access memory that is on the CPU. There are different levels of cahce (with lower numbers being smaller, more expensive, and faster to access). Cache is used to store data the is used regularly (like mouse location) so help speed up opperations. If the cache is bugger, it will be able to store more data, speeding up the CPU.

## Fetch Decode Execute
The CPU follows the Fetch Decode Execute cycle.

### Fetch
* The program counter increments.
* The value in the PC is stored in the MAR.
* The MARs value is sent over the address bus.
* The CU sends a READ signal over the control bus.
* The value in memory is sent over the data bus to the MDR.

### Decode
The CU then looks at the opt code of the instruction and works out what calculation has to be done.

### Execute
The ALU executes the instruction and stores the output in the Accumulaor.

## What affects CPU performance?
CPU performance is affected by three main things.
Clock speed, cache size and the number of cores.

### Clock Speed
The clock speed of a CPU is how many instucions each core can execute per second (more on core count later).
If the clock speed is 1Hz then 1 instruction in being executed per second.
Low end CPUs these days can have clockspeeds of 1.8GHz or 1800000000 instruction per second.
This makes it look like the computer is doing many things at one time, when in reality it is doing many things straight after each other very very fast.

### Core Count
The number of cores a CPU has effects of fast it is. A core is like a mini CPU, so if you have a clock speed of 1.8GHz and 2 cores, then 3.6x10<sup>9</sup> instructions are executed per second.
Doubling the core count theoretically double the CPU speed, however not all software is optimised to use multiple cores.

### Cache Size
As mention previousley, [the cache](#cache) is memory that is very quick to access.
Increasing the cache size increases how much data is fast to access, speeding up the CPU.
