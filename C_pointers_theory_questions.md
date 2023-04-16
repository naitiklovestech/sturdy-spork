# 100 C Programming Questions Based on Pointers

<details>
  <Summary>1. What is a pointer?</summary>
  
  - A pointer is a variable that stores the memory address of another variable as its value. A pointer variable points to a data type (like int ) of the same type, and is created with the * operator.

</details>

<details>
  <summary>2. How do you declare a pointer?</summary>
  
  - The pointer in c language can be declared using * (asterisk symbol). It is also known as indirection pointer used to dereference a pointer.
</details>

<details>
  <summary>3. How do you initialize a pointer?</summary>
  
  - You need to initialize a pointer by assigning it a valid address. This is normally done via the address-of operator ( & ). The address-of operator ( & ) operates on a variable, and returns the address of the variable. For example, if number is an int variable, &number returns the address of the variable number .
</details>

<details>
  <summary>4. What is the purpose of the `*` operator in C?</summary>
  
  -
</details>

<details>
  <summary>5. What is the difference between a pointer and a variable?</summary>
  
  - A pointer variable (or pointer in short) is basically the same as the other variables, which can store a piece of data. Unlike normal variable which stores a value (such as an int, a double, a char), a pointer stores a memory address. Pointers must be declared before they can be used, just like a normal variable.
</details>

<details>
  <summary>6. How do you assign a value to a pointer?</summary>
  
  - To assign an address of a variable into a pointer, you need to use the address-of operator & (e.g., pNumber = &number ). On the other hand, referencing and dereferencing are done on the references implicitly.
</details>

<details>
  <summary>7. What is the difference between `NULL` and `void` pointers?</summary>
  
  - The null pointer is basically used in a program to assign the value 0 to a pointer variable of any data type. The void pointer, on the other hand, has no value assigned to it and we use it to store the addresses of other variables in the program- irrespective of their data types.
</details>

<details>
  <summary>8. How do you dereference a pointer?</summary>
  
  - The unary operator * is used to declare a pointer and the unary operator & is used to dereference the pointer.. In both cases, the operator is “unary” because it acts upon a single operand to produce a new value
</details>

<details>
  <summary>9. What is pointer arithmetic?</summary>
  
  - Pointer arithmetic provides the programmer with a single way of dealing with different types: adding and subtracting the number of elements required instead of the actual offset in bytes.
</details>

<details>
  <summary>10. How do you compare two pointers?</summary>
  
  - We can compare pointers if they are pointing to the same array. Relational pointers can be used to compare two pointers. Pointers can’t be multiplied or divided.

  ```C
  #include <stdio.h>
  int main()
  {
    int *p2;
    int *p1;
    p2 = (int *)300;
    p1 = (int *)200;
    if(p1 > p2) 
    {
      printf("P1 is greater than p2");
    }
    else 
    {
      printf("P2 is greater than p1");
    }
   return(0);
  }
  ```
</details>

<details>
  <summary>11. How do you pass a pointer to a function?</summary>
  
  - C programming allows passing a pointer to a function. To do so, simply declare the function parameter as a pointer type.

Following is a simple example where we pass an unsigned long pointer to a function and change the value inside the function which reflects back in the calling function −

```C
#include <stdio.h>
#include <time.h>
 
void getSeconds(unsigned long *par);

int main () 
{

   unsigned long sec;
   getSeconds( &sec );

   /* print the actual value */
   printf("Number of seconds: %ld\n", sec );

   return 0;
}

void getSeconds(unsigned long *par)
{
   /* get the current number of seconds */
   *par = time( NULL );
   return;
}
```
</details>

<details>
  <summary>12. How do you return a pointer from a function?</summary>
  
  - Pointers in C programming language is a variable which is used to store the memory address of another variable. We can pass pointers to the function as well as return pointer from a function. But it is not recommended to return the address of a local variable outside the function as it goes out of scope after function returns

  ```C
  // C program to illustrate the concept of
  // returning pointer from a function
  #include <stdio.h>

  // Function that returns pointer
  int* fun()
  {
	// Declare a static integer
	static int A = 10;
	return (&A);
  }

  // Driver Code
  int main()
  {
	// Declare a pointer
	int* p;

	// Function call
	p = fun();

	// Print Address
	printf("%p\n", p);

	// Print value at the above address
	printf("%d\n", *p);
	return 0;
  }
```
</details>

