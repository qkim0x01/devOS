# devOS
- Building OS project from scratch

## Progress
- Roughly finished bootLoader and kernelLoader
- kernelLoader can load C kernel into memory
- C kernel clears background and prints "Hello World" 
- Turned on A20 Gate to access > 1MB memory

## Build
```
$ make
```
## Run
Qemu listen on port 1234 and wait for gdb connection
```
$ sh boot.sh
```
## Debug
```
$ gdbtui
$ (gdb) target remote:1234
$ (gdb) layout asm
```
## Files
- bootLoader.asm
	- First stage of bootloader (loads kernelLoader.asm)
- kernelLoader.asm
	- Second stage of bootloader (loads kernel)
- kernel.c
	- kernel
- func_16.asm
	- functions used in 16-bit real mode
## Next Step
- Make File System

