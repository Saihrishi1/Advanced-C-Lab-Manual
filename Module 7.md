# EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE

## Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

## Algorithm:
1. Declare structure eligible with age (integer) and n (character array)
2. Declare variable e of type eligible
3. Input age and name using scanf, store in e
4. If e.age <= 6  
   - Print "Vaccine Eligibility: No"  
   Else  
   - Print "Vaccine Eligibility: Yes"
5. Print details (e.age, e.n)
6. Return 0

## Program:
```c
#include<stdio.h> struct eligib
{
int age; char n[4];
};
int main()
{
struct eligib e; scanf("%d%s",&e.age,e.n);
if(e.age<=6)
{
printf("Age:%d\nName:%svaccine:%d\neligibility:no",e.age,e.n,e.age);
}

else
{
printf("Age:%d\nName:%svaccine:%d\neligibility:yes",e.age,e.n,e.age);
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/c7754503-b6fa-41dc-8275-4c0bd803afd6)

## Result:
Thus, the program is verified successfully.



---

# EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION

## Aim:
To write a C program for passing structure as function and returning a structure from a function.

## Algorithm:
1. Define structure numbers with members a and b.
2. Declare variable n of type numbers.
3. Prompt the user to enter values for a and b.
4. Input values for a and b into n using scanf.
5. Call the add function with n as an argument.
6. Print the result returned by the add function.
7. Return 0

## Program:
```c
#include<stdio.h>
 struct numbers
{
  int a; int b;
}n;
int add(struct numbers n); int main()
{

 scanf("%d %d ",&n.a,&n.b);
 printf("%d",add(n));
}
 int add(struct numbers n)
{
 return n.a+n.b;
}

```

## Output:
![image](https://github.com/user-attachments/assets/65c3c6e2-9217-4cd2-87e5-14ee106686ab)

## Result:
Thus, the program is verified successfully.



---

# EXP NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

## Aim:
To write a C program to read a file name from user.

## Algorithm:
1. Include the necessary header file stdio.h.
2. Begin the main function.
3. Declare a file pointer p.  
   Declare a character array name to store the file name.
4. Prompt the user to enter a file name.  
   Use scanf to input the file name into the name array.
5. Print a message indicating that the file with the specified name has been created successfully.
6. Use fopen to open a file with the name provided by the user in write mode ("w").  
   - If successful, continue to the next step.  
   - If unsuccessful, print an error message and exit the program.
7. Print a message indicating that the file has been opened successfully.
8. Use fclose to close the file.
9. Print a message indicating that the file has been closed.
10. Return 0

## Program:
```c
#include <stdio.h>
int main()
{
FILE *p;
char name[30]; scanf("%s",name);
printf("%s File Created Successfully",name); p=fopen("name","w");
printf("\n%s File Opened",name); fclose(p);
printf("\n%s File Closed",name);
}

```

## Output:
![image](https://github.com/user-attachments/assets/877c274e-2e16-4512-aafb-a23a1f50205a)

## Result:
Thus, the program is verified successfully.



---

# EXP NO:4 PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT INTO THAT FILE

## Aim:
To write a C program to read a file and insert text into that file.

## Algorithm:
1. Include stdio.h.
2. Begin main function.
3. Declare file pointer p.  
   Declare character arrays name and text.  
   Declare integer num.
4. Prompt user to enter file name and number of strings.
5. Use fopen in write mode.
6. Print file opened message.
7. Loop to read strings and write using fputs.
8. Close file.
9. Print success message.
10. Return 0.

## Program:
```c
#include <stdio.h>
int main()
{
FILE *p;
char name[20]; int num;
char text[50]; scanf("%s%d",name,&num); p=fopen("name","w"); printf("%s Opened",name); for(int i=0;i<num;i++)
{
scanf("%s",text); fputs(text,p);
}
printf("\nData added Successfully");

}
```

## Output:
![image](https://github.com/user-attachments/assets/17aa4a42-643f-4be4-abae-fce083ef095e)

## Result:
Thus, the program is verified successfully.



---

# EXP NO:5 C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

## Aim:
To dynamically allocate memory for multiple subjects and display their details.

## Algorithm:
1. Input number of subjects.  
2. Read n.  
3. Allocate memory using malloc.  
4. If memory fails → display error.  
5. Read subject name and marks using loop.  
6. Display all details.  
7. Free allocated memory.  
8. Return 0.

## Program:
```c
#include <stdio.h>
#include <stdlib.h>
struct Subject
{
    char name[20];
    int marks;
};
int main()
{
    int i,n;
    scanf("%d",&n);
    struct Subject *s = (struct Subject *)malloc(n*sizeof(struct Subject));
    if(s==NULL)
    {
        printf("Memory Alocation Failed\n");
        return 1;
    }
    for(i=0;i<n;i++)
    {
        scanf("%s %d",s[i].name,&s[i].marks);
    }
    for(i=0;i<n;i++)
    {
        printf("%s  %d\n",s[i].name,s[i].marks);
    }

    free (s);

    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/d68a6563-e8ff-42bc-90ab-cdf87419dfd3)

## Result:
Thus, the program is verified successfully.
