# 30 Programming Questions in C: Strings

1. Write a C program to count the number of characters in a string.

2. Write a C program to find the length of a string.

3. Write a C program to concatenate two strings.

4. Write a C program to compare two strings.

5. Write a C program to reverse a string.

6. Write a C program to convert all characters in a string to uppercase.

7. Write a C program to convert all characters in a string to lowercase.

8. Write a C program to find the first occurrence of a substring in a string.

```C
#include<stdio.h>
#include<string.h>

int main()
{
    char str1[100], str2[50];
    int i, index=0, found = 0;
    printf("\nEnter the string :");
    gets(str1);
    printf("\nEnter substring to be found :");
    gets(str2);

    while(str1[index]!='\0')
    {
        if(str1[index] == str2[0])
        {
            i = 0;
            found = 1;
            while(str2[i]!='\0')
            {
                if(str1[index+i]!= str2[i])
                {
                    found = 0;
                    break;
                }
                i++;
            
            }
        }

        if(found == 1)
        {
            break;
        }

        index++;
    }

    if(found == 1)
    {
        printf("\n'%s' is found at index %d\n", str2, index);
    }
    else
    {
        printf("\n'%s' is not found\n", str2);
    }

    return 0;

}
```

9. Write a C program to find the last occurrence of a substring in a string.

```C
#include<stdio.h>
#include<string.h>

int main()
{
    char s[1000],c;  
    int i,n,k=0;
 
    printf("Enter  the string : ");
    gets(s);
    printf("Enter character to be searched: ");
    c=getchar();
    
    for(i=strlen(s)-1;i>=0;i--)  
    {
    	if(s[i]==c)
    	{
		  k=1;
    	  break;
		}
 	}
    if(k)
 	    printf("character  %c  is last occurrence at location:%d ",c,i);
    else
        printf("character is not in the string ");

 	 
     
    return 0;
}
```

10. Write a C program to remove all occurrences of a character from a string.

```C
#include<stdio.h>
#include <string.h>
 
int main()
{
    char s[1000],c;  
    int  i,k=0;
 
    printf("Enter  the string : ");
    gets(s);
    
	printf("Enter character: ");
    c=getchar();
 
     
    for(i=0;s[i];i++)
    {
     	s[i]=s[i+k];
 
     	
     	if(s[i]==c)
     	{
		  k++;
		  i--;
	    }
     	
      	 
     	
	}
 
 	 printf("%s\n",s);
 	 
     
    return 0;
}
```

11. Write a C program to replace all occurrences of a character with another character in a string.

```C
#include <stdio.h> 
#include <string.h>
 
int main()
{
    char s[1000],c1,c2;  
    int  i;
 
    printf("Enter  the string : ");
    gets(s);
    
	printf("Enter a character replace: ");
    c1=getchar();
    getchar();
    printf("\nEnter character to replace  with  %c : ",c1);
    c2=getchar();
    printf("\n before replace:%s",s);
    
    for(i=0;s[i];i++)
	{  
		if(s[i]==c1)
		{
		   s[i]=c2;
	 
	    }

	}
	   
    printf("\nafter replace:%s",s);
 	 
     
    return 0;
}
```

12. Write a C program to find the frequency of a character in a string.

13. Write a C program to remove all spaces from a string.

14. Write a C program to check if a string is a palindrome.

15. Write a C program to sort an array of strings.

16. Write a C program to find the largest and smallest word in a string.

17. Write a C program to find the number of words in a string.

18. Write a C program to remove all vowels from a string.

19. Write a C program to remove all consonants from a string.

20. Write a C program to find the sum of all numbers in a string.

21. Write a C program to count the number of words starting with a particular letter in a string.

22. Write a C program to find the most repeated word in a string.

23. Write a C program to remove a particular word from a string.

24. Write a C program to replace a particular word with another word in a string.

25. Write a C program to extract a substring from a string.

26. Write a C program to find the number of occurrences of a substring in a string.

27. Write a C program to remove all punctuation marks from a string.

28. Write a C program to find the first non-repeating character in a string.

29. Write a C program to convert a string to an integer.

30. Write a C program to convert an integer to a string.

31. Write a C program to concatenate two strings without using library concatenate function.

```C
#include<stdio.h>
#include<string.h>

void concat(char[], char[]);

int main()
{
    char s1[100], s2[50];
    printf("\nEnter string 1 :");
    gets(s1);
    printf("\nEnter string 2 :");
    gets(s2);

    concat(s1,s2);

    printf("\nConcated string is :%s\n", s1);
    return 0;
}

void concat(char s1[], char s2[])
{
    int i, j;
    i = strlen(s1);
    for(j = 0; s2[j]!='\0' ; i++,j++)
    {
        s1[i] = s2[j];
    }
    s1[i] = '\0';
}
```
