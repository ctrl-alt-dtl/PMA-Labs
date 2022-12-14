# Lab 6-2

## Analyze the malware found in the *Lab06-02.exe*

### Questions

1. What operation does the first subroutine called by `main` perform?
2. What is the subroutine located at `0x40117F`?
3. What does the second subroutine called by `main` do?
4. What type of code construct is used in this subroutine?
5. Are there any network-based indicators for this program?
6. What is the purpose of this malware?

### Answers

1. It is the same function as in [Lab 6-1](/Chap6/6-1/README.md#answers) that checks for an Internet connection. There's some additional messages attached based on the success of having Internet access. Further analysis [below](#detailed-answers).
2. Same as Lab 6-1, in which `0x40117F` is a printf function.
3. The second subroutine is `0x401040` and that is the path if an Internet connection is found. Inside this function, a URL (`http://www.practicalmalwareanalysis.com`) is called, is downloaded, read, and parsed starting at the `<-!` comment section in an HTML file.
4. 

## Detailed Answers

### Static Analysis

### Dynamic Analysis

### Advanced Static Analysis
