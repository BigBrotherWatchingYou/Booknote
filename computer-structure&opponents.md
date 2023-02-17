# Hardware
## CPU structure
### Computer running process
1. programm was loaded into memory
2. when CPU execute a instruction, it will be sent into Buffer Register, then into IR(instruction register)
3. Instruction Decoder will genereate Operand based on IR's content



## IR( Instruction Register)
- temporary store instructions from memory(unaccessable, invisible)

## MDR (Memory Data Register)
- 

### Programm Counter(PC)  or Instruction Counter
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
### Programm Counter function
1. store info
2. count
#### PC process
- before execution: origin address was sent into PC
- executing: CPU will modify PC's content automatically, so that it can always reach next instruction's address
- modify process: mostly just +1
- Programmer can access PC while compilng program


## Memory and storage
## Memory
- Memory are usually consist of DRAM
### SRAM
- usually used as Cache
- faster than DRAM, but more expensive
### DRAM
- usually used as buffer zone for memory and graphic system
- need periodically recharge and refresh to keep info
### EEPROM
- electronic erasable programable read only memory
### external memory
- Harddisk.etc
### internal memory

#### associative memory
- access data base on content


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

## Bus
- using Bus structure in computer system makes it easier to unitilize, and reduce  quantity of info-transport-line.
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
- which means DMA connect directly Memory and I/O device

# CISC and RISC
## CISC
- CISC (Complex instruction set computer)
- Main: enhance function of ordinary instuctions, use instuctions o higher complexity to replace functions that were used to run by software programmm(which makes software functions more "hardwarelize")
- usually contains more than 3,000 instructions
- has many restrictions when executing streamline
### CISC feature
- instruction length under CISC frame are usually variable, and has a large variety forms
- instructions usually needs multiple cycle to finish
- about 20% instructions will are frequently used, the rest 80% usually won't be used(which is unreasonable)
## RISC
- RISC(reduced instructions set computer)
- Main: decreace the hardware's complexity by simplifying instructions, in order to run instructions in a single cycle
- speed up executive speed by optimizing compliation
- uses hardwires logic controllment
### RISC feature
- RISC
- Instructions are usually in solid(speified)format and length
- addressing mode are simple, most instructions can be done in one cycle
- suitable for streamline
- only load/store instuction can access memory
- data handling instructions onl operate content in register
- in order to boost calculation, RISC will set multiple register, and desinate register for special purpose
- CISC allow data-handling-instructions operate memory, don't need so much register


## General Purpose register
- CPU access speed ranking: General Purpose register > Cache > Memory > Disk

## address mapping
### Fully associative addresss mapping
- chunk in mian memory can be place in anywhere in cache
- minimum chunk conflicts among the three mapping ways
### Direct associative mapping
- (chunk number in main memory)/cache groups=chunk position in cache
### Group associative mapping
- chunk number/ cache groups= chunk groups in cache(in this group chunk can be placed anywhere)
## How does address mapping works?

--------theory waiting to fufill--------------


## System Reliability
![1](assets/system_reliability.jpg)
- if module reliability 1,2,3, are :0.90; 0.80; 0.80
- and you want the whole reliabiity is 0.85
- then module 4 's reliability should be at least:
- 0.85/(0.9*(1-0.8)*(1-0.8))

## Breakpoint
### Impact:
- Breakpoint makes computer able to react with accidents
- Increase CPU's efficiency
- If there's no breakpoint and meet a accident, CPU can only follow the program, require and handle all device(low efficiency)
### external interrupt
- interrupt caused by external device, can be divided into Maskable/nonMaskable interruption
#### Maskable interrupt
- interrupt request sent by external device that can set breakpoint
#### non-Maskable interrupt
- interrupt by software's breakpoint and 'error' when executing instructions(including overflow\ zero division)
### Definition
- accident occurs when CPU executing programm, that CPU has to stop running the current program, and handle another programm to deal with the accident.
- When the Accident was done, CPU returns to run the origin paused program
### Multiple breakpoint
- there are two ways dealing with multiple breakpoint
1.  while dealing with a breakpoint, ban other interrupt request
2.  concern about the priority of the breakpoints: allow higher-priority breakpoint interrupt a lower one; return to the lower when the higher one is done

# Chip, Capacity and address space
- if a storage (16K *8 bit, address space: 000H~3FFFH) was organized by chips(2K*4), then it needs 16 chips(16K*8/(2K*4))
- The storage(16K*8) means address space was divided into 8 part, each part(3FFF+1=4000)/8= 4*16^3)/8=8*16^2=800H
- each part: 0000H~0777FH, 0800H~0FFFH, 1000H~17FFFH
- for example: address unit: 0B1FH is in 0800H~0FFFH

# Flynn
- Definition: a classification of computer system structure
1. Instruction Stream
2. Data Stream
3. Multiplicity
## SISD 
- (Single instruction single datasteram)
- CANNOT concurrent compating
- ONLY serial computing
## SIMD 
- single instruction multiple datastream
- using one instuction-stream handle multiple data-stream
- useful in digital signal\graphics\multimedia
## MISD
- multiple instruction single datastream
- ONLY theoratical Model
- DO NOT exist
## MIMD 
- multiple instruction multiple datastream
- these instructions handle different data-stream
- FOR EXAMPLE: AMD CPU
