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
 