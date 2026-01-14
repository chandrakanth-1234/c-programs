### 1)Which is not a bitwise operator?

1. `&`
2. `|`
3. `<<`
4. `&&`

✅ Answer: 4.`&&`

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

### 📝Explanation: 

a=10->Binary:1010

b=2->Binary:0010

c=(a&b)=(1010 & 0010)=0010 

Decimal value of 0010 is 2.

---
