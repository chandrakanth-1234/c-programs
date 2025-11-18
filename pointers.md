## 1)Write a Program to print the address of variables using the address operator.
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
## 2)Write a program to print size of pointer variables.
```c
#include <stdio.h>
int main() {
    int *p1;
    float *p2;
    char *p3;
    double *p4;
    printf("Size of int pointer     = %lu bytes\n", sizeof(p1));
    printf("Size of float pointer   = %lu bytes\n", sizeof(p2));
    printf("Size of char pointer    = %lu bytes\n", sizeof(p3));
    printf("Size of double pointer  = %lu bytes\n", sizeof(p4));
}
```
## 3)Write a program to print size of pointer variables and size of values Dereferenced by them.
```c
#include <stdio.h>
int main() {
    int *p1;
    float *p2;
    char *p3;
    double *p4;
    printf("Size of int pointer          = %lu bytes\n", sizeof(p1));
    printf("Size of value *p1 (int)      = %lu bytes\n\n", sizeof(*p1));

    printf("Size of float pointer        = %lu bytes\n", sizeof(p2));
    printf("Size of value *p2 (float)    = %lu bytes\n\n", sizeof(*p2));

    printf("Size of char pointer         = %lu bytes\n", sizeof(p3));
    printf("Size of value *p3 (char)     = %lu bytes\n\n", sizeof(*p3));

    printf("Size of double pointer       = %lu bytes\n", sizeof(p4));
    printf("Size of value *p4 (double)   = %lu bytes\n", sizeof(*p4));
}
```
## 4)Write a program to illustrate the dereferencing of pointers.
```c
#include <stdio.h>
int main() {
    int a = 10;
    int *p;        
    p = &a;         
    printf("Value of a  = %d\n", a);
    printf("Address of a = %p\n", &a);
    printf("\nPointer p stores address = %p\n", p);
    printf("Dereferencing p gives value = %d\n", *p);
    *p = 20; 
    printf("\nAfter changing value through pointer:\n");
    printf("New value of a = %d\n", a);
    printf("Dereferenced value from p = %d\n", *p);
}
```
## 5)Write a C program to illustrate pointer arithmetic
```c
#include <stdio.h>
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *p;
    p = arr; 
    printf("Base Address (p)          = %p\n", p);
    printf("Value at p (*p)           = %d\n\n", *p);
    p++;  
    printf("After p++  (p)            = %p\n", p);
    printf("Value at new p (*p)       = %d\n\n", *p);
    p--;  
    printf("After p--  (p)            = %p\n", p);
    printf("Value at new p (*p)       = %d\n\n", *p);
    p = p + 2;
    printf("After p = p + 2  (p)      = %p\n", p);
    printf("Value at new p (*p)       = %d\n\n", *p);
    p = p - 1;
    printf("After p = p - 1  (p)      = %p\n", p);
    printf("Value at new p (*p)       = %d\n", *p);
}
```
## 6)Write a program to declare an integer variable a, assign it a value, then declare a pointer
variable, assign it the address of a, and finally print the value of a using the pointer variable.
```c
#include <stdio.h>
int main() {
    int a = 25;     
    int *p;       
    p = &a;         
    printf("Value of a (using pointer) = %d\n", *p);
}
```
## 7)Write a program to print postfix/prefix increment/decrement in a pointer variable of base
type int*.
```c
#include <stdio.h>
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *p = arr;  
    printf("Initial pointer (p) address: %p, value: %d\n", p, *p);
    printf("\np++  : address = %p, value = %d\n", p++, *p);
    printf("++p  : address = %p, value = %d\n", ++p, *p);
    printf("\np--  : address = %p, value = %d\n", p--, *p);
    printf("--p  : address = %p, value = %d\n", --p, *p);
}
```
## 8)Write a Program to print the value and address of elements of an array using pointers
notation.
```c
#include <stdio.h>
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *p;
    int i;
    p = arr;  
    printf("Value\tAddress\n");
    printf("-------------------------\n");
    for (i = 0; i < 5; i++) {
        printf("%d\t%p\n", *(p + i), (p + i));
    }
}
```
## 9)Write a program to print the value of array elements using pointers and subscript notation.
```c
#include <stdio.h>
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *p = arr;
    int i;
    printf("Using Pointer Notation:\n");
    for (i = 0; i < 5; i++) {
        printf("*(p + %d) = %d\n", i, *(p + i));
    }
    printf("\nUsing Subscript Notation:\n");
    for (i = 0; i < 5; i++) {
        printf("arr[%d] = %d\n", i, arr[i]);
    }
}
```
## 10)Write a program to print the value and address of array elements by subscripting a pointer
variable.
```c
#include <stdio.h>
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int *p;
    p=arr;
    printf("Value\tAddress\n");
    printf("---------------------------\n");
    for (i = 0; i < 5; i++) {
        printf("%d\t%p\n", p[i], &p[i]);
    }
}
```
## 11)Program to understand the difference between a to an integer and a pointer to an array of
integers.
```c
#include <stdio.h>
int main() {
    int a = 10;  
    int arr[5] = {1, 2, 3, 4, 5};
    int *p1;               
    int (*p2)[5]; 
    p1 = arr;              
    p2 = &arr;            
    printf("Integer a = %d\n", a);
    printf("Address of a = %p\n\n", &a);
    printf("Array base address (arr) = %p\n", arr);
    printf("Value of p1 (points to first element) = %p\n", p1);
    printf("Value pointed by p1 (*p1) = %d\n\n", *p1);

    printf("Address stored in p2 (pointer to whole array) = %p\n", p2);
    printf("Address of the entire array (&arr) = %p\n\n", &arr);

    printf("First element using p2: (*p2)[0] = %d\n", (*p2)[0]);
    printf("Second element using p2: (*p2)[1] = %d\n", (*p2)[1]);
}
```
## 12)Write a program to dereference a pointer to an array.
```c
#include <stdio.h>
int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int (*ptr)[5];
    ptr = &arr;
    printf("Accessing array elements using pointer to array:\n");
    for (int i = 0; i < 5; i++) {
        printf("Element %d = %d\n", i, (*ptr)[i]);
    }
}
```
## 13)Write a program to print the values and address of elements of 2-d array.
```c
#include <stdio.h>
int main() {
    int arr[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
    printf("Values and addresses of 2-D array elements:\n\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("arr[%d][%d] = %d\t", i, j, arr[i][j]);
            printf("Address = %p\n", (void*)&arr[i][j]);
        }
        printf("\n");
    }
}
```
## 14)Program to print elements of a 2-D array by subscripting a pointer to an array variable.
```c
#include <stdio.h>
int main() {
    int arr[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };
    int (*p)[3];
    p = arr;
    printf("Printing 2-D array elements using pointer to an array:\n\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++){
            printf("%d ", p[i][j]);
        }
        printf("\n");
    }
}
```
## 15)Program to print elements of a 3-D array using pointer notation.
```c
#include <stdio.h>
int main() {
    int arr[2][2][3] = {
        {
            {1, 2, 3},
            {4, 5, 6}
        },
        {
            {7, 8, 9},
            {10, 11, 12}
        }
    };
    int *p = &arr[0][0][0];   
    int total = 2 * 2 * 3;    
    printf("Elements of the 3-D array using pointer notation:\n\n");
    for (int i = 0; i < total; i++) {
        printf("%d ", *(p + i)); 
    }
}
```
