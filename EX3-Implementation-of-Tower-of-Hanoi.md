# EX3 Implementation of Tower of Hanoi
## DATE:
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```

Program to implement Tower of Hanoi
Developed by: Krishna Prasad S 
RegisterNumber:  212223230108

```
```c
#include<stdio.h>

void TOH(int n,char x,char y,char z)
{
   if(n == 1)
   {
      
      printf("%c to %c\n", x,y);
      return;
   }
   TOH(n-1,x,z,y);
   printf("%c to %c\n", x, y);
   TOH(n-1,z,y,x);
}

int main()
{
   int n = 2;
   TOH(n,'A','B','C');
}

```

## Output:



## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
