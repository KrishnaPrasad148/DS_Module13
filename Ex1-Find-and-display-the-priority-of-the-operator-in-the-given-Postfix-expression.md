# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```

Program to find and display the priority of the operator in the given Postfix expression
Developed by: Krishna Prasad S
RegisterNumber:  212223230108

```
```c

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
  else if(x == '*' || x == '/')
  {
      return 3;
  }
  else if(x == '^')
  {
      return 4;
  }
  return -1;
}

```
## Output:



## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
