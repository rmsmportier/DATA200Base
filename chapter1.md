---
title       : Homework 2
description : R Basics
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise xp:100 skills:1 key:42e6c4c8a9

## Working With R Scripts

Let's expand on in-class exercises and complete some simple R scripts

Complete all instructions in the R Script pane

*** =instructions

In the editor on the right, complete the code according to the following instructions:

- Assign the value 4.6 to the variable *a*
- Calculate the result of the expression using the variable *a* for missing value
- Assign the value 5.2 to the variable *b*
- Calculate the result of the expression using the variable *b* for missing value
- Press Submit Answer

*** =hint
- Put the variable name or value to assign in the spaces provided within the R expressions

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}

# Assign value 4.6 to variable a
____ <- 4.6

# Calculate the result of expression using variable a for missing value
6*____

# Assign value 5.2 to variable b
b ____ ____

# Calculate the result of expression using variable b for missing value
6*____

```

*** =solution
```{r}
# Assign value 4.6 to variable a
a <- 4.6

# Calculate the result of expression using variable a for missing value
6*a

# Assign value 5.2 to variable b
b <- 5.2

# Calculate the result of expression using variable b for missing value
6*b

```

*** =sct
```{r}
test_object("a", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *a*.",
            incorrect_msg = "Look at your value assigned to *a* and compare to instructions.  The assigned value is important")

test_object("b", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *b*.",
            incorrect_msg = "Look at your value assigned to *b* and compare to instructions.  The assigned value is important")

test_output_contains("6*a", incorrect_msg = "Check your expression using variable *a* and compare to instructions.")

test_output_contains("6*b", incorrect_msg = "Check your expression using variable *b* and compare to instructions.")

test_error()

success_msg("Nice work.  Notice that expression results depend on the value associated with the variable even though expressions look much alike.")

```


--- type:NormalExercise xp:100 skills:1 key:04acfaaf97

## Order of precedence PEMDAS

Let's get comfortable with how order of precedence occurs

Place parentheses around each evaluation to represent order of evaluation

Complete all instructions in the R Script pane

*** =instructions

In the editor on the right, complete the code according to the following instructions:

- Place parentheses around exponentiation portion of expression and calculate result of expression
- Place parentheses around exponentation and multiplication portion of expression and calculate result of expression
- Place parentheses around exponentation, multiplication, and integer division portion of expression and calculate result of expression
- Evaluate the expression without parentheses; are the results equivalent?
- Press Submit Answer

*** =hint
- Place parentheses around expressions in the order indicated in instructions

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}

# Place parentheses around exponentiation portion of expression
____2 ^ 3____ * 7 / 2

# Add parentheses for multiplication portion of expression
____(2 ^ 3) * 7 ____ / 2

# Add parentheses for division portion of expression
____((2 ^ 3) * 7) / 2____

# Evaluate expression without parentheses
2 ^ 3 * 7 / 2

```

*** =solution
```{r}
# Place parentheses around exponentiation portion of expression
(2 ^ 3) * 7 / 2

# Add parentheses for multiplication portion of expression
((2 ^ 3) * 7) / 2

# Add parentheses for integer division portion of expression
(((2 ^ 3) * 7) / 2)

# Evaluate expression without parentheses
2 ^ 3 * 7 / 2

```

*** =sct
```{r}
test_student_typed("(2 ^ 3) * 7 / 2", not_typed_msg = "Check placement of parentheses for first expression and compare to instructions.")

test_student_typed("((2 ^ 3) * 7) / 2", not_typed_msg = "Check placement of parentheses for second expression and compare to instructions.")

test_student_typed("(((2 ^ 3) * 7) / 2)", not_typed_msg =  "Check placement of parentheses for third expression and compare to instructions.")

test_student_typed("2 ^ 3 * 7 / 2", not_typed_msg = "Your final expression should have no parentheses, and result should match to third expression.")

test_error()

success_msg("Nice work.  Looking at PEMDAS, E indicates exponentiation first left to right, then Multiplication and Division.")

```


--- type:NormalExercise xp:100 skills:1 key:957c32707f

## Order of precedence PEMDAS (2)

Let's get comfortable with how order of precedence occurs

Place parentheses around each evaluation to represent order of evaluation

Complete all instructions in the R Script pane

*** =instructions

In the editor on the right, complete the code according to the following instructions:

- Place parentheses around exponentiation portion of expression and calculate result of expression
- Place parentheses around exponentation and multiplication portion of expression and calculate result of expression
- Place parentheses around exponentation, multiplication, and addition portion of expression and calculate result of expression
- Place parentheses around exponentation, multiplication, addition, and subtraction portion of expression and calculate result of expression
- Evaluate the expression without parentheses; are the results equivalent?
- Press Submit Answer

