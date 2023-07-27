#30 Basic programming questions in C

1. Write a C program to print "Hello, World!"

```C
#include<stdio.h>

int main()
{
    printf("Hello World!\n");

    return 0;
}
```

2. Write a C program to print the sum of two integers.

```C
#include<stdio.h>

int main()
{
    //Taking the two integers as input from the user
    int n1, n2;
    printf("Enter the first integer here :");
    scanf("%d", &n1);
    printf("Enter the second integer here :");
    scanf("%d", &n2);

    //Creating a variable to hold the value of sum and summin the two numbers and printing it out to the terminal
    int sum;
    sum = n1+n2;

    printf("The sum of the given integers is : %d\n", sum);

    return 0;
}
```

3. Write a C program to find the largest of two numbers.

```C
#include<stdio.h>

int main()
{
    //Taking two numbers as input from the user
    int n1, n2;
    printf("Enter the value of first number :");
    scanf("%d", &n1);
    printf("Enter the value of second number :");
    scanf("%d", &n2);

    //Comparing the numbers and creating conditions so that it can be determined that which number is greater
    if(n1==n2)
    {
        printf("Both numbers are equal\n");
    }
    else if(n1 > n2)
    {
        printf("First number is greater than the second number\n");
    }
    else if(n2 > n1)
    {
        printf("Second number is greater than the first number\n");
    }

    return 0;
}
```

4. Write a C program to find the factorial of a given number.

```C

```

5. Write a C program to check whether a number is even or odd.

```C
#include<stdio.h>

int main()
{
    //Taking the input from the user
    int num;
    printf("Enter the number here :");
    scanf("%d", &num);

    if(num%2==0)
    {
        printf("The given no is an even no");
    }
    else
    {
        printf("The given no is an odd no");
    }

    return 0;
}
```

6. Write a C program to check whether a given character is a vowel or consonant.

```C

```

7. Write a C program to print the reverse of a given string.

```C

```

8. Write a C program to find the length of a given string.

```C

```

9. Write a C program to concatenate two given strings.

```C

```

10. Write a C program to find the sum of an array of integers.

```C
#include<stdio.h>

int main()
{
    //Taking the integer to determine the size of array from the user
    int n;
    printf("Enter the length of integer array :");
    scanf("%d", &n);

    //Declaring array and making a loop to input integers in the array
    int arry[n];
    for( int i=0 ; i<n ; i++)
    {
        printf("Enter element %d :", i+1);
        scanf("%d", &arry[i]);
    }

    //Initialsing the integer that holds the sum of the array elements and a loop so that sum of the array elements can be calculated
    int sum_arr = 0;
    for(int i=0 ; i<n ; i++)
    {
        sum_arr += arry[i];
    }

    printf("The sum of the array entered is %d\n", sum_arr);

    return 0;
}
```

11. Write a C program to find the largest element in an array of integers.

```C
#include<stdio.h>

int main()
{
    //Taking the integer to determine the size of array from the user
    int n;
    printf("Enter the length of integer array :");
    scanf("%d", &n);

    //Declaring array and making a loop to input integers in the array
    int arry[n];
    for( int i=0 ; i<n ; i++)
    {
        printf("Enter element %d :", i+1);
        scanf("%d", &arry[i]);
    }

    //Initialising the integer variable that holds the value of largest element in the array and a loop to place the biggest value in the variable
    int lar_arr = arry[0];
    for(int i=0 ; i<n ; i++)
    {
        if(arry[i]>lar_arr)
        {
            lar_arr = arry[i];
        }
    }

    printf("The largest element of the array entered is %d\n", lar_arr);

    return 0;
}
```

12. Write a C program to find the smallest element in an array of integers.

```C
#include<stdio.h>

int main()
{
    //Taking the integer to determine the size of array from the user
    int n;
    printf("Enter the length of integer array :");
    scanf("%d", &n);

    //Declaring array and making a loop to input integers in the array
    int arry[n];
    for( int i=0 ; i<n ; i++)
    {
        printf("Enter element %d :", i+1);
        scanf("%d", &arry[i]);
    }

    //Initialising the integer variable that holds the value of largest element in the array and a loop to place the biggest value in the variable
    int smol_arr = arry[0];
    for(int i=0 ; i<n ; i++)
    {
        if(arry[i]<smol_arr)
        {
            smol_arr = arry[i];
        }
    }

    printf("The smallest element of the array entered is %d\n", smol_arr);

    return 0;
}
```

13. Write a C program to sort an array of integers in ascending order.

```C

```

14. Write a C program to sort an array of integers in descending order.

```C

```

15. Write a C program to count the number of occurrences of a given element in an array of integers.

```C

```

16. Write a C program to find the sum of the digits of a given number.

```C

```

17. Write a C program to reverse a given number.

```C

```

18. Write a C program to check whether a given number is a palindrome or not.

