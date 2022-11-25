# IDA Pro (Throwing Ghidra in here too)

## Lab 5-1

## Analyze the malware found in the file *Lab05-01.dll* using only IDA Pro (*Ghidra). The goal of this lab is to give you hands-on experience with IDA Pro\*. 

### Questions:
1. What is the address of `DllMain`?
2. Use the Imports window to browse `gethostbyname`. Where is the import located?
3. How many functions call `gethostbyname`?
4. Focusing on the call to `gethostbyname` located at `0x10001757`, can you figure out which DNS request will be made?
5. How many local variables has IDA Pro recognized for the subroutine at `0x10001656`?
6. How many parameters has IDA Pro recognized for the subroutine at `0x10001656`?
7. Use the Strings window to locate the string `\cmd.exe /c` in the disassembly. Where is it located?

### Answers: