# Ex4 Evaluation of prefix expression
## DATE:
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```

Program to evaluate the given prefix expression
Developed by: Krishna Prasad S
RegisterNumber:  212223230108

```
```c

#include<stdio.h>
#include<string.h>
#include<ctype.h>

int s[50];
int top=0;

void push(int ch)
{
	top++;
	s[top]=ch;
}

int pop()
{
	int ch;
	ch=s[top];
	top=top-1;
	return(ch);
}

void evalprefix(char p[50])
{
    int num1, num2, result;
    int len = strlen(p) - 1;
    while(len >= 0)
    {
        if(isdigit(p[len]))
        {
            push(p[len] - '0');
        }
        else
        {
            num1 = pop();
            num2 = pop();
            switch(p[len])
            {
                case '+':
                    result = num1 + num2;
                    break;
                case '-':
                    result = num1 - num2;
                    break;
                case '*':
                    result = num1 * num2;
                    break;
                case '/':
                    result = num1 / num2;
                    break;
                case '^':
                    result = num1 ^ num2;
                    break;
            }
            push(result);
        }
        len--;
    }
    printf("%d", pop());
}

int  main()
{
    char str[] = "+-2*341";
    evalprefix(str);
    return 0;
}

```

## Output:



## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
