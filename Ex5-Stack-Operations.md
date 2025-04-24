# Ex5 Stack Operations
## DATE:
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```

Program to perform push and pop operation of the stack in the infix to postfix conversion.
Developed by: Krishna Prasad S
RegisterNumber:  212223230108

```
```c

#include<stdio.h>

char stack[100];
int top = -1;

void push(char x)
{
   top++;
   stack[top] = x;
}

char pop()
{
   if(top == -1)
   {
       printf("Stack Underflow");
   }
   else
   {
       return stack[top--];
   }
   return -1;
}

```
## Output:



## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
