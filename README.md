## Exp 14 : IMPLEMENTATION OF HASH ALGORITHM


## AIM:

To implement a simple hash algorithm in C to generate a hash value for a given message, demonstrating how hashing can be used for data integrity.


## ALGORITHM:
1.	Accept a message as input from the user.
2.	Remove any newline character from the input message.
3.	Initialize a hash value to zero.
4.	For each character in the message:
a.	Multiply the current hash value by 31 (a prime number).
b.	Add the ASCII value of the current character to the hash.
5.	After processing all characters, the final hash value is produced.
6.	Display the generated hash value as the output.


## PROGRAM:
```
#include <stdio.h> 
#include <string.h> 
// Simple hash function for demonstration 
unsigned int simple_hash(const char *message) 
{ 
unsigned int hash = 0; int 
i; 
for (i = 0; i < strlen(message); i++) 
{ 
hash = (hash * 31) + message[i]; // Using a prime number for multiplication 
} 
return hash; 
} 
int main() 
{                                                                
char message[256];  
unsigned int hash_value; 
// Input message from user 
printf("Enter the message to hash: "); 
fgets(message, sizeof(message), stdin); 
message[strcspn(message, "\n")] = '\0'; // Remove newline character 
// Generate hash 
hash_value = simple_hash(message); 
printf("Generated hash value: %u\n", hash_value); 
return 0; 
} 
```
## OUTPUT:
<img width="983" height="337" alt="image" src="https://github.com/user-attachments/assets/06b30e8a-442c-4a9f-ab73-e54067327ac7" />


## RESULT:

The hash algorithm was implemented successfully, generating a hash value for the input message to demonstrate data integrity verification.
