# Ex 1(D) Evaluation of prefix expression
## DATE: 03.03.2025
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm

1.Start the program and include stdio.h, string.h, and ctype.h.

2.Define a stack with push and pop functions to store integers.

3.Create evalprefix function to evaluate a prefix expression from right to left.

4.For each character, if it’s an operator (+ or *), pop two operands, perform the operation, and push the result back.

5.If it’s a digit, convert it to integer and push it onto the stack.

6.After processing, pop and print the final result.

  

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

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
int a,b,c,i;
for(i=strlen(p)-1;i>=0;i--)
{
if(p[i]=='+')
{
a=pop();
b=pop();
c=a+b;
push(c);
}
else if(p[i]=='*')
{
a=pop();
b=pop();
c=a*b;
push(c);
}
else
{
push(p[i]-48);
}
}
printf("%d",pop());
}

```

## Output:
![image](https://github.com/user-attachments/assets/26c180b4-5fd8-4867-812f-53d795d0d9c5)


## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
