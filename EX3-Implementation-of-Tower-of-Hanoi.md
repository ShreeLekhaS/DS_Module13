# EX 1(C) Implementation of Tower of Hanoi
## DATE:
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1.Start the program and include the stdio.h library.
2.Define a recursive function TOH that moves n disks from source to destination using an auxiliary rod.
3.In TOH, if n is greater than 0, move n-1 disks from source to auxiliary.
4.Print the move of the largest disk from source to destination.
5.Move the n-1 disks from auxiliary to destination.
6.In main, read the number of disks from the user, call TOH with rods labeled 'A', 'B', 'C', then end the program.  

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by:Shree Lekha.S 
RegisterNumber:212223110052 
*/
#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
  if ( n>0)
  {
      TOH(n-1,x,z,y);
      printf("%c to %c\n", x,y);
      TOH(n-1, z,y,x);
  }
  
}
int main()
{
    
    int n= 3;
    scanf("%d", &n);
    TOH(n ,'A', 'B' , 'C');
}

```

## Output:
![image](https://github.com/user-attachments/assets/37144dd9-8555-4d0f-8bf7-09d9b86ed844)



## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