<details>
  <summary>13. What is a function pointer?</summary>
  
  -
</details>

<details>
  <summary>14. How do you declare a function pointer?</summary>
  
  -
</details>

<details>
  <summary>15. How do you call a function using a function pointer?</summary>
  
  -
</details>

<details>
  <summary>16. How do you use a pointer to a structure?</summary>
  
  -
</details>

<details>
  <summary>17. How do you allocate memory dynamically using `malloc()`?</summary>
  
  -
</details>

<details>
  <summary>18. How do you free memory allocated using `malloc()`?</summary>
  
  -
</details>

<details>
  <summary>19. How do you use the `sizeof` operator with pointers?</summary>
  
  -
</details>

<details>
  <summary>20. How do you use pointers to create dynamic arrays?</summary>
  
  -
</details>

<details>
  <summary>21. What is a pointer and why is it useful in C?</summary>
  
  -
</details>

<details>
  <summary>22. How do you declare a pointer in C?</summary>
  
  -
</details>

<details>
  <summary>23. How do you initialize a pointer to a variable?</summary>
  
  -
</details>

<details>
  <summary>24. What is the & operator in C and how is it used with pointers?</summary>
  
  -
</details>

<details>
  <summary>25. How do you dereference a pointer in C?</summary>
  
  -
</details>

<details>
  <summary>26. What is the difference between *p and p in C?</summary>
  
  -
</details>

<details>
  <summary>27. How do you assign a value to a pointer in C?</summary>
  
  -
</details>

<details>
  <summary>28. What is pointer arithmetic in C?</summary>
  
  -
</details>

<details>
  <summary>29. How do you use malloc() to dynamically allocate memory in C?</summary>
  
  -
</details>

<details>
  <summary>30. How do you use free() to deallocate memory in C?</summary>
  
  -
</details>

<details>
  <summary>31. What is a void pointer in C?</summary>
  
  -
</details>

<details>
  <summary>32. How do you cast a pointer from one type to another in C?</summary>
  
  -
</details>

<details>
  <summary>33. What is a double pointer in C and how is it used?</summary>
  
  -
</details>

<details>
  <summary>34. How do you pass a pointer to a function in C?</summary>
  
  -
</details>

<details>
  <summary>35. How do you return a pointer from a function in C?</summary>
  
  -
</details>

<details>
  <summary>36. How do you use pointers to create arrays in C?</summary>
  
  -
</details>

<details>
  <summary>37. What is the difference between an array and a pointer in C?</summary>
  
  -
</details>

<details>
  <summary>38. How do you use pointers to create structures in C?</summary>
  
  -
</details>

<details>
  <summary>39. How do you create a linked list using pointers in C?</summary>
  
  -
</details>

<details>
  <summary>40. How do you traverse a linked list in C using pointers?</summary>
  
  -
</details>

<details>
  <summary>41. How do you insert a node into a linked list in C using pointers?</summary>
  
  -
</details>

<details>
  <summary>42. How do you delete a node from a linked list in C using pointers?</summary>
  
  -
</details>

<details>
  <summary>43. How do you implement a stack using pointers in C?</summary>
  
  -
</details>

<details>
  <summary>44. How do you implement a queue using pointers in C?</summary>
  
  -
</details>

<details>
  <summary>45. How do you use pointers to pass arguments to a function in C?</summary>
  
  -
</details>

<details>
  <summary>46. How do you use pointers to return multiple values from a function in C?</summary>
  
  -
</details>

<details>
  <summary>47. How do you use pointers to access elements of a multi-dimensional array in C?</summary>
  
  -
</details>

<details>
  <summary>48. How do you use pointers to implement dynamic memory allocation for multi-dimensional arrays in C?</summary>
  
  -
</details>

<details>
  <summary>49. How do you use pointers to implement recursion in C?</summary>
  
  -
</details>

<details>
  <summary>50. How do you use pointers to create and manipulate strings in C?</summary>
  
  -
</details>
