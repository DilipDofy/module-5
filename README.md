# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    float length, width;
    float *ptr_length, *ptr_width, area;

    ptr_length = &length;
    ptr_width = &width;

    printf("Enter length of the rectangle: ");
    scanf("%f", ptr_length);

    printf("Enter width of the rectangle: ");
    scanf("%f", ptr_width);

    area = (*ptr_length) * (*ptr_width);

    printf("The area of the rectangle is: %.2f\n", area);

    return 0;
}
```
## OUTPUT
![Screenshot 2025-05-31 095842](https://github.com/user-attachments/assets/221f1efe-43e3-40cf-814d-ddb92f832226)

		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
char *str = (char *)malloc(8 * size(char));
if (str == NULL)
{
printf("Memory allocation failed!\n);
return 1;
}
str[0] = 'w'
str[1] = 'E';
str[2] ='L'
str[3] ='C'
str[4[ ='O'
str [5] ='M'
str[6] ='E'
str[7] ='\0';
printf("%s\n",str);
free(str);
return 0;
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/93c35ce1-647a-44af-9e35-6dbf97ed657d)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include<stdio.h>
struct student {
 chsr name[50];
int rollNumber;
float marks;
}
int main() {
 struct student student;
scanf("%s", student.name);
scanf("%d", &student.rollNumber);
scanf("%f", &student.marks);
printf("Displaying Information:\n);
printf("Name" %s\n", student.name);
printf("Roll number: %d\n",student.rollBumber);
printf("Marks: %.1f\n",student.marks);
return 0;
}

```

## OUTPUT

![image](https://github.com/user-attachments/assets/d2016d8e-d522-497d-831c-93fd65c6dd1c)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
struct employee
{
int eno;
char dept[20];
float basicpay;
float da;
float hra;
float grossSalary;
};
int main()
{
struct employee emp[3]
for (int i=0;i<3;i++)
{
scanf("%d %s %f", &emp[i].eno,emp[i].dept,&emp[i].basipay);
emp[i].da=emp[i].basicpay*0.10;
emp[i].hra=emp[i].basicpay*0.30;
emp[i].grossSalary=emp[i].basicpay+emp[i].hra;
}
printf("Details of the Employee:\n);
for(int i=0;,i<3;i++)
{
printf("%d %s %.0f %.0f %.2f\n", emp[i].eno,emp[i].dept,emp[i].basicpay,em
}
}
```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/390c4694-117a-403a-99bc-1746b18b4de5)


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
 #include <stdio.h>
 struct Student {
    char name[50];
    int marks[5];
    float total;
    float average;
 };
 int main() {
    struct Student student;
    int sum = 0;
    printf("Enter student's name: ");
    scanf("%s", student.name);
    printf("Enter marks for 5 subjects:\n");
    for (int i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%d", &student.marks[i]);
        sum += student.marks[i];
    }
    student.total = sum;
    student.average = sum / 5.0;
    printf("\nStudent Name: %s\n", student.name);
    printf("Total Marks: %.2f\n", student.total);
    printf("Average Marks: %.2f\n", student.average);
    return 0;
 }
```
## OUTPUT
![Screenshot 2025-05-31 100646](https://github.com/user-attachments/assets/2f3df3b6-d58a-4713-9957-874a9b825be8)


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


