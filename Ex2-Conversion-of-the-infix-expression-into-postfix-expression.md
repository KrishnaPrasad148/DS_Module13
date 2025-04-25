# Ex2 Conversion of the infix expression into postfix expression
## DATE: 20/02/2025
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. Start the program. 
2. Initialize a stack and set the top index to -1. 
3. Define the push() and pop() functions to add and remove elements from the stack. 
4. Define the priority() function to assign priorities to operators. 
5. Traverse the expression in the IntoPost() function, handling operands, parentheses, and operators. 
6. After processing the expression, pop and print any remaining operators from the stack. 
7. End. 

## Program:
```

Program to convert the infix expression into postfix expression
Developed by: Krishna Prasad S
RegisterNumber:  212223230108

```
```c

#include<stdio.h>
#include<ctype.h>

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
int priority(char x)
{
    if(x == '&' || x == '|')
  {
      return 1;
  }
  else if(x == '+' || x == '-')
  {
      return 1;
  }
  else if(x == '*' || x == '/' || x == '%')
  {
      return 3;
  }
  else if(x == '^')
  {
      return 4;
  }
  return -1;
}
void IntoPost(char *exp)
{
    char *e = exp;
    while(*e != '\0')
    {
        if(isalnum(*e))
        {
            printf("%c ", *e);
        }
        else if(*e == '(')
        {
            push(*e);
        }
        else if(*e == ')')
        {
            while(top != -1 && stack[top] != '(')
            {
                printf("%c ", pop());
            }
            pop();
        }
        else
        {
            while(top != -1 && priority(stack[top]) >= priority(*e))
            {
                printf("%c ", pop());
            }
            push(*e);
        }
        e++;
    }
    
    while(top != -1)
    {
       printf("%c ", pop());
    }
}


int main()
{
    char str[100] = "2*3%(2-1)+5|3" ;
    IntoPost(str);
    return 1;
}

```

## Output:



## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
