Lab 7a
======

Submit your finished code to the Dropbox. You will need to pass off the lab with the TA or tutor during their office hours (their information is in the CS 105 Course Information section of the Class Resources module), or the instructor in class. Follow the CS 105 
Formatting Guide which is also found in the CS 105 Course Information section.

Read the instructions carefully. Make sure your output matches the example run.

Objectives:
===========

In this lab, you will learn how to do the following:

-   Write a method
-   Pass arguments to the method
-   Write another method
-   Call the second method from the first
-   Use the jave.time.LocalDate module

Structure:
==========

Create the following structure in Eclipse for this lab.

**Package Name:** week7\
**Class Name:** Lab7a

Program: checkEligibility() Method
==================================

Write a program that asks the user to enter a name and a year, which represents the name of a potential student and the year they were born.

Perform input validation to ensure the user entered a valid whole number for the year.

Have your main() method call a method that you write called checkEligibility(), passing the name and year as arguments. Your checkEligibility() method will call another method you write called calculateAge(), passing the year as an argument, to get the age of the 
person. The checkEligibility() method will then use the age to determine which type of school, if any, the student is eligible to attend and display the result as shown in the example. Use the table found in the technical design below to determine the output.

The calculateAge() method will use a LocalDate object to calculate the age of the person based on the year that was passed in from the calling method. Return the age to the calling method.

Technical Design:
=================

#### **Module Imports**

You will need the following import statements for this program:

import java.time.LocalDate; // Import the LocalDate class\
import java.util.Scanner; // Needed for user input

#### **Needed Methods**

The **main()** method will:

-   Ask the user for a potential student's name and the year they were born.
-   Call the checkEligibility() method passing the name and year as arguments
-   Repeat the program until the user wants to quit

The **checkEligibility()** method will:

-   Accept a string and an integer
-   Call the calculateAge() method passing the year as an argument
-   Use the age returned from calculateAge() to determine which type of school, if any, for which the student is eligible
-   Display the result as shown in the example

The **calculateAge()** method will:

-   Accept an integer (year) as an argument
-   Declare a variable to get and store the current date and time
-   Extract the year from the variable and return the difference between the current year and the student's birth year

#### **Eligibility table**

| **Age** | **Eligibility**               |
| 0-4     | Not eligible to attend school |
| 5-11    | Elementary School             |
| 12-14   | Jr. High School               |
| 15-17   | High School                   |
| 18 +    | College                       |

#### **Getting the date with LocalDate**

The LocalDate module can get you the current date and time.  To get the current year, do the following:

-   Create a new variable of type LocalDate and set it to the result of LocalDate.now()
    -   CODE:  ***LocalDate rightnow = LocalDate.now()***
-   Call the getYear() method to get the current year
    -   CODE: ***int thisYear = rightNow.getYear()***

Key program requirements:
=========================

-   Do input validation on the year using try/catch.
-   Use the LocalDate module to get the current year.
-   Create two methods, checkEligibility() and calculateAge().
-   The names of the two variables inside main() which are passed to checkEligibility() as arguments MUST be the SAME AS the names of the parameters inside of your checkEligibility() method.
-   The name of the variable inside checkEligibility() which is passed to calculateAge() as an argument MUST be the SAME AS the name of the parameter inside of your calculateAge() method.
-   You must complete the Ponder activity below.
-   Submit the following .java file:
    -   Lab7a.java

Ponder:
=======

Discuss the following with your partner. **Failure to do this activity and discuss these questions before you attempt to pass off your program will result in a failed pass off**.

**1)** One of the key program requirements for this lab indicates that you must use the same names for variables inside of each method.  Discuss why your instructor would make this requirement.  Is this a requirement of Java?

**2)** Do the following:

-   On a separate piece of paper,** draw boxes that represent the various memory locations that will be used by your program.**
-   With your partner, use your finger or a pen to point at each line of code as you trace through the program from beginning to end. **Yes, really use your finger or a pen.**
-   Step through each line IN THE ORDER THAT IT WILL BE EXECUTED from beginning to end.
-   Discuss what each line of code does.
-   Make assumptions of what numbers the user will enter, then **write those numbers in the appropriate memory locations as you trace through the code with your finger.**
-   Show the paper with your memory locations to the TA or instructors when you pass off the program.

Example Run:
============

*This program will ask the user to enter a name and a birth year for a potential student.*\
*The program will then determine what type of school, if any, the potential student is eligible to attend.*\
*Please enter the name of a potential student: Emily*\
*Please enter the year the potential student was born: last year*

*Invalid response. Please enter a whole number for the birth year.*\
*Please enter the year the potential student was born: 2018*\
*Emily is 1 years old. Emily is too young to attend school.*

*Would you like to play again? (Y/N): y*\
*Please enter the name of a potential student: Fred*\
*Please enter the year the potential student was born: 2000*\
*Fred is 19 years old. Fred may attend college.*

*Would you like to play again? (Y/N): n*
