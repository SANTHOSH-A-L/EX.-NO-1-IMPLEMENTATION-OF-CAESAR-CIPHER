# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include<stdio.h> 
#include<string.h> 
#include<ctype.h>  
int main()  
{ 
char plain[100], cipher[100]; int key, i, length; 
printf("Enter the plain text: "); 
scanf("%s", plain);  
printf("Enter the key value: "); 
scanf("%d", &key);  
printf("\nPLAIN TEXT: %s", plain); 
printf("\nENCRYPTED TEXT: "); 
length = strlen(plain); 
for (i = 0; i < length; i++) 
{ 
cipher[i] = plain[i] + key; 
// Handling uppercase letters 

if (isupper(plain[i]) && cipher[i] > 'Z') 
{ 
cipher[i]= cipher[i] - 26; 
} 
// Handling lowercase letters 
if (islower(plain[i]) && cipher[i] > 'z') 
{ 
cipher[i] = cipher[i] - 26; 
} 
printf("%c", cipher[i]); 
} 
cipher[length] = '\0'; // Null-terminate the cipher text string 
printf("\nDECRYPTED TEXT: "); 
for (i = 0; i < length; i++) 
{  
plain[i] = cipher[i] - key; 
// Handling uppercase letters 
if (isupper(cipher[i]) && plain[i] < 'A') 
{ 
plain[i] = plain[i] + 26; 
} 
// Handling lowercase letters 
if (islower(cipher[i]) && plain[i] < 'a') 
{ 
plain[i] = plain[i] + 26; 
} 
printf("%c", plain[i]); 
} 
plain[length] = '\0'; // Null-terminate the plain text string return
}
```

## OUTPUT:
![WhatsApp Image 2025-09-04 at 08 47 59_6e030b69](https://github.com/user-attachments/assets/295fb039-38df-4f04-a78f-36b6e82472be)



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
