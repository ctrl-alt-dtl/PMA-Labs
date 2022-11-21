# Lab 3-3 (Unfortunately Also Broken, Too*)

## Execute the malware found in the file *Lab03-03.exe* while monitoring it using basic dynamic analysis tools in a safe environment.

### Questions:
1. What do you notice when monitoring this malware with Process Explorer?
2. Can you identify any live memory modifications?
3. What are the malware's host-based indicators?
4. What is the purpose of this program?

### Answers:

![3-3: SVCHOST.exe](Images/3-3-3.png)

1. Since this is broken on Win 7 the malware sample does not effectively work during execute. In Process Explorer I see **svchost.exe** started as a child process to **Lab03-03.exe**. Hopwever, it fails out and closes by itself. Just by looking at the code in Ghidra, my assumption is this sample is trying to "replace" **svchost.exe**. 
2. Stepping through with x32dbg I can see data being written from .text and .rdata from memory in the created **svchost.exe**. [More here](#in-memory).
3. Viewing the in-memory dump I can see the `practicalmalwareanalysis.log` filename and a series of key presses that are associated with it.[More here](#in-memory).
4. It is a keylogger application, I just cannot execute the malware correctly for the `practicalmalwareanalysis.log` to be created.


## Detailed Answers

### In-Memory

![3-3: In-Memory Dump](Images/3-3-2.png)

Stepping through the execution at `0x0041251` I eventually see this information being written to the newly created **svchost.exe**. There's a loop starting at `0x00401260` that copies the sections in-memory and writes them to the new process.

![3-3: svchost-procexplorer](Images/3-3-6.png)

![3-3: svchost-memory](Images/3-3-4.png) ![3-3: svchost-image](Images/3-3-5.png)
Note: I ran this a few times so the PIDs do not line up with my screenshots. Here I have a partially stepped through svchost.exe.

![3-3: svchost-procexplorer-2](Images/3-3-7.png)

However, by the time the process is about to resume (and before it crashes) the memory of the process increased in size. Which means this process was having data written to it before being restarted.