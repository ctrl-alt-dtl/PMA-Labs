# Lab 7-1

## Analyze the malware found in the *Lab07-01.exe*

### Questions

1. How does this program ensure that is continues running (achieves persistence) when the computer is restarted?
2. Why does this program use a mutex?
3. What is a good host-based signature to use for detecting this program?
4. What is a good network-based signature for detecting this malware?
5. What is the purpose of this program?
6. When will this program finish executing?

### Answers

1. I see immediately int the strings the value of `MalService` and `Malservice` as well as `CreativeServiceA`, `OpenSCManagerA`, `StartServiceCtrlDispatcherA` so my initial guess is that persistence is achieved through the creation of a Windows Service.
2. The use of a mutex here would be to make sure the malware only has one version of itself running on the machine.
3. A great host-name signature would be the Windows Service name of `MalService1` that are registered during creation and most likely the [`CreateMutexA`](https://learn.microsoft.com/en-us/windows/win32/api/synchapi/nf-synchapi-createmutexa) function call along with the mutex name of `HGL345`. I had to open Ghidra to find where `HGL345` is used in order to verify it was indeed a hard coded signature. The use is at `0x401052`.
4. Looking at the strings from *Detect It Easy* I see the URL string for `http://www.malwareanalysisbook.com` as well as `Internet Explorer 8.0` as User Agent. I also see `InternetOpenUrlA` and `InternetOpenA`.
5. 
6. 

## Detailed Answers

### Static Analysis

### Dynamic Analysis

### Advanced Static Analysis
