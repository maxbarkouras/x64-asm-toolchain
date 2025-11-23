# x64-ASM-Toolchain
An assembler and disassembler written in x64 assembly for the MIPS ISA (yes its crazy) 

**Compilation:**
- This was written for x64 assembly on ***windows***.
  - While it can be made to run on linux by replacing all syscalls and simplyfing logic, its current state is windows exclusive.
- Download NASM for windows.
- Compile & Link (for both assembler and disassembler):
  - ```nasm -f win64 mipsAssembler.asm -o mipsAssembler.obj```
  - ```link /entry:_start /subsystem:windows mipsAssembler.obj /nodefaultlib```
- Now you should have a runnable exe for both assembly and disassembly.

**Usage:**
- For assembler, a MIPS file must be saved as *'assembly.asm'* in the same directory as program execution.
- For disassembler, a *'machine.bin'* binary file must be saved in the same directory as program execution.
  - This does not have to be assembled with the assembler, can be done using alternative programs like MARS.
  - A text represented binary file is also allowed, literal 1s and 0s, which must be saved as "binary.bin".
- Run the assembler/disassembler and output files will be created in current directory.
