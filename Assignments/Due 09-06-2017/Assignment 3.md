# CIS 7 - Discrete Structures - Assignment 3
Due 9/06/2017

Part 1: Prepare Your GitHub Account.

  - [X]  Sign in to GitHub    
  - [X]  Create a file for exercise answers called "Assignment 3"

Part 2: Reading & Exercises

  - [X] Read Chapter 1.1: Statements, Symbolic Representation, and Tautologies
  - [ ] Do Review Questions (in file "Assignment 1" created above):
    - [X] #35
    - [ ] #37 - 38
    - [ ] #61 - 64

Part 3: Upload your assignment to GitHub

  - [ ] git commit -am "assignment 3"
  - [ ] git push
  - [ ] Email james.wilson@rccd.edu to indicate that the assignment is complete

## Answers

#### 35. Consider the following pseudocode.
         
          repeat
          i = 1
          read a value for x
          if ((x < 5.0) and (2x < 10.7)) or ("5x > 5.1) then
           write the value of x
          end if
          increase i by 1
          until i > 5
   The input values for x are 1.0, 5.1, 2.4, 7.2, and 5.3. What are the output values?

          //x = 1.0
          if ((TRUE) and (TRUE)) or (FALSE)
          //pseudocode will print 1.0

          //x = 5.1
          if ((FALSE) and (TRUE)) or (TRUE)
          //pseudocode will print 5.1

          //x = 2.4
          if ((TRUE) and (TRUE)) or (TRUE)
          //pseudocode will print 2.4

          //x = 7.2
          if ((FALSE) and (FALSE)) or (TRUE)
          //pseudocode will print 7.2

          //x = 5.3
          if ((FALSE) and (TRUE)) or (TRUE)
          //pseudocode will print 5.3