*** =hint
- Place parentheses around expressions in the order indicated in instructions

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}

# Place parentheses around exponentiation portion of expression
3 + 6 * 7 - ____ 2 ^ 4 ____

# Add parentheses for multiplication portion of expression
3 + ____ 6 * 7 ____ - (2 ^ 4)

# Add parentheses for addition portion of expression
____ 3 + (6 * 7) ____ - (2 ^ 4)

# Add parentheses for subtraction portion of expression
____ (3 + (6*7) ) - (2 ^ 4) ____

# Evaluate expression without parentheses
3 + 6 * 7 - 2 ^ 4

```

*** =solution
```{r}
# Place parentheses around exponentiation portion of expression
3 + 6 * 7 - ( 2 ^ 4 )

# Add parentheses for multiplication portion of expression
3 + ( 6 * 7 ) - (2 ^ 4)

# Add parentheses for addition portion of expression
( 3 + (6 * 7) ) - (2 ^ 4)

# Add parentheses for subtraction portion of expression
( (3 + (6*7) ) - (2 ^ 4) )

# Evaluate expression without parentheses
3 + 6 * 7 - 2 ^ 4

```

*** =sct
```{r}
test_student_typed("3 + 6 * 7 - ( 2 ^ 4 )", not_typed_msg = "Check placement of parentheses for first expression and compare to instructions.")

test_student_typed("3 + ( 6 * 7 ) - (2 ^ 4)", not_typed_msg = "Check placement of parentheses for second expression and compare to instructions.")

test_student_typed("( 3 + (6 * 7) ) - (2 ^ 4)", not_typed_msg = "Check placement of parentheses for third expression and compare to instructions.")

test_student_typed("( (3 + (6*7) ) - (2 ^ 4) )", not_typed_msg = "Check placement of parentheses for fourth expression and compare to instructions.")

test_student_typed("3 + 6 * 7 - 2 ^ 4", not_typed_msg = "Your final expression should have no parentheses, and result should match to fourth expression.")

test_error()

success_msg("Nice work.  Looking at PEMDAS, E indicates exponentiation first left to right, then Multiplication, then Addition and Subtraction.")

```


--- type:NormalExercise xp:100 skills:1 key:6ce8ebff12

## Evaluating Expression

Let's assign 4 expressions to 4 variables

Complete all instructions in the R Script pane

*** =instructions

In the editor on the right, complete the code according to the following instructions:

- Assign the value of first expression to variable *a*
- Assign the value of second expression to variable *b*
- Assign the value of third expression to variable *c*
- Assign the value of fourth expression to variable *d*
- Press Submit Answer, and look at result for each to understand what occurred

*** =hint
- Use assignment operator and appropriate variable name for each instruction

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}

# Assign value of expression to variable a
____ ____ (-4)^2 + 2

# Assign value of expression to variable b
____ ____ -4^2 + 2

# Assign value of expression to variable c
____ ____ (-4)^(2+2)

# Assign value of expression to variable d
____ ____ -4^(2+2)


```

*** =solution
```{r}
# Assign value of expression to variable a
a <- (-4)^2 + 2

# Assign value of expression to variable b
b <- -4^2 + 2

# Assign value of expression to variable c
c <- (-4)^(2+2)

# Assign value of expression to variable d
d <- -4^(2+2)


```

*** =sct
```{r}
test_object("a", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *a*.",
            incorrect_msg = "Look at your value assigned to *a* and compare to instructions.  The assigned value is important")

test_object("b", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *b*.",
            incorrect_msg = "Look at your value assigned to *b* and compare to instructions.  The assigned value is important")

test_object("c", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *c*.",
            incorrect_msg = "Look at your value assigned to *c* and compare to instructions.  The assigned value is important")

test_object("d", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *d*.",
            incorrect_msg = "Look at your value assigned to *d* and compare to instructions.  The assigned value is important")

test_error()

success_msg("Nice work.  Look at each result closely and try to interpret what expression was evaluated.")

```


--- type:MultipleChoiceExercise lang:r xp:50 skills:1 key:37c9d82c55
## Which variable matches desired expression

Which variable *a*, *b*, *c*, *d* matches to this desired outcome?
- *square negative 4 and add 2 to the result*

Variables created in previous exercise already exist
 
*** =instructions
- *Value assigned to a, (-4)^2 + 2*
- *Value assigned to b, -4^2 + 2*
- *Value assigned to c, (-4)^(2+2)*
- *Value assigned to d, -4^(2+2)*

*** =hint
Look at expression for each variable and the result, select the one that matches desired outcome
- You can evaluate by entering variable name and pressing enter in R console pane

