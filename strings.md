## Write a c program to reverse the string and count the no of characters in the string

 ```c
#include <stdio.h>

int main() {
    char str[100];
    int i,count=0;
    char temp;
    scanf("%s",str);
    for(i=0;i<str[i];i++){
        count++;
    }
    printf("The no of characters in the string =%d\n",count);
    for(i=0;i<count/2;i++){
        temp=str[i];
        str[i]=str[count-i-1];
        str[count-i-1]=temp;
    }
    printf("%s",str);
    return 0;
}

```

## 1)Write a c program to input a string and print.

```c
#include<stdio.h>
int main() {
    char str[20];
    printf("Enter a string: ");
    fgets(str,sizeof(str),stdin);   
    printf("The string is %s\n", str);
}
```
## 2)Write a program in C to find the length of a string without using library functions.
```c
#include <stdio.h>

int main() {
    char str[100];
    int length = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    for (i = 0; str[i]; i++) {
            length++;
    }
    printf("Length of the string = %d\n", length);
}
```
## 3)Write a program in C to separate individual characters from a string.
```c
#include <stdio.h>
int main() {
    char str[100];
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    printf("\nIndividual characters:\n");
    for (i = 0; str[i]; i++) {
        printf("%c\n", str[i]);
    }
}
```
## 4)Write a program in C to print individual characters of a string in reverse order.
```c
#include <stdio.h>
int main() {
    char str[100];
    int i, length = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    for (i = 0; str[i]; i++) {
            length++;
    }
    printf("\nCharacters in reverse order:\n");
    for(i=length-1;i>=0;i--){
        printf("%c\n", str[i]);
    }
}
```
## 5)Write a C program  to count the totoal no of words in a string.
```c
#include <stdio.h>
#include <string.h>
int main() {
    char str[200];
    int i, words = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    for (i = 0; str[i]; i++) {
        if (i==0||str[i]==' '||str[i]=='\t') {
            words;
        }
    }
    printf("Total number of words: %d\n", words);
}
```
## 6)Write a program in C to compare two strings without using string library functions.
```c
#include <stdio.h>

int main() {
    char str1[100], str2[100];
    int flag = 0;
    printf("Enter first string: ");
    fgets(str1, sizeof(str1), stdin);
    printf("Enter second string: ");
    fgets(str2, sizeof(str2), stdin);
    for(int i=0;str1[i]|| str2[i];i++) {
        if (str1[i] != str2[i]) {
            flag = 1;  
            break;
        }
    }
    if (flag == 0)
        printf("Strings are equal.\n");
    else
        printf("Strings are NOT equal.\n");
}
```
## 7) Write a program in C to count the total number of alphabets, digits and special characters in a string.
```c
#include <stdio.h>

int main() {
    char str[200];
    int i, alphabets = 0, digits = 0, special = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    for (i = 0; str[i] != '\0'; i++) {
        if ((str[i] >= 'a' && str[i] <= 'z') ||
            (str[i] >= 'A' && str[i] <= 'Z')) {
            alphabets++;
        }
        else if (str[i] >= '0' && str[i] <= '9') {
            digits++;
        }
        else if (str[i] != '\n' && str[i] != ' ') {  
            special++;
        }
    }
    printf("\nTotal Alphabets = %d\n", alphabets);
    printf("Total Digits = %d\n", digits);
    printf("Total Special Characters = %d\n", special);
}
```
## 8)Write a program in C to copy one string to another string.
```c
#include <stdio.h>
int main() {
    char str1[100], str2[100];
    int i;
    printf("Enter a string: ");
    fgets(str1, sizeof(str1), stdin);
    for (i = 0; str1[i] != '\0'; i++) {
        str2[i] = str1[i];
    }
    str2[i] = '\0'; 
    printf("Copied string: %s", str2);
}
```
## 9)Write a program in C to count the total number of vowels or consonants in a string.
```c
#include <stdio.h>

int main() {
    char str[200];
    int i, vowels = 0, consonants = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    for (i = 0; str[i] != '\0'; i++) {
        char ch = str[i];
        if ((ch >= 'a' && ch <= 'z') ||
                 (ch >= 'A' && ch <= 'Z')){
        if (ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u' ||
            ch=='A' || ch=='E' || ch=='I' || ch=='O' || ch=='U') {
            vowels++;
        }
        else 
            consonants++;
        }
    }
    printf("\nTotal Vowels = %d\n", vowels);
    printf("Total Consonants = %d\n", consonants);
}
```
## 10)Write a program in C to find the maximum number of characters in a string.
```c
#include <stdio.h>

int main() {
    char str[200];
    int i, count = 0;
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        count++;
    }
    printf("Total number of characters in the string = %d\n", count);
}
```
