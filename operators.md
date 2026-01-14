### 1)Which is not a bitwise operator?

1. `&`
2. `|`
3. `<<`
4. `&&`

✅ Answer: `&&`

📝Explanation: && is a Logical AND operator ,not a bitwise.

---

### 2) Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
 int a=10;
 int b=2;
 int c;
 c=(a & b);
 printf("c= %d",c);
 return 0;
}
```
✅ Output: 2

📝Explanation: 

a=10->Binary:1010

b=2->Binary:0010

c=(a&b)=(1010 & 0010)=0010 

Decimal value of 0010 is 2.

---

### 3) Predict the output of the following program.
```c
#include <stdio.h>
#define MOBILE 0x01
#define LAPPY 0x02
int main()
{
 unsigned char item=0x00;
 item |=MOBILE;
 item |=LAPPY;
 printf("I have purchased ...:");
 if(item & MOBILE){
 printf("Mobile, ");
 }
 if(item & LAPPY){
 printf("Lappy");
 }
 return 1;
}
```
 1. I have purchased ...:
 2. I have purchased ...:Mobile, Lappy
 3. I have purchased ...:Mobile,
 4. I have purchased ...:Lappy

Output: I have purchased ...:Mobile, Lappy

Explanation:

Mobile=0x01->Binary:0001

Lappy=0x02->Binary:0010

item=0x00->Binary:0000

item|=Mobile->0001

item|=Lappy->0011

item&Mobile->True=prints Mobile

item&Lappy->True=prints Lappy

I have purchased ...:Mobile,Lappy

---

### 4) Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
 char var=0x04;
 var = var | 0x04;
 printf("%d,",var);
 var |= 0x01;
 printf("%d",var);

 return 0;
}
```
1. 8,9
2. 4,5
3. 8,8
4. 4,4

Output: 4,5

Explanation:

var=0x04->0100->Decimal=4

var=var|0x04=>0100|0100=>0100->Decimal=4

var|=0x01=>var|0x01=>0100|0001=>0101->Decimal=5

so 4,5

---

### 5) Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
 char flag=0x0f;
 flag &= ~0x02;
 printf("%d",flag);
 return 0;
}
```
 1. 13
 2. d
 3. 22
 4. 1

Output: 13

Explanation:

flag=0x0f=1111->Decimal=15

~0x02=> ~(0010)=>1101

flag&=~0x02=>1111&1101=>1101

Decimal value of 1101 is 13.

--- 

### 6) Consider the given statement:
```c
int x = 10 ^ 2
```
What will be the value of x?
 1. 5
 2. 6
 3. 7
 4. 8

Output: 8

Explanation:

10->Binary=1010

2->Binary=0010

10^2=>1010^0010=>1000

Decimal value of 1000 is 8

---

### 7) Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
 int x=10;
 x &= ~2;
printf("x= %d",x);
 return 0;
}
```
 1. x= 10
 2. x= 8
 3. x= 12
 4. x= 0

Output:x=8

Explanation:

x=10->Binary=1010

~2=> ~(0010)=>1101

x&=~2=>x&~2=>1010&1101=>1000

Decimal value of 1000 is 8

---

### 8) Which Bitwise Operator can be used to check whether a number is EVEN or ODD quickly?
 1. Bitwise AND (&)
 2. Bitwise OR (|)
 3. Bitwise XOR (^)
 4. Bitwise NOT (~)

Output:Bitwise AND

Explanation:

A number is ODD if Least Significant Bit is '1'.

A number is EVEN if Least Significant Bit is '0'.

---
