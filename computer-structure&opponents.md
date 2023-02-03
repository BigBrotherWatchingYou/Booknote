# Hardware
## CPU structure
###Programm Counter(PC)  or Instruction Counter
- It determins where the program is heading
- It store instruction address in memory 
- PC can store 'instruction address' and temporary store 'arithmetical/logical calculation result'
1. Before the program is executed, the first instruction's memory address was sent into Program Counter,
CPU will follow PC's command, reading the first instruction (Fetch instruction) 
2. when executing the instruction, CPU will rewrite the information in PC ( For instance: PC= PC +1), so that 
it can always reach the next intruction's address
3. Beacause of the mostly instruction were executed in order, the rewrite process usually runs like (PC = PC +1)
4. when it comes to a transfer instruction, the instruction result is to change the value of PC(turns to the aimed address)
5. Thus, CPU always following the PC's command, (fetching instructions, compiling code, executing) and based on it , the program
transfer was accomplished.

# Hardware
## CPU and Memory
- while a program is running , CPU needs to get instructions from Memory, analyse and execute. 
- this was based on 'Different section of the Instruction Cycle' , which was stored in memory using binary code.

# Hardware
## Input/Output
### Input/Output Devices definition
- system's connection to the external world
- Each I/O device connected to the I/O bus either by an adapter or a controller
- Controllers are chipsets in the device itself or on the system's main printed circuit board (often called
the motherboard).
- An adapter is a card that plugs into a slot on th emotherboard
- both of them are to transfer information back and forth between the I/O bus and an I/O device
- controlling ways between computer and peripherals: Process Control, Interrupt(break), DMA(Direct memory access)
- Process control: CPU executing process controls the Input/Output process
- Interrupt(break):device send CPU a "break request signal" , when CPU respond, it will stop the executing task and 
run the device's request. When it was done, CPU turns back to its work.
- DMA(direct memory access) : CPU send order to DMA controller and let it handle the Data transportation, and
send back the information to CPU( this can greatly reduce occupation of CPU and save resourses)

 
# Hardware
## Accumulator(AC)
- main part of calculator that store calculation results
- providing a work area for ALU(arithmetic logical unit, temporary store information of the ALU calculation


# Hardware
## Bus: Data bus, Address bus, and Control bus
### Between CPU and bus
- DMA occupy bus resources, and CPU won't use bus all the time(while in a instruction cycles)
- so that DMA request's checkpoint will executed at the end of each bus period(or so called machine cycles)

### Word Length
- 1 word = 2Byte = 16bit
- we usually call 16bit= 1 word
- Word Length means the bits that CPU can handle at a same time
- the longer the Word Length, the more effective
- FOR EXAMPLE: if a memory has a 4GB capacity, and a 32-bit Word Length , then :
the width of AB and DB is 32-bit

### Data bus (DB)
1. transport CPU data to Storage or I/O.etc  (and vice versa)
2. the width of
### Address Bus(AB)
- Data can only be transported from CPU to storage or I/O,
- AB is to transporting address
### Control Bus(CB)
- Control Bus is a bunch of different control lines
## VLIW:(Very Long Instruction Word) 
- a group of instructions, it links many instructions together, which speed up calculation
- binary
- transfer control signals and timing signals to device in the proximity
- (Base on data transformation)could be divinded into serial bus/parallel bus
- (Base on whether the timing signal is independent) : synchronous bus/asynchronous bus### serial bus
- only one line(high efficiency)
### parallel bus
- all line transport at the same time(which lead to interupttion, low efficiency)
### synchronous bus
- connectted device synchronize using the same clock(working in the same scheule)
### asynchronous bus
- no united clock, different scheule(which means higher completibility, for example Firewire or IEEE1394\USB 2.0)

# System
## DMA(Direct memory access)
- transfer a address value to another place
- dont't need CPU controllment
- using hardware to open a tunnel for RAM and I/O device(which makes CPU more effective)
- 

# CISC and RISC
## CISC
- CISC (Complex instruction set computer)
- Main: enhance function of ordinary instuctions, use instuctions o higher complexity to replace functions that were used to run by software programmm(which makes software functions more "hardwarelize")
- usually contains more than 3,000 instructions
## RISC
- RISC(reduced instructions set computer)
- Main: decreace the hardware's complexity by simplifying instructions, in order to run instructions in a single cycle
- speed up executive speed by optimizing compliation
- uses hardwires logic controllment

