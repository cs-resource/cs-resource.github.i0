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

### Code
``` c
#include <stdio.h>
#define MAX_SIZE 100

int main()
{
    int arr[MAX_SIZE];
    int i, size, pos;

    printf("Enter size of the array : ");
    scanf("%d", &size);
    printf("Enter elements in array : ");
    for(i=0; i<size; i++)
    {
        scanf("%d", &arr[i]);
    }

    printf("Enter the element position to delete : ");
    scanf("%d", &pos);


    if(pos < 0 || pos > size)
    {
        printf("Invalid position! Please enter position between 1 to %d", size);
    }
    else
    {
        for(i=pos-1; i<size-1; i++)
        {
            arr[i] = arr[i + 1];
        }

        size--;

        printf("\nElements of array after delete are : ");
        for(i=0; i<size; i++)
        {
            printf("%d, ", arr[i]);
        }
    }
}
```

### Output

```
Enter size of the array : 5
Enter elements in array : 1 2 3 4 6
Enter the element position to delete : 5

Elements of array after delete are : 1, 2, 3, 4
```

## Q7 Write a C program to input elements in two array and merge two array to third array.

### Code 

``` c
#include <stdio.h>
#define MAX_SIZE 100      

void main()
{
    int arr1[MAX_SIZE], arr2[MAX_SIZE], mergeArray[MAX_SIZE * 2];
    int size1, size2, mergeSize;
    int index1, index2, mergeIndex;
    int i;
     
    printf("Enter the size of first array : ");
    scanf("%d", &size1);

    printf("Enter elements in first array : ");
    for(i=0; i<size1; i++)
    {
        scanf("%d", &arr1[i]);
    }

    printf("\nEnter the size of second array : ");
    scanf("%d", &size2);

    printf("Enter elements in second array : ");
    for(i=0; i<size2; i++)
    {
        scanf("%d", &arr2[i]);
    }


    mergeSize = size1 + size2;

    index1 = 0;
    index2 = 0;
    for(mergeIndex=0; mergeIndex < mergeSize; mergeIndex++)
    {
        if(index1 >= size1 || index2 >= size2)
        {
            break;
        }


        if(arr1[index1] < arr2[index2])
        {
            mergeArray[mergeIndex] = arr1[index1];
            index1++;
        }
        else
        {
            mergeArray[mergeIndex] = arr2[index2];
            index2++;
        }
    }

    while(index1 < size1)
    {
        mergeArray[mergeIndex] = arr1[index1];
        mergeIndex++;
        index1++;
    }
    while(index2 < size2)
    {
        mergeArray[mergeIndex] = arr2[index2];
        mergeIndex++;
        index2++;
    }


    
    printf("\nArray merged in ascending order : ");
    for(i=0; i<mergeSize; i++)
    {
        printf("%d, ", mergeArray[i]);
    }
}
```

### Output

```
Enter the size of first array : 5
Enter elements in first array : 1 2 3 4 5

Enter the size of second array : 5
Enter elements in second array : 6 7 8 9 10

Array merged in ascending order : 1, 2, 3, 4, 5, 6, 7, 8, 9, 10,
```
## Q8 Write a C program to input elements in array and find reverse of array.

### Code

``` c
#include <stdio.h>
#define MAX_SIZE 100   

int main()
{
    int arr[MAX_SIZE];
    int size, i;

    printf("Enter size of the array: ");
    scanf("%d", &size);

    printf("Enter elements in array: ");
    for(i=0; i<size; i++)
    {
        scanf("%d", &arr[i]);
    }

    printf("\nArray in reverse order: ");
    for(i = size-1; i>=0; i--)
    {
        printf("%d, ", arr[i]);
    }

    return 0;
}
```

### Output

```
Enter size of the array: 5
Enter elements in array: 1 2 3 4 5

Array in reverse order: 5, 4, 3, 2, 1,
```
## Q9 Write a C program to input elements in array and search whether an element exists in array or not.

### Code

``` c
#include <stdio.h>

#define MAX_SIZE 100  

void main()
{
    int arr[MAX_SIZE];
    int size, i, toSearch, found;

    printf("Enter size of array: ");
    scanf("%d", &size);

    printf("Enter elements in array: ");
    for(i=0; i<size; i++)
    {
        scanf("%d", &arr[i]);
    }

    printf("\nEnter element to search: ");
    scanf("%d", &toSearch);

    found = 0; 
    
    for(i=0; i<size; i++)
    {
        if(arr[i] == toSearch)
        {
            found = 1;
            break;
        }
    }

    if(found == 1)
    {
        printf("\n%d is found at position %d", toSearch, i + 1);
    }
    else
    {
        printf("\n%d is not found in the array", toSearch);
    }
}
```

### Output

```
Enter size of array: 5
Enter elements in array: 1 2 3 4 5

Enter element to search: 3

3 is found at position 3
```
## Q10 Write a C program to input elements in array and sort array elements in ascending or descending order.

### Code

``` c
#include <stdio.h>
#define MAX_SIZE 100    

void main()
{
    int arr[MAX_SIZE];
    int size;
    int i, j, temp;

    printf("Enter size of array: ");
    scanf("%d", &size);

    printf("Enter elements in array: ");
    for(i=0; i<size; i++)
    {
        scanf("%d", &arr[i]);
    }

    for(i=0; i<size; i++)
    {
        for(j=i+1; j<size; j++)
        {
            if(arr[i] > arr[j])
            {
                temp     = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }

    printf("\nElements of array in ascending order: ");
    for(i=0; i<size; i++)
    {
        printf("%d, ", arr[i]);
    }
}
```

