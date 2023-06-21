# C Programming Questions using Pointers

1. Write a program to swap two numbers using pointers.

```C
#include <stdio.h>
 
int main()
{
   int x, y, *a, *b, temp;
 
   printf("Enter the value of x and y\n");
   scanf("%d%d", &x, &y);
 
   printf("Before Swapping\nx = %d\ny = %d\n", x, y);
 
   a = &x;
   b = &y;
 
   temp = *b;
   *b = *a;
   *a = temp;
 
   printf("After Swapping\nx = %d\ny = %d\n", x, y);
 
   return 0;
}
```

2. Write a program to calculate the sum of elements in an array using pointers.

```C
#include<stdio.h>
#include<stdlib.h>

int main()
{
    int i, n, sum =0;
    int *ptr;
    printf("Enter size of array :");
    scanf("%d", &n);
    ptr = (int *) malloc(n * sizeof(int));

    printf("Enter elements in the list\n");
    for(i=0;i<n;i++)
    {
        printf("Enter element %d :",i);
        scanf("%d", ptr + i);
    }

    for(i=0;i<n;i++)
    {
        sum = sum + *(ptr+i);
    }

    printf("Sum of all elements in an array is = %d", sum);

    return 0;
}
```

3. Write a program to reverse a string using pointers.

```C
#include<stdio.h>
#include<string.h>

int str_len(char *st);
void revstr(char *st);

int main()
{
    char st[50];
    printf("Enter the string to be reversed :");
    scanf("%s", &st);

    revstr(st);

    printf("The reverse string is: %s", st);
    return 0;
}

void revstr(char *st)
{
    int len,i;
    char *start, *end, temp;

    len = str_len(st);
    start = st;
    end = st;

    for(i=0;i<len;i++)
    {end++;}

    for(i=0; i<len/2; i++)
    {
        temp = *end;
        *end = *start;
        *start = temp;

        start++;
        end--;
    }
}

int str_len(char *st)
{
    int i = 0;
    while(*(ptr+i)!='\0')
    {i++;}
    return i;
}
```

4. Write a program to find the length of a string using pointers.

```C
#include<stdio.h>

int main() {
  char str[20], *pt;
  int i = 0;
  printf("Pointer Example Program : Find or Calculate Length of String \n");
  printf("Enter Any string [below 20 chars] : ");
  gets(str);
  pt = str;
  while (*pt != '\0') {
    i++;
    pt++;
  }
  printf("Length of String : %d", i);

  return 0;
}
```

5. Write a program to find the largest and smallest elements in an array using pointers.

```C
// C program for the above approach
#include <stdio.h>
#include <stdlib.h>
 
// Function to find the largest element
// using dynamic memory allocation
void findLargest(int* arr, int N)
{
    int i;
 
    // Traverse the array arr[]
    for (i = 1; i < N; i++) {
        // Update the largest element
        if (*arr < *(arr + i)) {
            *arr = *(arr + i);
        }
    }
 
    // Print the largest number
    printf("%d ", *arr);
}
 
// Driver Code
int main()
{
    int i, N = 4;
 
    int* arr;
 
    // Memory allocation to arr
    arr = (int*)calloc(N, sizeof(int));
 
    // Condition for no memory
    // allocation
    if (arr == NULL) {
        printf("No memory allocated");
        exit(0);
    }
 
    // Store the elements
    *(arr + 0) = 14;
    *(arr + 1) = 12;
    *(arr + 2) = 19;
    *(arr + 3) = 20;
 
    // Function Call
    findLargest(arr, N);
    return 0;
}
```

6. Write a program to copy a string using pointers.

```C
#include<stdio.h>

void copy_string(char*, char*);

main()
{
    char source[100], target[100];    
    printf("Enter source string\n");    
    gets(source);    
    copy_string(target, source);    
    printf("Target string is \"%s\"\n", target);    
    return 0;
}

void copy_string(char *target, char *source)
{
    while(*source)
    {
        *target = *source;        
        source++;        
        target++;
    }    
    *target = '\0';
}

```

7. Write a program to concatenate two strings using pointers.

```C
#include <stdio.h>

int main()
{
    printf("\n\n\t\tStudytonight - Best place to learn\n\n\n");
    char aa[100], bb[100];

    printf("\nEnter the first string: ");
    gets(aa);   // inputting first string

    printf("\nEnter the second string to be concatenated: ");
    gets(bb);   // inputting second string

    char *a = aa;
    char *b = bb;

    // pointing to the end of the 1st string
    while(*a)   // till it doesn't point to NULL-till string is not empty
    {
        a++;    // point to the next letter of the string
    }
    while(*b)   // till second string is not empty
    {
        *a = *b;
        b++;
        a++;
    }
    *a = '\0';  // string must end with '\0'
    printf("\n\n\nThe string after concatenation is: %s ", aa);
    printf("\n\n\t\t\tCoding is Fun !\n\n\n");
    return 0;
}
```

