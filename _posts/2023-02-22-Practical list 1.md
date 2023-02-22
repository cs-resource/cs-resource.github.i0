---
title: Advance Computer Programming Practical list - 1
date: 2023-02-22 00:00:00 
categories: [Advance Computer Programming ]
tags: [practical list - 1]     # TAG names should always be lowercase
---

## Q1 Write a C program to declare an array capable of storing 10 student marks. Input marks of all 10 students and find their average.
### Code
```c
#include <stdio.h>

void main()
{
    int n[11];
    int i,j,sum=0;
    float avg;
   
    for ( i = 1; i <= 10; i++ ) {
        printf("Enter The Marks for %d Student :: ",i);
        scanf("%d",&n[i]);
        sum = sum + n[i];
    }

    avg = sum/10;
    printf("\nAverage of all 10 Students marks is :: %.2f",avg);
}
```

### Output
```
Enter The Marks for 1 Student :: 50
Enter The Marks for 2 Student :: 25
Enter The Marks for 3 Student :: 50
Enter The Marks for 4 Student :: 25
Enter The Marks for 5 Student :: 50
Enter The Marks for 6 Student :: 25
Enter The Marks for 7 Student :: 50
Enter The Marks for 8 Student :: 25
Enter The Marks for 9 Student :: 50
Enter The Marks for 10 Student :: 25

Average of all 10 Students marks is :: 37.00
```
## Q2 Write a C program to declare, initialize, input elements in array and print array. How to input and display elements in an array using for loop in C programming. C program to input and print array elements using loop.

## Q3 Write a C program to input elements in array and print all negative elements. How to display all negative elements in array using loop in C program. 

## Q4 Write a C program to input elements in array and copy all elements of first array into second array.

## Q5 Write a C program to insert element in array at specified position. C program to insert element in array at given position.

## Q6 Write a C program to delete element from array at specified position. How to remove element from array at given position in C programming.

## Q7 Write a C program to input elements in two array and merge two array to third array.

## Q8 Write a C program to input elements in array and find reverse of array.

## Q9 Write a C program to input elements in array and search whether an element exists in array or not.

## Q10 Write a C program to input elements in array and sort array elements in ascending or descending order.

## Q11 Write a C program to read elements in two matrices and add elements of both matrices.

## Q12 Write a C program to read elements in two matrices and find the difference of two matrices.

## Q13 Write a C program to enter elements in two matrices and check whether both matrices are equal or not.

## Q14 Write a C program to read elements in a matrix and find transpose of the given matrix.

## Q15 Write a C program to find length of a string using loop. How to find length of a string without using in-built library function strlen() in C programming.