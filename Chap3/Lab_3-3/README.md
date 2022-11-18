# Lab 3-3 (Unfortunately Also Broken, Too*)

## Execute the malware found in the file *Lab03-03.exe* while monitoring it using basic dynamic analysis tools in a safe environment.

### Questions:
1. What do you notice when monitoring this malware with Process Explorer?
2. Can you identify any live memory modifications?
3. What are the malware's host-based indicators?
4. What is the purpose of this program?

### Answers:

1. Since this is broken on Win 7 the malware sample does not effectively work during execute. In Process Explorer I see **svchost.exe** started as a child process to **Lab03-03.exe**. Just by looking at the code in Ghidra, my assumption is this sample is trying to replace **svchost.exe**.
2. 
3. 
4. 