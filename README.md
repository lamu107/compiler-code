# compiler-code
#include <stdio.h> 
#include <string.h> 
#include <ctype.h> 
 
// Function to check if the string is a C keyword 
int isKeyword(char *str) { 
    char *keywords[] = { 
        "auto", "break", "case", "char", "const", "continue", "default", 
        "do", "double", "else", "enum", "extern", "float", "for", "goto", 
        "if", "int", "long", "register", "return", "short", "signed", 
        "sizeof", "static", "struct", "switch", "typedef", "union", 
        "unsigned", "void", "volatile", "while"  }; 
    int i, num_keywords = 32; 
    for (i = 0; i < num_keywords; i++) { 
        if (strcmp(str, keywords[i]) == 0) { 
            return 1;     }    } 
    return 0;} 
// Function to check if the identifier is valid 
int isValidIdentifier(char *str) { 
    int i; 
     
    // Check if string is empty 
    if (strlen(str) == 0) { 
        return 0; 
    } 
     
    // Check if first character is a letter or underscore 
    if (!isalpha(str[0]) && str[0] != '_') { 
        return 0; 
    } 
     
    // Check remaining characters 
    for (i = 1; i < strlen(str); i++) { 
        if (!isalnum(str[i]) && str[i] != '_') { 
            return 0; 
        } 
    } 
     
    // Check if the string is a keyword 
    if (isKeyword(str)) { 
        return 0; 
    } 
     
    return 1; 
} 
 
int main() { 
    char identifier[50]; 
    printf("Enter an identifier: "); 
    scanf("%s", identifier); 
     
    if (isValidIdentifier(identifier)) { 
        printf("%s is a valid identifier.\n", identifier); 
    } else { 
        printf("%s is not a valid identifier.\n", identifier); 
    } 
    return 0; 
} 
