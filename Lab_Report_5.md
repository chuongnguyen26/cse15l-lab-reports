# Lab Report 5

- Name: Chuong Nguyen
- Email: chn021@ucsd.edu
---

## Lab on Creating a Grading Script

![Image1](/Report_5_Images/Image1.png)

- Step 1: I created a variable CPATH to hold the string containing the path directory of lib for later runs of JUnit tests.
- Step 2: Always remove student-submission directory if there is one. Once done, I will git clone a new student-submission directory. In doing this, will allow me to run on multiple different student-submission libraries from github. Afterward, I will have the message be printed in the terminal to inform the user that the student-submission repo from github has been successfully cloned to the local device.
- Step 3: Once cloning is finished, change the current directory to student-submission and check if a java file ListExamples exist in the directory.
    - If the file exists in the current directory, the device will print a message stating that it has found the file.
    - Otherwise, return the statement that informs the user that the file has not been found, therefore, the bash script will end.
- Step 4: If the ListExmaples file is found, copy the TestListExamples.java outside of the student-submission directory and create another TestListExamples.java file inside the student-submission directory.
- Step 5: Once done copying, compile all java files with the JUnit test. Then check if the exit value returns 0. If the exit value is indeed 0, proceed to the next step. Otherwise, print an error statement that informs the user regarding an error occured while compiling and exit the script.
- Step 6: If no error occurred during compiling, print all existing files in the student-submission directory. 
- Step 7: Run the JUnit test on the TestListExamples java file and store all return values into the TestResult.txt file.

### At this stage, the machine have finished cloning the repo from github, checking for correct file, compiling and running the test file with the JUnit tests. The machine will then proceed to parsing results from running the JUnit tests and convert those values to percentage grade that will be returned to the user.

- Step 8: Since I know that the number for test ran and failed which are displayed, as ```.E.E..``` an example, will always be on the second line of the result output. In order to access the line to count the number of passes and failures, I will first parse the first two lines of the output inside the TestResult.txt. The parsed lines will then be stored inside a parsedHead.txt file. I then will parse the last line in the parsedHead.txt file and store into a parsedTail.txt file.
- Step 9: Once I have the line containing test results, I will then grep search the pattern ```.``` in the parsedTail.txt file and count how many of those pattern appeared in the line. The reason I am parsing ```.``` is to count how many JUnit test ran, in order the value of total test to a variable TOTAL_TEST for later use.
- Step 10: A continuation from step 9, I will repeat the same process to count for how many of the pattern ```E``` exists in the test result line, as ```E``` represents the amount of the test failed on the current ListExample.java file.
- Step 11: Once I have the values for the total tests and failed tests, I will be using these values to find the difference between the two in order to calculate the number of passed tests.
- Step 12: Afterward, I converted the ratio of passed tests and total tests to a grading percentage.
- Step 13: The final step is to print out the grade in the terminal for the user to see.
---

### Examples of the grading script working on different file submissions from the github repo:

---

- Repo 1 Link: https://github.com/ucsd-cse15l-f22/list-methods-lab3

![Image2](/Report_5_Images/Image2.png)

---

- Repo 2 Link: https://github.com/ucsd-cse15l-f22/list-methods-lab3

![Image2](/Report_5_Images/Image2.png)