*** =pre_exercise_code
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer

a <- (-4)^2 + 2

b <- -4^2 + 2

c <- (-4)^(2+2)

d <- -4^(2+2)
```

*** =sct
```{r}

msg_bad = "That is not correct!"
msg_success = "Exactly! Parentheses ensure the value -4 is squared, and then using PEMDAS addition of 2 occurs."
test_mc(1, feedback_msgs = c(msg_success, msg_bad, msg_bad, msg_bad))
```

--- type:MultipleChoiceExercise lang:r xp:50 skills:1 key:0ae4eb0240
## What Is the Data Type?

Four variables *a*, *b*, *c*, and *d* have been pre-loaded into your R session.  

In the R Console, use *typeof(a)*, *typeof(b)*, etc. to assist in answering the following.

Which of the following describes the "atomic" type for each variable?
 
*** =instructions
- *a* is *double*, *b* is *integer*, *c* is *logical*, and *d* is *character*
- *a* is *integer*, *b* is *integer*, *c* is *character*, and *d* is *logical*
- *a* is *logical*, *b* is *character*, *c* is *double*, and *d* is *integer*
- *a* is *character*, *b* is *logical*, *c* is *integer*, and *d* is *double*

*** =hint
Evaluate the type of each using *typeof()* function. Select the one that matches desired outcome

*** =pre_exercise_code
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer

a <- TRUE

b <- "testing"

c <- 4.52

d <- 5L
```

*** =sct
```{r}

msg_bad = "That is not correct!"
msg_success = "Exactly! *typeof()* always provides the 'atomic' type of individual data values.  As we begin to learn more advanced data structures, these 'atomic' types are the foundation for more advanced data."
test_mc(3, feedback_msgs = c(msg_bad, msg_bad, msg_success, msg_bad))
```

--- type:MultipleChoiceExercise lang:r xp:50 skills:1 key:d6ad617438
## What Is In Your Workspace?

Data has been pre-loaded into your R session.  

In the R Console, use *ls()* to assist in answering the following.

How many variables have been pre-loaded into your environment?
 
*** =instructions
- 4
- 3
- 7
- 2

*** =hint
Use *ls()* to see what is in your workspace

*** =pre_exercise_code
```{r}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer

a <- 5

b <- 6

c <- 9

d <- 10

e <- 12

f <- "Hi there"

g <- TRUE

```

*** =sct
```{r}

msg_bad = "That is not correct!"
msg_success = "Exactly! *ls()* allows us to see the data loaded into current workspace.  This can also be used in combination with *pattern* argument to find specific data."
test_mc(3, feedback_msgs = c(msg_bad, msg_bad, msg_success, msg_bad))
```

--- type:NormalExercise xp:100 skills:1 key:586e1a4488

## What Does Equal Mean?

We are going to explore a bit and learn some new data concepts using R.

Complete all instructions in the R Script pane.

*** =instructions

In the editor on the right, complete the code according to the following instructions:

- Use the assignment operator to assign the result on right to variable *x*.  The syntax on the right is 'c'ombining the data values inside parentheses together.
- Use the *class()* function to evaluate the class of the resulting structure.  Notice that this is not the same as the 'atomic' type.  Class refers to the full grouping of data.
- Leave the commands assigning values to *y* and *z* as they are.
- Print the contents of *x* by entering *x* on its own
- Print the contents of *z* by entering *z* on its own
- Use the *==* operator to compare the value of *x* and *z*.  What happens?
- Press Submit Answer

*** =hint
- Follow the prompts above.  Although you may not fully understand the syntax, focus on what is stored in each variable.


*** =pre_exercise_code

```{r}
# no pec
```

*** =sample_code
```{r}

# Assign the data on the right to the variable x on the left using the assignment operator
x ____ 100

# Use class() function to evaluate the class of the resulting structure.  Did anything unexpected happen?
____(x)

# Calculate the atan() of the reciprocal
y <- atan(1/x)

# Calculate the tan of y, and then take the reciprocal
z <- 1/tan(y)

# Print the contents of x
____

# Print the contents of z
____

# Use the == operator to compare the value of x and z.  
x ____ z


```

*** =solution
```{r}
# Assign the data on the right to the variable x on the left using the assignment operator
x <- 100

# Use class() function to evaluate the class of the resulting structure.  Did anything unexpected happen?
class(x)

# Calculate the atan of the reciprocal
y <- atan(1/x)

# Calculate the tan of y, and then the reciprocal
z <- 1/tan(y)

# Print the contents of x
x

# Print the contents of z
z

# Use the == operator to compare the value of x and z.  
x == z

```

