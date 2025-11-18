# EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

## Aim:
To write a C program to create a function to find the greatest number

## Algorithm:
1. Include the necessary header `#include <stdio.h>`.
2. Use a series of if and else if statements to compare the values and return the maximum among them.
3. Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4. Use scanf to take four integers as input.
5. Call the max_of_four function with the input integers and store the result in the greater variable.

## Program:
```c
#include<stdio.h>
int max_of_four(int a,int b,int c,int d)
{
    if(a>b && a>c && a>d)
    {
        return a;
    }
    else if(b>a && b>c && b>d)
    {
        return b;
    }
    else if(c>a && c>b && c>d)
    {
        return c;
    }
    else
    {
        return d;
    }
}
int main()
{
    int n1,n2,n3,n4,greater;
    scanf("%d%d%d%d",&n1,&n2,&n3,&n4);
    greater=max_of_four(n1,n2,n3,n4);
    printf("%d",greater);
}
```

## Output:
![image](https://github.com/user-attachments/assets/1e610c20-facc-4621-bc18-f7e78b8020f7)

## Result:
Thus, the program that creates a function to find the greatest number is verified successfully.



---

# EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND XOR COMPARISONS

## Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:
1. Define a function calculate_the_max that takes two integers n and k as parameters.
2. Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations.
3. Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4. Check conditions for AND, OR, and XOR operations and update the maximum values.
5. Declare variables n and k to store user input.
6. Use scanf to take two integers as input.
7. Call the calculate_the_max function with input values.

## Program:
```c
#include<stdio.h>
int main()
{
    int n,k;
    scanf("%d %d",&n,&k);
    int max_and=0;
    int max_or=0;
    int max_xor=0;

    for(int i=1;i<n;i++)
    {
        for(int j=i+1;j<=n;j++)
        {
            int reand=i&j;
            int reor=i|j;
            int rexor=i^j;

            if(reand<k && reand>max_and)
                max_and=reand;

            if(reor<k && reor>max_or)
                max_or=reor;

            if(rexor<k && rexor>max_xor)
                max_xor=rexor;
        }
    }

    printf("%d\n",max_and);
    printf("%d\n",max_or);
    printf("%d",max_xor);
}
```

## Output:
![image](https://github.com/user-attachments/assets/2559981f-3411-468a-9bf3-775e9d04c124)

## Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons is verified successfully.



---

# EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

## Aim:
To write a C program to write the logic for the requests

## Algorithm:
1. Declare variables noshel and noque for the number of shelves and queries.
2. Read number of shelves and queries.
3. Allocate shelves and book count arrays.
4. Process queries inside a loop.
5. Update shelves, retrieve values, or print count as required.

## Program:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, q;
    scanf("%d", &n);
    scanf("%d", &q);

    int** shelves = (int**)malloc(n * sizeof(int*));
    int* book_counts = (int*)calloc(n, sizeof(int));

    for (int i = 0; i < n; i++) {
        shelves[i] = NULL;
    }

    for (int i = 0; i < q; i++) {
        int type;
        scanf("%d", &type);

        if (type == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            book_counts[x]++;
            shelves[x] = (int*)realloc(shelves[x], book_counts[x] * sizeof(int));
            shelves[x][book_counts[x] - 1] = y;
        }
        else if (type == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", shelves[x][y]);
        }
        else if (type == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", book_counts[x]);
        }
    }

    for (int i = 0; i < n; i++) {
        free(shelves[i]);
    }
    free(shelves);
    free(book_counts);

    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/ac829334-3b5c-4c0e-8201-2e2b025d6c84)

## Result:
Thus, the program to write the logic for the requests is verified successfully.



---

# EXP NO:24 C PROGRAM TO PRINT THE SUM OF THE INTEGERS IN THE ARRAY

## Aim:
To write a C program to print the sum of the integers in the array.

## Algorithm:
1. Read the number of elements.
2. Declare an array of size n.
3. Read n integers.
4. Add them to the sum.
5. Print the result.

## Program:
```c
#include<stdio.h>
int main ()
{
    int n;
    scanf("%d",&n);
    int arr[n];
    int sum=0;
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
        sum=sum+arr[i];
    }
    printf("%d",sum);
}
```

## Output:
![image](https://github.com/user-attachments/assets/6b757102-7afe-4287-a3db-854d162dadca)

## Result:
Thus, the program prints the sum of the integers in the array is verified successfully.



---

# EXP NO:25 C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

## Aim:
To write a C program that counts the number of words in a given sentence.

## Algorithm:
1. Input the sentence.
2. Initialize a word counter.
3. Iterate through the characters.
4. Count transitions from space to non-space.
5. Print total number of words.

## Program:
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    fgets(str,sizeof(str),stdin);
    int len=sizeof(str);
    int count=1;

    for(int i=0;i<len-1;i++){
        if(str[i]==' ')
            count++;
    }
    printf("Total number of words in the string is :%d",count);
    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/89ca740d-7881-4441-8644-6b30d4fc0295)

## Result:
Thus, the program that counts the number of words in a given sentence is verified successfully.
