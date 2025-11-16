## Write a Program to print the address of variables using the address operator.
```c
#include <stdio.h>
int main() {
    int a;
    float b;
    char c;
    printf("Enter the integer:");
    scanf("%d",&a);
    printf("Enter the float value:");
    scanf("%f",&b);
    printf("Enter the character:");
    scanf("%c",&c);
    printf("Value=%d Address of a = %p\n",a,&a);
    printf("Float value=%f Address of b = %p\n",b,&b);
    printf("Character=%c Address of c = %p\n",c,&c);
}
```
