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

## Write a c program to input a string and print.

```c
#include<stdio.h>
int main() {
    char str[20];
    printf("Enter a string: ");
    fgets(str,sizeof(str),stdin);   
    printf("The string is %s\n", str);
}
```
## Write a program in C to find the length of a string without using library functions.
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
## Write a program in C to separate individual characters from a string.
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
## Write a program in C to print individual characters of a string in reverse order.
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