### Output

```
Enter size of array: 5
Enter elements in array: 5 4 3 2 1

Elements of array in ascending order: 1, 2, 3, 4, 5,
```

## Q11 Write a C program to read elements in two matrices and add elements of both matrices.

### Code
``` c
#include <stdio.h>
#define SIZE 3 

void main()
{
    int A[SIZE][SIZE]; 
    int B[SIZE][SIZE]; 
    int C[SIZE][SIZE]; 

    int row, col;

    printf("Enter elements in matrix A of size 3x3: \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            scanf("%d", &A[row][col]);
        }
    }
    printf("\nEnter elements in matrix B of size 3x3: \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            scanf("%d", &B[row][col]);
        }
    }

    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            C[row][col] = A[row][col] + B[row][col];
        }
    }
    printf("\nSum of matrices A+B = \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            printf("%d ", C[row][col]);
        }
        printf("\n");
    }
}
```

### Output
``` 
Enter elements in matrix A of size 3x3:
1 2 3
4 5 6
7 8 9

Enter elements in matrix B of size 3x3:
9 8 7
6 5 4
3 2 1

Sum of matrices A+B =
10 10 10
10 10 10
10 10 10
```

## Q12 Write a C program to read elements in two matrices and find the difference of two matrices.

### Code
``` c
#include <stdio.h>

#define SIZE 3

int main()
{
    int A[SIZE][SIZE];  
    int B[SIZE][SIZE];  
    int C[SIZE][SIZE];  

    int row, col;

    printf("Enter elements in matrix A of size 3x3: \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            scanf("%d", &A[row][col]);
        }
    }

    printf("\nEnter elements in matrix B of size 3x3: \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            scanf("%d", &B[row][col]);
        }
    }

    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            C[row][col] = A[row][col] - B[row][col];
        }
    }

    printf("\nDifference of two matrices A-B = \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            printf("%d ", C[row][col]);
        }
        printf("\n");
    }
}
```

### Output

```
Input elements in 3x3 matrix1:
1 2 3
4 5 6
7 8 9

Input elements in 3x3 matrix2:
9 8 7
6 5 4
3 2 1

Difference of two matrices A-B =
-8 -6 -4
-2 0 2
4 6 8
```

## Q13 Write a C program to enter elements in two matrices and check whether both matrices are equal or not.

### Code
``` c
#include <stdio.h>
#define SIZE 3

void main()
{
    int A[SIZE][SIZE]; 
    int B[SIZE][SIZE];

    int row, col, isEqual;

    printf("Enter elements in matrix A of size %dx%d: \n", SIZE, SIZE);
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            scanf("%d", &A[row][col]);
        }
    }

    printf("\nEnter elements in matrix B of size %dx%d: \n");
    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            scanf("%d", &B[row][col]);
        }
    }

    isEqual = 1;

    for(row=0; row<SIZE; row++)
    {
        for(col=0; col<SIZE; col++)
        {
            if(A[row][col] != B[row][col])
            {
                isEqual = 0;
                break;
            }
        }
    }

    if(isEqual == 1)
    {
        printf("\nMatrix A is equal to Matrix B");
    }
    else
    {
        printf("\nMatrix A is not equal to Matrix B");
    }
}
```

### Output

```
Enter elements in matrix A of size 3x3:
1 2 3
4 5 6
7 8 9

Enter elements in matrix B of size 6422288x3:
1 2 3
4 5 6
7 8 9

Matrix A is equal to Matrix B
```

## Q14 Write a C program to read elements in a matrix and find transpose of the given matrix.

### Code
``` c
#include <stdio.h>
#define MAX_ROWS 3
#define MAX_COLS 3

int main()
{
    int A[MAX_ROWS][MAX_COLS];  
    int B[MAX_COLS][MAX_ROWS];  

    int row, col;

    printf("Enter elements in matrix of size %dx%d: \n", MAX_ROWS, MAX_COLS);
    for(row=0; row<MAX_ROWS; row++)
    {
        for(col=0; col<MAX_COLS; col++)
        {
            scanf("%d", &A[row][col]);
        }
    }

    for(row=0; row<MAX_ROWS; row++)
    {
        for(col=0; col<MAX_COLS; col++)
        {
            B[col][row] = A[row][col];
        }
    }
    printf("\nOriginal matrix: \n");
    for(row=0; row<MAX_ROWS; row++)
    {
        for(col=0; col<MAX_COLS; col++)
        {
            printf("%d ", A[row][col]);
        }

        printf("\n");
    }
    
    printf("Transpose of matrix A: \n");
    for(row=0; row<MAX_COLS; row++)
    {
        for(col=0; col<MAX_ROWS; col++)
        {
            printf("%d ", B[row][col]);
        }

        printf("\n");
    }
}
```

### Output
```
Enter elements in matrix of size 3x3:
1 2 3
4 5 6
7 8 9

Original matrix:
1 2 3
4 5 6
7 8 9
Transpose of matrix A:
1 4 7
2 5 8
3 6 9
```
## Q15 Write a C program to find length of a string using loop. How to find length of a string without using in-built library function strlen() in C programming.

### Code
``` c
#include <stdio.h>
int main() {
    char s[] = "CS Resource";
    int i;

    for (i = 0; s[i] != '\0'; ++i);
    
    printf("Length of the string: %d", i);
    return 0;
}
```
### Output

```
Length of the string: 11
```