```C
#include<stdio.h>
#include<math.h>

int main()
{
    //Taking numer as an input from the user 
    int n1;
    printf("Enter the number to be checked here :");
    scanf("%d", &n1);

    //Input is taken now we need to create a reverse number of this number that is inputted by the user
    int inpcpy, x, revno;
    inpcpy = n1;

    for(int i = 0 ; i<= ; i++)
    {
        x = inpcpy%10;
        inpcpy = inpcpy-x;
        inpcpy = inpcpy/10;

        revno = revno + pow(x, i);
    }

    if(n1 == revno)
    {
        printf("The given number is a palindrome");
    }
    else
    {
        printf("The given no is not a palindrome");
    }
}
```

19. Write a C program to find the factorial of a given number using recursion.

```C
#include<stdio.h>

long int multiplyNumbers(int n);

int main()
{
    //Taking the value from the user and then passing it to the function
    int n1;
    printf("Enter the number here :");
    scanf("%d", &n1);

    long int y;
    y = multiplyNumbers(n1);
    printf("%ld\n", y);

    return 0;
}


long int multiplyNumbers(int n)
{
    if (n>=1)
        return n*multiplyNumbers(n-1);
    else
        return 1;
}
```

20. Write a C program to find the sum of the natural numbers up to a given limit.

```C
#include<stdio.h>
#include<math.h>

int main()
{
    //Taking limit from the user in integer form usin an initialised variable
    int n1;
    printf("Enter the limit of the series here :");
    scanf("%d", &n1);

    //Using the limit to make a loop and store the sum of the series in an integer variable
    int sum_ser = 0;
    for(int i=1 ; i<=n1 ; i++)
    {
        sum_ser += i;
    }
    printf("The sum of the series totals up to : %d\n", sum_ser);

    return 0;
}
```

21. Write a C program to find the GCD of two given numbers.

```C
#include<stdio.h>

int main()
{
    //Taking input from the user in two different integer numbers and also a gcd integer which will store the value of gcd
    int n1, n2, gcd;
    printf("Enter the first number here :");
    scanf("%d", &n1);
    printf("Enter the second number here :");
    scanf("%d", &n2);

    //Creating conditions that check the numbers with respect to each other and calculate the GCD of the given numbrs
    if( n1==n2 )
    {
        printf("The GCD of the given numbers is : %d", n1);
    }
    else
    {
        //Making a loop to run from 1 to ni or n2 whichever is larger and then finding the greatest common diviser
        for(int i=0 ; i<=n1 && i<=n2 ; i++)
        {
            if(n1%i==0 && n2%i==0)
            {
                gcd = i;
            }
        }
    }
    //Now that gcd is found out we will print it on the terminal
    printf("The value of GCD for the given numbers is : %d\n", gcd);
    return 0;
}
```

22. Write a C program to find the LCM of two given numbers.

```C
#include<stdio.h>
#include<math.h>

int main()
{
    //Initialising two varibales and then taking the no in them from user
    int n1, n2;
    printf("Enter first number here :");
    scanf("%d", &n1);
    printf("Enter second number here :");
    scanf("%d", &n2);

    //Using conditions to check and find the LCM of the numbers enetered by the user
    if(n1==n2)
    {
        printf("The lcm of the given numbers is : %d\n", n1);
    }
    else if(n1>n2)
    {
        if((n1%n2)==0)
        {
            printf("The LCM of given numbers is : %d\n", n1);
        }
        else
        {
            int mul_num;
            mul_num = n1 * n2;
            printf("The LCM of given numbers is : %d\n", mul_num);
        }
    }
    else if(n2>n1)
    {
        if((n2%n1)==0)
        {
            printf("The LCM of given numbers is : %d\n", n2);
        }
        else
        {
            int mul_num;
            mul_num = n1 * n2;
            printf("The LCM of given numbers is : %d\n", mul_num);
        }
    }

    return 0;
}
```

23. Write a C program to convert a decimal number to binary.

```C

```

24. Write a C program to convert a binary number to decimal.

```C

```

25. Write a C program to convert a decimal number to octal.

```C

```

26. Write a C program to convert an octal number to decimal.

```C

```

27. Write a C program to convert a decimal number to hexadecimal.

```C

```

28. Write a C program to convert a hexadecimal number to decimal.

```C

```

29. Write a C program to find the sum of the series 1^2+2^2+3^2+...+n^2.

```C
#include<stdio.h>
#include<math.h>

int main()
{
    //Creating an integer n and taking input from the user
    int n;
    printf("Enter the value of n :");
    scanf("%d", &n);

    //Creating a variable to store the sum of the series and loop to calulate the sum of series
    int ser_sum = 0;
    for(int i=0 ; i<=n ; i++)
    {
        ser_sum = ser_sum + pow(i,2);
    }
    printf("The sum of the series totals up to : %d\n", ser_sum);

    return 0;
}
```

30. Write a C program to find the sum of the series 1+2+3+...+n.

```C
#include<stdio.h>
#include<math.h>

int main()
{
    // Creating an integer n and taking input from the user
    int n;
    printf("Enter the value of n :");
    scanf("%d", &n);

    //Creating a variable to store the value of sum of the series and a loop to calculate the sum of series
    int sum_ser = 0;
    for(int i=0 ; i<=n ; i++)
    {
        sum_ser = sum_ser + i;
    }
    printf("The sum of the series totals up to : %d\n", sum_ser);

    return 0;
}
```
