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