*** =sct
```{r}
test_object("x", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *x*.",
            incorrect_msg = "Look at your value assigned to *x* and compare to instructions.  The assigned value is important")

test_object("y", eq_condition="equal",
            undefined_msg = "Do not modify assignment statement for *y*.",
            incorrect_msg = "Do not modify assignment statement for *y*.  The assigned value is important")

test_object("z", eq_condition="equal",
            undefined_msg = "Do not modify assignment statement for *z*.",
            incorrect_msg = "Do not modify assignment statement for *z*.  The assigned value is important")

test_output_contains("numeric", incorrect_msg = "Check your evaluation of *class* for *x*.")

test_output_contains("TRUE", incorrect_msg = "Check your comparison of *x* and *z*; be sure to use the double == operator.")

test_error()

success_msg("Nice work.  When we assigned the value to *x* and used the *class()* function, we should have observed that the class is numeric.  Atomic type is about individual elements while class is about how elements are grouped.  Integer, double, and complex are all considered *numeric* class.  We completed an operation that we then reversed, and our result seems to have come out equal as we would expect.  Let's investigate further with next exercise.")

```


--- type:NormalExercise xp:100 skills:1 key:2b0a374801

## What Does Equal Mean? (2)

We are going to explore some more and learn some new data concepts using R.

Complete all instructions in the R Script pane.

*** =instructions

In the editor on the right, complete the code according to the following instructions:

- Use the assignment operator to assign the result on right to variable *x*.  The syntax on the right is 'c'ombining the data values inside parentheses together.
- Use the *class()* function to evaluate the class of the resulting structure.  Notice that this is not the same as the 'atomic' type.  Class refers to the full grouping of data.
- Leave the commands assigning values to *y* and *z* as they are.
- Print the contents of *x* by entering *x* on its own
- Print the contents of *z* by entering *z* on its own
- Use the *==* operator to compare the value of *x* and *z*.  What happens?
- Use the *all.equal()* function to compare every element of both *x* and *z* to see if all are equal.  What happens?
- Press Submit Answer

*** =hint
- Follow the prompts above.  Although you may not fully understand the syntax, focus on what is stored in each variable.


*** =pre_exercise_code

```{r}
# no pec
```

*** =sample_code
```{r}

# Assign the data on the right to the variable x on the left using the assignment operator
x ____ 1:1000

# Use class() function to evaluate the class of the resulting structure.  Did anything unexpected happen?
____(x)

# Calculate the atan() of the reciprocal
y <- atan(1/x)

# Calculate the tan of y, and then take the reciprocal
z <- 1/tan(y)

# Print the contents of x
____

# Print the contents of z
____

# Use the == operator to compare the value of x and z.  
x ____ z

# Use all.equal() to compare every element of x and z.
____(x,z)


```

*** =solution
```{r}
# Assign the data on the right to the variable x on the left using the assignment operator
x <- 1:1000

# Use class() function to evaluate the class of the resulting structure.  Did anything unexpected happen?
class(x)

# Calculate the atan of the reciprocal
y <- atan(1/x)

# Calculate the tan of y, and then the reciprocal
z <- 1/tan(y)

# Print the contents of x
x

# Print the contents of z
z

# Use the == operator to compare the value of x and z.  
x == z

# Use all.equal() to compare every element of x and z.
all.equal(x,z)



```

*** =sct
```{r}
test_object("x", eq_condition="equal",
            undefined_msg = "Be sure to assign value to variable *x*.",
            incorrect_msg = "Look at your value assigned to *x* and compare to instructions.  The assigned value is important")

test_object("y", eq_condition="equal",
            undefined_msg = "Do not modify assignment statement for *y*.",
            incorrect_msg = "Do not modify assignment statement for *y*.  The assigned value is important")

test_object("z", eq_condition="equal",
            undefined_msg = "Do not modify assignment statement for *z*.",
            incorrect_msg = "Do not modify assignment statement for *z*.  The assigned value is important")

test_output_contains("numeric", incorrect_msg = "Check your evaluation of *class* for *x*.")

test_output_contains("FALSE", incorrect_msg = "Check your comparison of *x* and *z*; be sure to use the double == operator.")

test_function_result("all.equal")

test_error()

success_msg("Nice work.  When we assigned the value to *x* and used the *class()* function, we should have observed that the class is numeric.  Atomic type is about individual elements while class is about how elements are grouped.  This time however we also see that *x* is a vector with many numeric values.  When we run the same operations we ran previously, every element of x has the same operation applied.  x is called a vector.  This time what we see is that some elements in the reverse operation do not return to their original value.  Real numbers stored in computers are approximated, so we cannot always count on comparing with == to get TRUE result.  It is better to rely on functions like *all.equal()* that support some level of tolerance to evaluate.")

```


