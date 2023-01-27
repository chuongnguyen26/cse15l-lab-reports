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
