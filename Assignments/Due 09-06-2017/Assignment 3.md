# CIS 7 - Discrete Structures - Assignment 3
Due 9/06/2017

Part 1: Prepare Your GitHub Account.

  - [X]  Sign in to GitHub    
  - [X]  Create a file for exercise answers called "Assignment 3"

Part 2: Reading & Exercises

  - [X] Read Chapter 1.1: Statements, Symbolic Representation, and Tautologies
  - [ ] Do Review Questions (in file "Assignment 1" created above):
    - [X] #35
    - [X] #37 - 38
    - [X] #61 - 64

Part 3: Upload your assignment to GitHub

  - [X] git commit -am "assignment 3"
  - [X] git push
  - [X] Email james.wilson@rccd.edu to indicate that the assignment is complete

## Answers

### 35. 
Consider the following pseudocode.
         
        repeat
        i = 1
        read a value for x
        if ((x < 5.0) and (2x < 10.7)) or (sqrt(5x) > 5.1) then
         write the value of x
        end if
        increase i by 1
        until i > 5
   The input values for x are 1.0, 5.1, 2.4, 7.2, and 5.3. What are the output values?

        //x = 1.0
        if ((TRUE) and (TRUE)) or (FALSE)
        //pseudocode will print 1.0

        //x = 5.1
        if ((FALSE) and (TRUE)) or (FALSE)
        //pseudocode will not print

        //x = 2.4
        if ((TRUE) and (TRUE)) or (FALSE)
        //pseudocode will print 2.4

        //x = 7.2
        if ((FALSE) and (FALSE)) or (TRUE)
        //pseudocode will print 7.2

        //x = 5.3
        if ((FALSE) and (TRUE)) or (TRUE)
        //pseudocode will print 5.3
___________________________________________          
###  37. 
Rewrite the following statement form with a simplified conditional expression, where the function odd(n)
returns true if n is odd.

    if not((Value1 < Value2) or odd(Number))
    or (not(Value1 < Value2) and odd(Number)) then
    statement1
    else
    statement2
    end if
    
- A = (Value1 < Value2)
- B = odd(Number)
- P = (A v B)'
- Q = (A' ^ B)
- R = P v Q
    
| A | B | P | Q | R |
|---|---|---|---|---|
| T | T | F | F | F |
| T | F | F | F | F |
| F | T | F | T | T |
| F | F | T | F | T |

__R is logically equivalent to (A'), thus:__

    if not(Value1 < Value2) then
    statement1
    else
    statement2
    end if

________________________________________________
### 38. 
You want your program to execute statement 1 when A is false, B is false, and C is true, and to execute
statement 2 otherwise. You wrote

    if not(A and B) and C then
    statement 1
    else
    statement 2
    end if
 Does this do what you want?
 
    ((FALSE and FALSE)' and TRUE) == TRUE
    
__The statement will execute correctly.__

### 61. 
You meet two of the inhabitants of this country, Percival and Llewellyn. Percival says, “At least one of us
is a liar.” Is Percival a liar or a truth teller? What about Llewellyn? Explain your answer.

- A = Percival is a truth-teller
- B = Llewellyn is a truth-teller
- P = A' v B' ("At least on of us is a liar")
- Q = P <-> A (Accounts for contradictions; P can only be true if Percival is a truth-teller)

| A | B | P | Q |
|---|---|---|---|
| T | T | F | F |
| T | F | T | T |
| F | T | T | F |
| F | F | T | F |

In order for Q to be true, Percival must be a truth-teller and Llewellyn is a liar.

### 62.
Traveling on, you meet Merlin and Meredith. Merlin says, “If I am a truth teller, then Meredith is a truth
teller.” Is Merlin a liar or a truth teller? What about Meredith? Explain your answer.

- A = Merlin is a truth-teller
- B = Meredith is a truth-teller
- P = A -> B ("If I am a truth teller, Meredith is a truth-teller")
- Q = P <-> A (Accounts for contradictions; P can only be true or false if Merlin is a truth-teller or a liar, respectively)

| A | B | P | Q |
|---|---|---|---|
| T | T | T | T |
| T | F | F | F |
| F | T | T | F |
| F | F | T | F |

In any case when Merlin is lying, her statement is true (which is a contradiction). Thus, Merlin must be a truth-teller. Merlin's statement is only false when Merlin is a truth-teller and Meredith is a liar, but that contradicts the fact that Merlin is a truth-teller. Therefore, Both Merlin and Meredith are truth-tellers.

### 63.
Next, you meet Rothwold and Grymlin. Rothwold says, “Either I am a liar or Grymlin is a truth teller.” Is
Rothwold a liar or a truth teller? What about Grymlin? Explain your answer

- A = Rothwold is a truth-teller
- B = Grymlin is a truth-teller
- P = A' v B ("I am a liar or Grymlin is a truth teller")
- Q = P <-> A (Accounts for contradictions; P can only be true or false if Rothwold is a truth-teller or a liar, respectively)

| A | B | P | Q |
|---|---|---|---|
| T | T | T | T |
| T | F | F | F |
| F | T | T | F |
| F | F | T | F |

The explanation for this answer is exactly the same as the answer for __#62.__ This makes sense because Rothwold's statement is logically equivalent to Merlin's statement (using the implication rule.)

### 64.
Finally, you meet Gwendolyn and Merrilaine. Gwendolin says, “I am a liar but Merrilaine is not.” Is
Gwendolyn a liar or a truth teller? What about Merrilaine?

- A = Gwendolyn is a truth-teller
- B = Merrilaine is a truth-teller
- P = A' ^ B ("I am a liar but Merrilaine is a truth teller")
- Q = P <-> A (Accounts for contradictions; P can only be true or false if Gwendolyn is a truth-teller or a liar, respectively)

| A | B | P | Q |
|---|---|---|---|
| T | T | F | F |
| T | F | F | F |
| F | T | T | F |
| F | F | F | T |

When Gwendolyn is a truth-teller, his statement is false. Thus, Gwendolyn must be a liar. When Gwendolyn is a liar and Merrilaine is a truth-teller, Gwendolyn's statement is true (thereby contradicting the fact that Gwendolyn is a liar.) Both Gwendolyn and Merrilaine are liars. BAM!
