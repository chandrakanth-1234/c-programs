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
