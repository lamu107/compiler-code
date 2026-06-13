The program follows a systematic sequence of checks: 
1. Input: Receive a string (identifier) from the user. 
2. Empty Check: Verify that the string length is greater than zero. 
3. First Character Rule: * Check if the first character is an alphabetic letter (a-z, A-Z) or an 
underscore (_). 
o If it is a digit or a special character, the identifier is invalid. 
4. Subsequent Character Rule: * Iterate through the remaining characters of the string. 
o Each character must be alphanumeric (letter or digit) or an underscore. 
o If any special character (e.g., @, #, $) or space is found, the identifier is invalid. 
5. Keyword Restriction: 
o Compare the input string against a pre-defined list of 32 reserved C keywords 
(e.g., int, while, return). 
o If the string matches any keyword, the identifier is invalid. 
6. Output: If all conditions are satisfied, the string is marked as valid. Otherwise, it is 
marked as invalid.
