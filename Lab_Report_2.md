# Lab Report 2

- Name: Chuong Nguyen
- Email: chn021@ucsd.edu
---

## Part 1

- Below are some of the images displaying codes that show how a web server is made.
![Image-1](photo_1.png)
![Image-2](photo_2.png)
- In this '**StringServer.java**' file, I have two classes, a handler class and a StringServer class. The handler class is supposed to handle all requests made by the users. While, the StringServer class will be responsible for starting the server.

1. Class Handler implements an interface URLHandler:
    - The class has two field variables and two methods, one is a private helper method and the other is a public method.

    1. Field Variables:
        - Variable size is an integer type that takes note of the number of elements in the array. The variable will be incremented after each time a new element is added.
        - Variable list is an array type that holds the cumulative input strings from user requests.
    2. Methods:
        - The expandList method is a helper method which takes in an array of String type referencing to a list object containing all current input elements. This method is supposed to expand the length of list array by ten more indices when the number of element (size) is equal to the current array length.
        - The handleRequest is a public method that returns an output corresponding to the user request. If the url's path is equal to '/' then return a statement informing user the avaible requests that the users could make. If the request is equal to the 'add-message', the computer will find the query and make a comparison. Before comparing the query, the query will be splitted into two elements, each storing data on each side of the equal sign. If the right side of the query is equal to 's', the left side will be appened to the list array. After each call, the all string elements in the list array will be concatenated to a single string and display the output to the user on the webpage.
2. Class StringServer:
    - The class has one public method that will start the web server.

    1. Method:
        - The main method will look for an input value which is equivalent to port number in order to start the server, while the input is valid in the range from 1024 to 49151. When the input value taken from the terminal is the valid, the value will be converted from String to an Integer which will be used as the port number. Afterward, the server will starter by creating a new handler object.

- Note: This algorithm could be shortened by just concatenating all inputs to a single string instead of having to store in an array and iterate through the array using the for loop to access and append elements to a single array. Despite the shorter route, I encountered a problem using just the string instead of the array. The problem was that everytime when I make a new request to add a new word, both the last previous term and newly requested term will both be concatenated despite the previous word has already been added. Meaning that each term will be unintentionally added twice to the list. I later found out that the problem was caused by me using the device memory to paste the previous url link and replace the old term with the new term in query. Though the problem was found, I decided to continue with my current approach because I think it is beneficial for me to practice with arrays, lists, and data structures expecially while taking CSE 12.

---

![Image-3](photo_3.png)

- In the terminal, I compiled both the StringSever.java and Server.java files. After word, I ran the java StringSever file with the port number equals to 4585. Once entered, a local url link will be displayed for the user to view. In the terminal, I have the query printed out after each request made to make sure the server works correctly and to make it easier for debugging.

---

![Image-4](photo_4.png)

1. Which methods will be called?
    - The main method in class StringServer will always be called in order for the web server to be up and running. When the web server first runs, the handleRequest method will be called to handle '/' request which will return a statement telling users the next option to choose.
    - In the example above, method handleRequest will be called to handle request of path equals to 'add-message' and query equals to '?s=String' which in this case is 'Hello'. 
    - Since 'Hello' is the first element in the list array with length up to 5, expandList will not be called.

2. What are the relevant arguments to those methods, and the values of any relevant fields of the class? 
    1. Relevant Arguments:
        - For the handleRequest method in the Handler class, the argument contains one URI object. This URI object will be used to determine the request made by the users.
        - For the main method in the StringServer class, the argument contains a string array that takes in all user inputs from the terminal. In this case, the value 4585 will be taken in and read as the port value for the server.
        - For the expandList method in the Handler class, the argument contains a string array which holds the same reference to the list array object. The array will be used to detemine the new length of the array after expansion, and also to transfer all elements from the old array to the new array. Since the array has fixed length, expansion could only be possible by creating a bigger array and transfer all current elements to the new array. However, since this method is not called no relevant value is passed to the method's argument.
    2. Relevant Fields:
        - There are only two field variables in this file, and both happend to be in the handler class. The size variable which is initialized to zero will keep track of the number of elements in the Array. While the list of string array is initially set to an object with length 5 to store elements from user requests for display on the server after each valid request. After the request is handled, the size is equal to 1 and 'Hello' is added to the first index in the list array.
3. How are the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
    - The values of any relevant fields will be perceived as string type when passing as requests. So no matter what type of fields the values are, the values will always be added to the list and printed out as string type. Each time a new string is added, the size of list will be incremented by one.

![Image-5](photo_5.png)
(Note: Since the url in mac will just display localhost and port value, so in order to see the path and query, I have to click on the search bar for full display of the url. )

1. Which methods will be called?
    - The main method in class StringServer will not be called because the server is already running.
    - In the example above, method handleRequest will be called to handle request of path equals to 'add-message' and query equals to '?s=String' which in this case is 'How_are_you    '. 
    - Since 'How_are_you' is the second element in the list array with length up to 5, expandList will not be called.

