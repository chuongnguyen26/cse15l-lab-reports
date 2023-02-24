# Lab Report 4

- Name: Chuong Nguyen
- Email: chn021@ucsd.edu
---

### Step 1 : Log into ieng6

![Image1](/Lab_4_Photos/Image1.png)

![Image1](/Lab_4_Photos/Image2.png)

Key Pressed: `<Ctrl-r> ssh <enter>`

* The ssh cs15lwi23afp@ieng6.ucsd.edu command was in the search history. But since I don't know where exactly in the search history, I pressed "**Ctrl-R**" to enable search command and searched for the "ssh" pattern. When I found the correct "ssh" command, I pressed "**enter**" to run the "ssh" command line. Since I know that I only use ssh for logging in, searching for the command pattern in the search history will be faster. 

---

### Step 2 : Clone your fork of the repository from your Github account

![Image1](/Lab_4_Photos/Image3.png)


![Image1](/Lab_4_Photos/Image4.png)

Key Pressed: `<Ctrl-r> git <enter>`

* The git clone https://github.com/ucsd-cse15l-w23/skill-demo1-data command was in the search history. But since I don't know where exactly in the search history, I pressed "**Ctrl-R**" to enable search command and searched for the "git" pattern. When I found the correct "git" command, I pressed "**enter**" to run the "git" command line and start cloning the git repo. Since I know that "git clone" lab7 repo was the most recent "git clone" command line I called, by searching "git" pattern should give me the correct git clone command of lab7 repo.

---

### Step 3 : Run the tests, demonstrating that they fail

![Image1](/Lab_4_Photos/Image5.png)

Key Pressed: `cd l <tab><enter>`

* The cd lab7/ command changes my current directory to lab7. Since I know that lab7 is the only sub-directory in my current directory, I pressed "**tab**" to autofill the name of the sub-directory after finished typing "cd l". Once autofill is completed, I pressed "**enter**" to run the command line and change my directory to lab7.

---

![Image1](/Lab_4_Photos/Image6.png)

![Image1](/Lab_4_Photos/Image7.png)

Key Pressed: `<Ctrl-r> javac <enter>`

* The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was in the search history. But since I don't know where exactly in the search history, I pressed "**Ctrl-R**" to enable search command and searched for the "javac" pattern. When I found the correct "javac" command, I pressed "**enter**" to run the "javac" command line and start compiling all java files in the directory. Since I know that "javac" of files in lab7 was the most recent "javac" type command line I called, by searching "javac" pattern should give me the correct javac command line to compile all java files exist in lab7.

---

![Image1](/Lab_4_Photos/Image8.png)

![Image1](/Lab_4_Photos/Image9.png)

Key Pressed: `<Ctrl-r> java <space><enter>`

* The java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests command was in the search history. But since I don't know where exactly in the search history, I pressed "**Ctrl-R**" to enable search command and searched for the "java" pattern. But since "javac" also contains the substring "java", typing "java" alone won't be helpful. To have the pattern "java" stands as its own word, press "**space**" immediately after "java". Once I found the correct "java" command, I pressed "**enter**" to run the "java" command line that will run the TestListExamples file. Since I know that I only ran "java" command line on TestListExamples file prior to the competition, by searching through the search history with the pattern "java**space**>" will give me the correct command line.

---

### Step 4 : Edit the code file to fix the failing test

![Image1](/Lab_4_Photos/Image10.png)

Key Pressed: `nano<space> L <tab> j <tab><enter>`

The nano ListExamples.java command opens a text editor. I typed in "nano" to specify which text editor to use. The "**space**" separates the "nano" text editor and the file. I typed "L" since this is the first letter of java ListExamples file that I will be accessing. Additionally, since the ListExamples is the only file name in the directory that started with the letter "L", so I pressed "**tab**" to autocomplete "ListExamples.". However, there are two different file types with the same file name, so I typed "j" to specify the file type and pressed "**tab**" to autofill the rest of the word "java". Once done, I pressed "**enter**" to run the command line and open the nano text editor for the ListExamples.java file.

---

![Image1](/Lab_4_Photos/Image11.png)

Key Pressed: `<Ctrl-w> index1 <enter>`

The Search: index1 command is used to find the first occurence of the specified pattern in the file. I used "**Ctrl-W**" to enable the search, in order to locate the first occurence of the pattern in the ListExamples.java file. Afterward, I typed "index1" as the pattern I want to look for in the file. Once done with stating the pattern, I pressed "**enter**" to look for the first occurrence of "index1".

---

![Image1](/Lab_4_Photos/Image12.png)

Key Pressed: `<down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><right><right><right><right><delete><2>`

I pressed "**down**" 17 times because the variable index1 that I wanted to change locates 14 lines below the first occurence of "index1" that I used "Ctrl-W" to locate. To change from "index1" to "index2", I moved the cursor "**right**" 4 times. Afterward, I pressed "**delete**" to remove the number 1 from index1 and pressed "**2**" to replace 1.

---

![Image1](/Lab_4_Photos/Image13.png)

Key Pressed: `<Ctrl-o><enter><Ctrl-x>`

Once done, I pressed "**Ctrl-o**" to initiate the same of my updated ListExamples.java file. I then pressed "**enter**" to save the newly updated code block to the ListExamples.java file. Afterward, I pressed "**Ctrl-x**" to exit the nano text editor and return to my terminal.

### Step 5 : Run the tests, demonstrating that they now succeed
 
### Step 6 : Commit and push the resulting change to your Github account