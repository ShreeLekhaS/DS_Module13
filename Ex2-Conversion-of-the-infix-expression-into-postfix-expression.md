# Ex 1(B) Conversion of the infix expression into postfix expression
## DATE:
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1.Start the program and include stdio.h and ctype.h.
2.Define stack functions push and pop to manage operators.
3.Create a priority function to assign precedence to operators.
4.Write IntoPost to convert infix to postfix by scanning each character: print operands, push ‘(’, pop on ‘)’, and handle operators based on priority.
5.After scanning, pop and print remaining operators from the stack.
6.In main, initialize the expression and call IntoPost, then end the program.

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

#include<stdio.h>
#include<ctype.h>

char stack[100];
int top = -1;
void push(char x)
{
stack[++top]=x;

}

char pop()
{
if(top==-1) return 0;
else
return stack[top--];
}
int priority(char x)
{
if(x=='(')
{
return 0;
}
if(x=='&'||x=='|')
{
return 1;
}
if(x=='+'||x=='-')
{
return 2;
}
if(x=='*'||x=='/'||x=='%')
{
return 3;
}
if(x=='^')
{
return 4;
}
return 0;
}


char IntoPost(char *exp)
{
char *e,x; e=exp; while(*e!='\0')
{
if(isalnum(*e))
{
printf("%c ",*e);
}
else if(*e=='(')
{
push(*e);
}
else if(*e==')')
{
while((x=pop())!='(') printf("%c ",x);
}
else
{
while(priority(stack[top])>=priority(*e)) printf("%c ",pop());
push(*e);
}
e++;
}
 
while(top != -1)
{
printf("%c ",pop());
}return 0;
}

int main()
{
char exp[100]="3%2+4*(A&B)"; IntoPost(exp);
return 1;
}

```

## Output:

![image](https://github.com/user-attachments/assets/ee5732ab-25e7-46f0-aa6e-dfd09687175e)


## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
