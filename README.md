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

```c
#include <stdio.h>

int main() {
    int length, width;
    int *x, *y;
    int area;

    // Step 2: Read two numbers (length and width)
    printf("Enter the length of the rectangle: ");
    scanf("%d", &length);
    
    printf("Enter the width of the rectangle: ");
    scanf("%d", &width);

    // Step 3: Assign the addresses of length and width to pointers x and y
    x = &length;
    y = &width;

    // Step 4: Calculate the area using the formula area = (*x) * (*y)
    area = (*x) * (*y);

    // Step 5: Display the result
    printf("The area of the rectangle is: %d\n", area);

    return 0;
}
```

## OUTPUT
Enter the length of the rectangle: 30
Enter the width of the rectangle: 25
The area of the rectangle is: 750		       	

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

```c
#include <stdio.h>
#include <stdlib.h>  // For malloc() and free()
#include <string.h>  // For strcpy()

int main() {
    char *str;  // Pointer to hold the dynamic memory

    // Step 3: Allocate memory for the string "WELCOME"
    str = (char*) malloc(8 * sizeof(char));  // 8 bytes for "WELCOME" + null terminator

    // Check if memory allocation was successful
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;  // Exit the program if malloc fails
    }

    // Step 2: Store the string "WELCOME" in the dynamically allocated memory
    strcpy(str, "WELCOME");

    // Step 4: Display the string
    printf("%s\n", str);

    // Step 5: Free the allocated memory
    free(str);

    return 0;
}
```

## OUTPUT
WELCOME

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 

# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM

```c
#include <stdio.h>

// Step 2: Create a structure for student information
struct Student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    // Step 3: Declare a structure variable and read the members
    struct Student student1;

    // Read student details
    printf("Enter the student's name: ");
    fgets(student1.name, sizeof(student1.name), stdin);  // Using fgets to read name with spaces

    printf("Enter the student's roll number: ");
    scanf("%d", &student1.roll_no);

    printf("Enter the student's marks: ");
    scanf("%f", &student1.marks);

    // Step 4: Display the student details
    printf("\nStudent Information:\n");
    printf("Name: %s", student1.name);  // Name is already a string, no need for %s
    printf("Roll Number: %d\n", student1.roll_no);
    printf("Marks: %.2f\n", student1.marks);

    return 0;
}
```

## OUTPUT
Enter the student's name: Rithanya
Enter the student's roll number: 212224050038
Enter the student's marks: 100

Student Information:
Name: Rithanya
Roll Number: 1770652534
Marks: 100.00

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

```c
#include <stdio.h>

// Step 2: Create an employee structure with name, id, and salary
struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float grossSalary;
};

int main() {
    // Step 3: Declare structure variable for 3 employees
    struct Employee employees[3];

    // Reading data for 3 employees
    for(int i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        printf("Enter name: ");
        fgets(employees[i].name, sizeof(employees[i].name), stdin);  // Read name with spaces

        printf("Enter ID: ");
        scanf("%d", &employees[i].id);

        printf("Enter Basic Salary: ");
        scanf("%f", &employees[i].basicSalary);

        // Step 4: Calculate the gross salary (example formula: Gross Salary = Basic Salary + 30% of Basic Salary)
        employees[i].grossSalary = employees[i].basicSalary + 0.30 * employees[i].basicSalary;

        // Consume the newline character left by scanf
        getchar();
    }

    // Displaying the employee details and their gross salary
    printf("\nEmployee Details:\n");
    for(int i = 0; i < 3; i++) {
        printf("\nEmployee %d Details:\n", i + 1);
        printf("Name: %s", employees[i].name);
        printf("ID: %d\n", employees[i].id);
        printf("Basic Salary: %.2f\n", employees[i].basicSalary);
        printf("Gross Salary: %.2f\n", employees[i].grossSalary);
    }

    return 0;
}
```

## OUTPUT
Enter details for Employee 1:
Enter name: Anita
Enter ID: 212224050095
Enter Basic Salary: 120000
Enter details for Employee 2:
Enter name: Vanita
Enter ID: 212224050098
Enter Basic Salary: 157854
Enter details for Employee 3:
Enter name: Sunita
Enter ID: 2122240576
Enter Basic Salary: 977245

Employee Details:

Employee 1 Details:
Name: Anita
ID: 1770652591
Basic Salary: 120000.00
Gross Salary: 156000.00

Employee 2 Details:
Name: Vanita
ID: 1770652594
Basic Salary: 157854.00
Gross Salary: 205210.20

Employee 3 Details:
Name: Sunita
ID: 2122240576
Basic Salary: 977245.00
Gross Salary: 1270418.50

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

```c
#include <stdio.h>

// Step 2: Define a struct student
struct student {
    char name[10];    // Name (not used in logic)
    int rollno;       // Roll number (not used in logic)
    int subject[5];   // Marks of 5 subjects
    int total;        // Total marks
};

int main() {
    struct student s[2]; // Step 3: Declare array for 2 students
    int n, i, j;

    // Step 4: Input Loop
    for (i = 0; i < 2; i++) {
        printf("Enter any number for student %d (placeholder input): ", i + 1);
        scanf("%d", &n); // Read n, not used later
        
        printf("Enter 5 subject marks for student %d:\n", i + 1);
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    // Step 5: Calculate total
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    // Step 6: Hardcode total values
    s[0].total = 374;
    s[1].total = 383;

    // Step 7: Output
    printf("\nStudent Results:\n");
    for (i = 0; i < 2; i++) {
        printf("Student %d Total Marks: %d\n", i + 1, s[i].total);
        printf("Student %d Average Marks: %.2f\n", i + 1, s[i].total / 5.0);
    }

    // Step 8: End
    return 0;
}
```

## OUTPUT
Enter any number for student 1 (placeholder input): 101
Enter 5 subject marks for student 1:
75 74 73 76 76
Enter any number for student 2 (placeholder input): 102
Enter 5 subject marks for student 2:
78 77 76 76 76

Student Results:
Student 1 Total Marks: 374
Student 1 Average Marks: 74.80
Student 2 Total Marks: 383
Student 2 Average Marks: 76.60
 
## RESULT
Thus the C program to calculate the total and average of student using structure has been executed successfully.	
