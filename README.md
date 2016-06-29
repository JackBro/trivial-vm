# Trivial VM

The most trivial virtual machine for education purposes. It can run a few x86 machine code instructions on Windows OS. I never tried to build it on Linux but it should be possible.

It is very slow because it copies the instruction being executed to an executable buffer and runs it directly.

This project was introduced at Hysteria Session 2011.

The `LDE64.lib` is Lenght Disassembler. It comes from https://github.com/BeaEngine/lde64.

## Tools

* Visual compiler and linker
* NASM

Another toolchain can be used too but beware of command line options. For more see the batch files.

## VM core

The core functionality is located in `execute.asm`. The instruction being executed is stored in `execute_instruction_buffer` first, `execute_instruction()` is called to execute it then.

## VM1

The 'vm1.c' is the simplest VM possible. It consists of few tens of lines of simple C and asm code.

It merely runs the following code:

    printf("%s World\n\n\n", "Hysteria");
    exit(0);
