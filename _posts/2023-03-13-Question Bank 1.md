---
title: Question Bank-1 | ACP
date: 2023-03-13 00:00:00 
categories: [Advance Computer Programming ]
tags: [question bank,question bank 1]     # TAG names should always be lowercase
---

## Q1 What is an array? What are the advantages of using an array? Write characteristic of an Array.

Array is useful concept for representing a group of similar values under a single
name. Thus, array can be defined simply as a group of values of same type.

### Advantages of an Array:
1 Create arrays with small items: It's best to learn about arrays using small physical items to model the dimensions.

2 Use computer software: It's best to develop your knowledge about array functioning by learning about them within a computer programming network. You can use software to model your arrays digitally.

3 Develop your knowledge of coding languages: It's best to use a specific coding language, like Python, Java, or C#, depending on your preferred software. Understanding these languages can help you apply your data elements to an array in a particular coding software.

### Characteristic of an Array
1) An array holds elements that have the same data type.

2) Array elements are stored in subsequent memory locations.

3) Two-dimensional array elements are stored row by row in subsequent memory locations.

4) Array name represents the address of the starting element.

5) Array size should be mentioned in the declaration. Array size must be a constant expression and not a variable.

## Q2 Explain initialization and working of single dimensional array with example.

Array represents a group of similar values under a single name. The C programming allows
user to define one-dimensional array as follows.

for example:
``` c
type array_name[size];
int a[10];
```
where a is the name of the array of 10 integers.

Individual elements of an array are accessed using the subscripted variables. A subscripted
variable consists of array name and the position of the element in the array.

For example, a[i] denotes the ith element in the array a. As subscript or index starts from 0 in
the C programming, the individual elements of the above array are denoted as a[0], a[1],
a[2], ….., a[9].

The a[0] shows the first element, while a[9] shows the last element in array.

These subscripted variables are used in programming just like normal variables

The individual elements of an array are assigned values as like the normal variables. For example,
statement
x=5;

Assign 5 to variable x. similarly,
``` c
a[5] = 25;
```
Store 25 at 6th position in array a. Assume that all 10 elements of the array a is assigned the values
as follows.
``` c
a[0] = 3;
a[1] = 8;
a[2] = 11;
a[3] = 6;
a[4] = 18;
a[5] = 10;
a[6] = 25;
a[7] = 29;
a[8] = 30;
a[9] = 50;
```

## Q3 What is two-dimensional array? Give its declaration and various ways to initialize them.

Two-dimensional arrays are used to represent the two-dimensional structures
like matrix, tables etc. The two-dimensional array is declared as follows.
``` c
type array_name[row_size][column_size];
```
where row_size denotes total number of rows and column_size denotes the total number of columns.Two dimensional array can also be initialized at the time of declaration. Following statement
``` c
int a[2][2] = {0, 0, 1, 1};
```
initializes both the elements of the first row by o and second row by 1. The above is same as
``` c
int a[2][2] = { {0, 0/}, {1, 1}};
```
The same is written as follows in more readable fashion.
``` c
    int a[2][2] = {
        {0, 0},
        {1, 1}
        };
```
If sufficient values are not provided, remaining are initialized with zeros. For examples,
``` c 
    int a[3][3] = { {1,2},
    {3}
    };
```
initializes the last element of first row, last two elements of second row and whole third row by
zeros. For initializing all the elements of two-dimensional array by zeros, the following is more
convenient.
```c 
int a[4][3] = { {0}, {0}, {0}, {0}};
```
## Q4 What is a string? How does C store strings?

Strings are used to represent non-numeric information like name of a person, address etc. Strings are made up of the sequence of characters.

A string is sequence of characters. Strings are useful to store the non-numerical
quantities such as name, address etc. The C stores the characters as ASCII value in
memory. Hence, internally string is a sequence of ASCIIs, Each string in C is ended
with the special character called null character and denoted as ‘\0’ or NULL,

For example string “hello” is stored as

| 'h' | 'e' | 'l' | 'l' | 'o' | '\o' |

## Q5 How to declare and initialize the string. Explain with example.

The string is declared as follows
``` c
char s[10];
```

where s is a string which can store maximum 9 characters as one byte is needed
to store the ‘\0’ character. The string can also be initialized at the time of
declaration as follows.
``` c
char city[7] = {'R', 'a', 'j', 'k', 'o', 't', '\0'};
```
In above, the size is not compulsory and if not given, compiler automatically
computes and puts it.

## Q6 What is string? What are the operation that can be performed on string?

## Q7 Explain various string handling operations available in ‘C’ with example.

## Q8 What is sscanf() function explain with syntax & examples.

The C library function int sscanf(const char *str, const char *format, ...) reads formatted
input from a string.

### Syntax
``` c
int sscanf(const char *str, const char *format, ...)
```
### Parameters
* str − This is the C string that the function processes as its source to retrieve the data.
* format − This is the C string that contains one or more of the following items: Whitespace
character, Non-whitespace character and Format specifiers
* A format specifier follows this prototype: [=%[*][width][modifiers]type=]

### Example

``` c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
void main ()
{
    int day, year; char weekday[20], month[20], dtm[100];
        strcpy( dtm, "Saturday March 25 1989" );
        sscanf( dtm, "%s %s %d %d", weekday, month, &day, &year );
        printf("%s %d, %d = %s\n", month, day, year, weekday );
}
```

### Output
``` output
March 25, 1989 = Saturday
```

## Q9 What is sprint() function explain with syntax & examples.
The C library function int sprintf(char *str, const char *format, ...) sends formatted
output to a string pointed to, by str.

### Syntax
``` c
int sprintf(char *str, const char *format, ...)
```
### Parameters
* str − This is the pointer to an array of char elements where the resulting C string is stored.
* format − This is the String that contains the text to be written to buffer. It can optionally
contain embedded format tags that are replaced by the values specified in
subsequent additional arguments and formatted as requested. Format tags prototype:
%[flags][width][.precision][length]specifier,other arguments − This function expects a
sequence of pointers as additional arguments, each one pointing to an object of the
type specified by their corresponding %-tag within the format string, in the same order

### Example
``` c
#include <stdio.h>
#include <math.h>
void main ()
{
    char str[80];
        sprintf(str, "Value of Pi = %f", M_PI);
        puts(str);
}
```
## Q10 What is the drawbacks of linear array.

### Disadvantages of Arrays
* The number of elements to be stored in an array should be known in advance.
* An array is a static structure (which means the array is of fixed size). Once declared the size of the array cannot be modified. The memory which is allocated to it cannot be increased or decreased.
* Insertion and deletion are quite difficult in an array as the elements are stored in consecutive memory locations and the shifting operation is costly.
* Allocating more memory than the requirement leads to a wastage of memory space and less allocation of memory also leads to a problem.