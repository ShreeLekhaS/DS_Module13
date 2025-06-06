# EX 1(A) Display operator precedence in the infix expression.
## DATE: 22.02.2025
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm

1.Start the program.

2.Include the required libraries (stdio.h, string.h).

3.Define a function priority to return the priority level of a given operator.

4.Store the expression (A*B)^C+(D%H)/F&G in a character array.

5.Loop through each character of the expression.

6.Check if the character is an operator, then get its priority and print the corresponding priority level.

7.End the program.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Shree Lekha.S
RegisterNumber: 212223110052 
*/

#include <stdio.h>
#include<string.h>

    int priority(char x)
{
   if(x=='^')
   return 1;
   if(x=='*'||x=='%'||x=='/')
   return 2;
   if(x=='+'||x=='-')
   return 3;
   if(x=='&')
   return 4;
   else
   return 0;
}
int main()
{
   int i,j;
   char x;
   char ch[100]="(A*B)^C+(D%H)/F&G";
   for(i=0;i<strlen(ch);i++)
   {
       for(j=0;j<strlen(ch);j++)
       {
           if(ch[i]=='^'||ch[i]=='*'||ch[i]=='%'||ch[i]=='/'||ch[i]=='+'||ch[i]=='-'||ch[i]=='&')
       {
           x=ch[i];
           if(priority(x)==1)
           {
               printf("%c  ----> Highest Priority\n",x);
               break;
           }
           if(priority(x)==2)
           {
               printf("%c  ----> Second Highest Priority\n",x);
               break;
           }
           if(priority(x)==3)
           {
              printf("%c  ----> Second Lowest Priority\n",x);
              break;
           }
           if(priority(x)==4)
           {
             printf("%c  ----> Lowest Priority\n",x);
             break;
           }
       } 
       }
   }
    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/229f7cf8-0b1a-4d95-914c-5e547e8f2c95)

## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