8. Write a program to delete an element from an array using pointers.

```C
#include<stdio.h>
#include<stdlib.h>
void delete(int n,int *a,int pos);

int main()
{
   int *a,n,i,pos;
   printf("enter the size of array:");
   scanf("%d",&n);
   a=(int*)malloc(sizeof(int)*n);
   printf("enter the elements:");
   for(i=0;i<n;i++)
   {
      scanf("%d",(a+i));
   }
   printf("enter the position of element to be deleted:");
   scanf("%d",&pos);
   delete(n,a,pos);
   return 0;
}

void delete(int n,int *a,int pos){
   int i,j;
   if(pos<=n)
   {
      for(i=pos-1;i<n;i++)
      {
         j=i+1;
         *(a+i)=*(a+j);
      }
      printf("after deletion the array elements is:");
      for(i=0;i<n-1;i++)
      {
         printf("%d\t",(*(a+i)));
      }
   }
   else{
      printf("Invalid Input");
   }
}
```

9. Write a program to insert an element in an array using pointers.

```C
#include<stdio.h>
#include<stdlib.h>

void insert(int n1, int *a, int len, int ele)
{
   int i;
   printf("Array elements after insertion is:");
   for(i=0;i<len-1;i++)
   {
      printf("%d",*(a+i));
   }
   printf("%d",ele);
   for(i=len-1;i<n1;i++)
   {
      printf("%d",*(a+i));
   }
}

int main()
{
   int *a,n1,i,len,ele;
   printf("enter size of array elements:");
   scanf("%d",&n1);
   a=(int*)malloc(n1*sizeof(int));
   printf("enter the elements:");
   for(i=0;i<n1;i++)
   {
      scanf("%d",a+i);
   }
   printf("enter the position where the element need to be insert:");
   scanf("%d",&len);
   if(len<=n1)
   {
      printf("enter the new element that to be inserted:");
      scanf("%d",&ele);
      insert(n1,a,len,ele);
   }
   else
   {
      printf("Invalid Input");
   }
   return 0;
}
```

10. Write a program to sort an array using pointers.

```C
#include <stdio.h> 
  
// Function to sort the numbers using pointers 
void sort(int n, int* ptr) 
{ 
    int i, j, t; 
  
    // Sort the numbers using pointers 
    for (i = 0; i < n; i++) { 
  
        for (j = i + 1; j < n; j++) { 
  
            if (*(ptr + j) < *(ptr + i)) { 
  
                t = *(ptr + i); 
                *(ptr + i) = *(ptr + j); 
                *(ptr + j) = t; 
            } 
        } 
    } 
  
    // print the numbers 
    for (i = 0; i < n; i++) 
        printf("%d ", *(ptr + i)); 
} 
  
// Driver code 

int main() 
{ 
    int n = 5; 
    int arr[] = { 0, 23, 14, 12, 9 }; 
  
    sort(n, arr); 
  
    return 0; 
}
```

11. Write a program to count the number of vowels in a string using pointers.

```C

```

12. Write a program to count the number of words in a string using pointers.

```C

```

13. Write a program to find the first occurrence of a character in a string using pointers.

```C

```

14. Write a program to find the last occurrence of a character in a string using pointers.

```C

```

15. Write a program to find the middle element of an array using pointers.

```C

```

16. Write a program to reverse an array using pointers.

```C

```

17. Write a program to check if a string is a palindrome using pointers.

```C

```

18. Write a program to find the factorial of a number using pointers.

```C

```

19. Write a program to check if a number is prime or not using pointers.

```C

```

20. Write a program to find the GCD and LCM of two numbers using pointers.

```C

```

21. Write a program to convert a decimal number to binary using pointers.

```C

```

22. Write a program to convert a binary number to decimal using pointers.

```C

```

23. Write a program to find the power of a number using pointers.

```C

```

24. Write a program to print the Fibonacci series using pointers.

```C

```

25. Write a program to find the sum of the digits of a number using pointers.

```C

```

26. Write a program to check if a number is Armstrong number or not using pointers.

```C

```

27. Write a program to find the maximum and minimum of three numbers using pointers.

```C

```

28. Write a program to check if a number is even or odd using pointers.

```C

```

29. Write a program to find the average of numbers in an array using pointers.

```C

```

30. Write a program to find the second largest and second smallest elements in an array using pointers.

```C

```
