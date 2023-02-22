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
### Code
``` c
#include <stdio.h>
#define MAX_SIZE 100

void main()
{
    int arr[MAX_SIZE]; 
    int i, n;

    printf("Enter size of array: ");
    scanf("%d", &n);

    printf("Enter %d elements in the array : \n", n);
    for(i=1; i<=n; i++)
    {
        printf("Element %d = ", i);
        scanf("%d", &arr[i]);
    }
    
    printf("\nElements in array are: ");
    for(i=1; i<=n; i++)
    {
        printf("%d, ", arr[i]);
    }
}
```

### Output
```
Element 1 = 2
Element 2 = 4
Element 3 = 6
Element 4 = 46
Element 5 = 4

Elements in array are: 2, 4, 6, 46, 4,
```
## Q3 Write a C program to input elements in array and print all negative elements. How to display all negative elements in array using loop in C program. 

### Code
``` c
#include <stdio.h>
#define MAX_SIZE 100 

void main()
{
    int arr[MAX_SIZE]; 
    int i, n;

    printf("Enter size of the array : ");
    scanf("%d", &n);
    
    for(i=1; i<=n; i++)
    {
        printf("Enter %d elements in the array :: ", n);
        scanf("%d", &arr[i]);
    }

    printf("\nAll negative elements in array are : ");
    for(i=1; i<=n; i++)
    {
        if(arr[i] < 0)
        {
            printf("%d\t", arr[i]);
        }
    }
}
```

### Output

```
Enter size of the array : 4
Enter 4 elements in the array :: -3
Enter 4 elements in the array :: -5
Enter 4 elements in the array :: 3
Enter 4 elements in the array :: 3

All negative elements in array are : -3 -5
```

## Q4 Write a C program to input elements in array and copy all elements of first array into second array.

### Code
``` c
#include <stdio.h>
#define MAX_SIZE 100

void main()
{
    int original[MAX_SIZE], copy[MAX_SIZE];
    int i, size;

    printf("Enter the size of the array : ");
    scanf("%d", &size);
    
    printf("Enter elements of Original array : \n");
    for(i=1; i<=size; i++)
    {
        printf("Enter %d elements in the array :: ", i);
        scanf("%d", &original[i]);
    }

    for(i=1; i<=size; i++)
    {
        copy[i] = original[i];
    }

    printf("\nElements of Original array are : ");
    for(i=1; i<=size; i++)
    {
        printf("%d, ", original[i]);
    }

    printf("\nElements of Copy array are : ");
    for(i=1; i<=size; i++)
    {
        printf("%d, ", copy[i]);
    }
}
```

### Output

``` 
Enter the size of the array : 3
Enter elements of Original array :
Enter 1 elements in the array :: 3
Enter 2 elements in the array :: 4
Enter 3 elements in the array :: 4

Elements of Original array are : 3, 4, 4,
Elements of Copy array are : 3, 4, 4,
```

## Q5 Write a C program to insert element in array at specified position. C program to insert element in array at given position.

### Code
``` c
#include <stdio.h>
#define MAX_SIZE 100

void main()
{
    int arr[MAX_SIZE];
    int i, size, n, pos;

    printf("Enter size of the array : ");
    scanf("%d", &size);

    printf("Enter elements in array : ");
    for(i=0; i<size; i++)
    {
        scanf("%d", &arr[i]);
    }

    printf("Enter element to insert : ");
    scanf("%d", &n);
    printf("Enter the element position : ");
    scanf("%d", &pos);

    if(pos > size+1 || pos <= 0)
    {
        printf("Invalid position! Please enter position between 1 to %d", size);
    }
    else
    {
        for(i=size; i>=pos; i--)
        {
            arr[i] = arr[i-1];
        }
        
        arr[pos-1] = n;
        size++; 

        printf("Array elements after insertion : ");
        for(i=0; i<size; i++)
        {
            printf("%d, ", arr[i]);
        }
    }
}
```

### Output

```
Enter size of the array : 3
Enter elements in array : 1 2 3
Enter element to insert : 4
Enter the element position : 3
Array elements after insertion : 1, 2, 4, 3,
```

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