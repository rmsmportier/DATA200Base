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
