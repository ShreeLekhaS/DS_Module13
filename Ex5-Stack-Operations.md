# Ex 1(E) Stack Operations
## DATE: 05.03.2025
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm

1.Start the program.

2.Declare a character stack array and initialize the top index to -1.

3.Define push function to add a character to the stack and increment top.

4.Define pop function to remove and return the top character if the stack is not empty.

5.Return -1 from pop if the stack is empty.

6.End the program.

 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Shree Lekha.S
RegisterNumber:212223110052
*/

char stack[100]; 
int top = -1; 
void push(char x) 
{ 
    stack[++top] = x; 
} 
 
char pop() 
{ 
    if(top == -1) 
        return -1; 
    else 
        return stack[top--]; 
} 
```

## Output:

![image](https://github.com/user-attachments/assets/eaa49ad7-dc4f-4985-8368-c884d11b93e2)


## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
