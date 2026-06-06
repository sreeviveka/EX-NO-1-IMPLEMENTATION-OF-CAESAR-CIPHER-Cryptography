# EX.NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
## NAME: V.S.SREE VIVEKA
## REG NO: 2305001031
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
#include <stdio.h>

int main()
{
    char text[100];
    int key, i;

    printf("Enter text: ");
    scanf("%s", text);

    printf("Enter key: ");
    scanf("%d", &key);

    for(i = 0; text[i] != '\0'; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
            text[i] = (text[i] - 'A' + key) % 26 + 'A';

        else if(text[i] >= 'a' && text[i] <= 'z')
            text[i] = (text[i] - 'a' + key) % 26 + 'a';
    }

    printf("Encrypted: %s\n", text);

    for(i = 0; text[i] != '\0'; i++)
    {
        if(text[i] >= 'A' && text[i] <= 'Z')
            text[i] = (text[i] - 'A' - key + 26) % 26 + 'A';

        else if(text[i] >= 'a' && text[i] <= 'z')
            text[i] = (text[i] - 'a' - key + 26) % 26 + 'a';
    }

    printf("Decrypted: %s\n", text);

    return 0;
}
```
## OUTPUT:
<img width="517" height="245" alt="image" src="https://github.com/user-attachments/assets/f4871dda-b602-4185-bdf8-1b9e4c3434f1" />
<img width="442" height="285" alt="image" src="https://github.com/user-attachments/assets/7727ef09-49e5-411c-82fb-75f210e54e36" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