2. What are the relevant arguments to those methods, and the values of any relevant fields of the class? 
    1. Relevant Arguments:
        - For the handleRequest method in the Handler class, the argument contains one URI object. This URI object will be used to determine the request made by the users.
        - For the main method in the StringServer class, the argument contains a string array that takes in all user inputs from the terminal. In this case, the value will be taken in and read as the port value for the server, while the value is valid.
        - Since expandList is not called, no value will be passed to the argument.
    2. Relevant Fields:
        - There are only two field variables in this file, and both happend to be in the handler class. The size variable which is initialized to zero will keep track of the number of elements in the Array. While the list of string array is initially set to an object with length 5 to store elements from user requests for display on the server after each valid request. After the request is handled, the size is equal to 2 and 'How_are_you' is added to the second index in the list array.
3. How are the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
    - The values of any relevant fields will be perceived as string type when passing as requests. So no matter what type of fields the values are, the values will always be added to the list and printed out as string type. Each time a new string is added, the size of list will be incremented by one.

---

## Part 2

- Bugs from the methodInPlace:
    - failure-inducing input
        ```
        import static org.junit.Assert.*;
        import org.junit.*;

        public class ArrayTests {
            @Test 
            public void testReverseInPlace() {
                int[] input3 = {1,2};
                ArrayExamples.reverseInPlace(input3);
                assertArrayEquals(new int[]{2,1}, input3);


                int[] input4 = {1,2,3};
                ArrayExamples.reverseInPlace(input4);
                assertArrayEquals(new int[]{3,2,1}, input4);
                assertArrayEquals(new int[]{1,2,3}, input2);
                assertArrayEquals(new int[]{3,2,3}, input2);

                int[] input5 = {1,2,3,4};
                ArrayExamples.reverseInPlace(input5);
                assertArrayEquals(new int[]{4,3,3,4}, input3);
            }
        }
        ```
        - These inputs will induce errors in the JUnit test because the length of list array is more that 1 index long. Since the algorithm only reverses the first half of the list and keep the second half the same, any inputs with list longer than one index, no matter if the list has odd or even amount of elements, will fail the JUnit test.

    - Input not inducing failure:
        ```
        import static org.junit.Assert.*;
        import org.junit.*;

        public class ArrayTests {
            @Test 
            public void testReverseInPlace() {
                int[] input1 = { 3 };
                ArrayExamples.reverseInPlace(input1);
                assertArrayEquals(new int[]{ 3 }, input1);

                int[] input2 = {};
                ArrayExamples.reverseInPlace(input2); 
            }
        }
        ```
        - These inputs will not induce a failure in the JUnit test because since the length of the array is one index or less, reversing or not reversing will both result in the identical display.
    
    - The symptoms:
        - Symptoms when inputs induce error:
        ![Image-6](photo_6.png)
            - When JUNit fails, there will be an error message displaying in the terminal. As in this example, the test failed on line 18 of ArrayTests.java file. The test expected the value 1 at index 1 but displayed 2. Normally, testing would stop immediately after encountering the first error which in this case happens at line 18 where I anticipated {2,1} to return.
            
        - Symptoms when inputs do not induce error:
        ![Image-7](photo_7.png)
            - For the inputs {} and { 3 }, both scenarios passed the JUnit test because both have an array length of 1 or less. As the length becomes greater than one, JUnit will start to fail as the reverseInPlace method only reverses the first half of the list while keeping the second half the same. In essence, the method mirrors values from both ends going toward the center, instead of actually reversing the order from beginning to the end.
    
    - The bug:
        - Before:
            ```
            static void reverseInPlace(int[] arr) {
                for(int i = 0; i < arr.length; i += 1) {
                arr[i] = arr[arr.length - i - 1];
                }
            }
            ```

        - After:
            ```
            static void reverseInPlace(int[] arr) {
                for(int i = 0; i < arr.length/2; i += 1) {
                int temp = arr[i];
                arr[i] = arr[arr.length - i - 1];
                arr[arr.length - i - 1] = temp;
                }
            }
            ```
        ![Image_8](photo_8.png)

- Briefly describe why the fix addresses the issue?
    - The original reverseInPlace method failed the JUnit test when the length of list was greater than 1. The reason was because during the process of reversing, the method failed to store the first half of the elements, so when the setting the first half indeces equal to the second half elements, none of the first half elements were saved. Due to this reason, when setting the second half idices to the first half elements, the first half elements are now elements of the second half. Instead of reversing, this algorithm simply mirrored the values of one half to the other. To address the bug, I set the for loop to run half of the list's length value. I then store the element at index i as temporary, set index i equals to the element at index list's length subtract i and 1, and set the index list's length subtract i and 1 equals to element being stored as temporary. Doing so, I can ensure of not losing the first half elements when setting the first half idices to the second half elements. Finally to not mirror the other half, I set the second half idices to the first half emlements being temporarily stored at a local variable.

---

## Part 3:

- In week 2, I learned how to create a local and remote web servers. I also learned how to manipulate paths and queries of the url, and just changing the displays regarding different requests. In week 3, I learned how to come up with more efficient test cases and the process of looking for symptoms and debugging the algorithm. The labs have taught me new skills and applications that are very useful for my programmings.