# Lab 6-3

## Analyze the malware found in the *Lab06-03.exe*

### Questions

1. Compare the calls in `main` to Lab 6-2's `main` method. What is the new function called from `main`?
2. What parameters does this new function take?
3. What major code construct does this function contain?
4. What can this function do?
5. Are there any host-based indicators for this malware?
6. What is the purpose of this malware?

### Answers

1. The calls in Lab 6-3 are similar to [Lab 6-2](/Chap6/6-2/README.md#answers), except the new function that is called is `0x401130`. This new function is what processes the commands from the HTML comment section in `http://www.praticalmalwareanalysis.com/cc.htm`.
2. This function takes two parameters. The first parameter is a character that comes from the HTML comment which is used in the switch statement of that function. The second parameter is the `argv[0]` program name which is used in the second case of the switch statement.
3. The major code construct is a switch statement that executes five different actions based on the command received.
4. This function can create a new directory, can copy and delete a file, open a registry and set a value, sleep for 100 seconds, or print error messages.
5. The host-based indicators are the file and directory names and the attributes of the registry key.
6. Building off of Labs 6-1 and 6-2, this malware has the additional purpose of using the value set in the HTML comment section and execute a command based on the path of a switch statement.

## Detail Answers

### Static Analysis

### Dynamic Analysis

![6-3: Dynamic Analysis](Images/6-3-1.png)
![6-3: Dynamic Analysis](Images/6-3-2.png)
![6-3: Dynamic Analysis](Images/6-3-3.png)

### Advanced Static Analysis
