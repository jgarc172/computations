## Compute Using Basic Operations

Humans and computers compute in small steps using the most basic operations in arithmetic; for example, the addition operator (`+`).  Larger problems or more complex operations can be solved by combining results from small computations; for example the definition of the multiplication operator (`*`) is based on the use of the addition operator.

## Operations and Problems

Start conceptualizing your problems in the same way that Arithmetic operations are represented.  For example:

```
  2 + 3 = 5
```

Your problem could be conceptualized in this form:

```
  I have: 2 and 3
  I want: their sum
                 - - - - -
                |         |
  (2, 3) - - -> |    ?    |- - -> sum
                |         |
                 - - - - -
```

To solve your problem, think about any tool (operation) that you already have that might solve your problem.

Since this is a simple problem, we could use one simple operation, the addition operator, (`+`) to implement your needed solution:

```
                 - - - - -
                |         |
  (2, 3) - - -> |    +    |- - -> 5
                |         |
                 - - - - -
```

## The "How" in your Problem Statement

So, your problem statement can be expresses as:

`How` can I compute `what I want` from `what I have`?

And it can be visualized as this:
```
                        - - - - -
                       |         |
  (what I have) - - -> |  how?   |- - -> (what I want)
                       |         |
                        - - - - -
```

## Algorithms

When you write the steps in the "How", you would have found one of many possible solutions.  These steps are also called an `"algorithm"`.

```
                        - - - - -
                       |         |
  (what I have) - - -> |algorithm|- - -> (what I want)
                       |         |
                        - - - - -
```
In our example above, our algorithm is one of the simplest algorithms you would find, which is applying the `+` operator on the the two numbers that we have.

## Definitions, Computations, and Sets

Mathematics defines the set of numbers and their operations.  It also defines how elements in a set of numbers can be distinguished using symbolic representation.

## The Need for Tools

Before the invention of digital computers, humans who worked doing calculations were called `Computers`.  They memorized the results of calculations for small numbers, and used tools like paper and pencil to calculate larger numbers or larger quantities of smaller numbers.

But humans are limited in speed and memory; digital computers were created to perform the job of `Computers` when the job required lots of data that needed to be computed into useful results.


### Example:
To compute the sum of three and two, you probably don't need to write down the following steps because you might have already memorized the solution and would quickly know the answer.

```
sum of three and two
    3 + 2
is    5
```

But if you were asked to sum two very large numbers, like 
```
7345235 and 96734
```
Unless you are super-smart, you may not know the answer from memory.  Then we go back to asking the question, `how` do we add these two large numbers to obtain the sum?

```
                   - - - - -
  7345235         |         |
    and    - - -> |  how?   |- - -> (sum)
   96734)         |         |
                   - - - - -
```

you may find the need to write down both numbers in specific areas of your paper.  This allows you to keep track of intermediate computations and eventually arrive at the result.

We were taught to align the numbers in the following form:
```
    7345235 <--- first number
  +   96734 <--- second number
   --------
         
```

Then we would arrive at the result by following an algorithm such as,

"add two pairs of digits and any carry over, at a time, starting from right to left.  Intermediate results are to be written down in corresponding areas of the paper: the sum of each pair is written down below the line; the carry over digit would be written on the top of the next pair of digits.
```
    0110000 <--- carry digits
    7345235 <--- first number
  + 0096734 <--- second number
   --------
    7441969 <--- result number
```

If we call the algorithm above, alg1, then we can visualize it as

```
                   - - - - -
  7345235         |         |
    and    - - -> |  alg1   |- - -> 7441969 
   96734)         |         |
                   - - - - -
```

**Question**: What new tools were used in the previous exercise?

## Memory Recall Tools

### Ability to Distinguish Different Numbers and Digits
In the previous exercise we intentionally used `different locations` of the paper to `distinguish` the two different numbers being added.  We also `aligned` them in such way that pairs of digits were `selected` in each `step`. 

We also used other parts of the paper to `identify` intermediate results.  The area for the carry over digits is used temporarily and then is ignored; the area for the result number is temporarily used, digit by digit.  At the end of the calculations, the complete set of digits is identified as the resulting number, the sum.

**Note**:
The paper didn't do the calculation, we (human) did the actual calculation on each pair of digits and we wrote the intermediate results in other areas of the paper.

**The paper and its different locations were used as tools.**

Digital computers use similar tools.  For example the computer memory is a very long sequence of registers that contain a sequence of digits, each register is `located` and identified by an address number.  So there are many different locations where different numbers can be stored, can be retrieved from, and then can be computed to form new numbers that are stored in other locations.

The computer memory doesn't perform the calculations either; the computer's processing unit (CPU) performs the calculations.  The CPU also reads numbers from the various memory registers, places them in other convenient registers, performs the calculation, and finally writes the result in a chosen register.

This is very similar to how humans act: as computers using paper and pencil.

### Following Algorithms

Notice that we followed the algorithm that we learned from our teachers in elementary school.  And we were successful.

I don't remember my teachers ever writing the algorithm for adding two large integers.  The teacher instead would use the whiteboard or paper to demonstrate computations visually.  We would observe and would follow those steps, and eventually memorize them.

Computers, at least the fundamental computers, don't have eyes and don't learn like we do.  But they can follow any algorithm we write as programs.

We will write algorithms understood by humans and that can be translated to algorithms that a computer can follow

## Basic Definitions in Arithmetic (Domain Knowledge)

The domain in computers is only Arithmetic.  We must understand it first, before we can solve problems in other domains.

### Addition, Subtraction, Multiplication, Division

The arithmetic operators (functions) for numbers are `binary`; that is, they take two operands (arguments) that are numbers and their result is another number

```
a + b
a - b
a * b  (multiplication)
a / b  (division)
```

When there are more than two operands, we use arithmetic's associative property to group them by two, as required by the `binary` operators

```
Associative Property:
a + b + c = (a + b) + c = a + (b + c)

The association can be started from left or right
```

## A Simpler Problem

What is the sum of 3, 5, 8, and 2?

### Write down your proposed solution using your domain knowledge

```
3 + 5 + 8 + 2 = ?
```

Again, we used different areas, locations, to distinguish the different numbers.

### Write down necessary smaller steps using your domain knowledge

Associate two operands at a time from left, then apply the operation.
```
(3 + 5) + 8 + 2
   8    + 8 + 2
    (8 + 8) + 2
      16    + 2
       (16 + 2)
          18
```          
Again, we used new areas, locations, to write down intermediate results.
### Result of the computation

```
3 + 5 + 8 + 2 = 18
```

### Variables

You can use a label (variable) to keep track of (to distinguish) the intermediate results.  This is a memory helper for both humans and eventually will also be useful when writing computer programs.

#### Variable Notation:
You can assign a value to a variable, for example `x`.  **Note**: the operator `=` or `<-` indicate setting the contents of variable `x` to the
given value.
```
x = 5
or 
x <- 5

```
To avoid confusion with the mathematical symbol `=`, we will use `<-` for now to indicate the assignment operator.

You can replace the contents of the variable with other values or expressions.  The expressions can contain the previous value
of the variable

```
r <- 5
r <- r + 2
is equivalent to
r <- 5 + 2
finally
r is 7

the final result of r is 7, 
by replacing the previous value 5 on the 
right hand side of the <- operator
```

Now, let's try using a variable `r` as a memory helper in the previous problem to store the temporary computations.
```
(3 + 5) + 8 + 2
assign the first computation to r
r <- 3 + 5
r <- 8

continue with the steps
      r + 8 + 2
    (r + 8) + 2
replace r with the new computation
r <- r + 8
r <- 8 + 8
r <- 16

continue with the steps
          r + 2
replace r with the new computation
r <- r + 2
r <- 16 + 2
r <- 18

the result of all the operations are contained in the last
value of r
           r is 18
```

**Note**: All the previous values in `r` were discarded by overwriting them with a new value.  We kept the very last value as the result.  We could have used several distinct variables for each step, but it is more efficient to reuse a single variable when its intermediate values are temporary and will not be used for the final result.

## Generalize
As you write down the steps for your solution, pay attention to the patterns that emerge.  This is generalization.  It allows to define solutions for a general set of values.

### Pattern: Accumulator

We just discovered a pattern in the previous exercise:
```
r <- r + N

where r and N are numbers
```


The pattern can work with other operators:
```
r <- r * N
r <- r - N
```

### Pattern: Repetition

In the previous exercise we also noticed that the pattern repeated. But at this point it is difficult to write down the pattern because we did not label the different four integers.

We can expand on the concept of the variable.  The variable we used contained a single integer, one single value.  We can designate variables that contain a group of values.  A group of values is typically known as an array or list of values.

We can use the following notation to assign the four values to a variable N:
```
N <- [3, 5, 8, 2]
or
N <- {3, 5, 8, 2}
```

Each individual value can be recalled using the following notation:
```
N[i]
where i is an integer and is used as an index
```
In our exercise, we had four values; so the `i` variable can start from 1, and end with 4.
```
N[1] is 3
N[2] is 5
N[3] is 8
N[4] is 2
```
It is a convention in many programming languages to have arrays elements start with the index value of 0.  Such that the values will be referenced as follows:
```
N[0] is 3
N[1] is 5
N[2] is 8
N[3] is 2
```

Now it is easier to write down the concept of repetition.

Repetition has a `start` and an `end`.  In our case the index `i` starts at 1 and ends at 4 (or starts at 0 and ends at 3).

## Our First Written Algorithm

Here is an algorithm that describes our previous exercise to sum a list of integers:
```
N <- [3, 5, 8, 2]
r <- 0
Repeat for each value in N (with an index i from 0 to 3):
   r <- r + N[i]

The result is the last value of r.

```

Let's test it:
```
Before the repetition:
r <- 0

During the Repetition:

   when i is 0:
      r <- r + N[0]
      r <- 0 + 3
      r <- 3

   when i is 1:
      r <- r + N[1]
      r <- 3 + 5
      r <- 8   

   when i is 2:
      r <- r + N[2]
      r <- 8 + 8
      r <- 16 

   when i is 3:
      r <- r + N[3]
      r <- 16 + 2
      r <- 18

The last value of r is the result, 18.  It passed the test!
```

## Definitions from Smaller Definition (More Domain Knowledge)

## Multiplication

The multiplication of two integers, x and y:
```
x * y = x + x + x . . . for y instances of x (repetition)
```

More general:
```
x * y = 0 + x + x + x . . . for y instances of x 
```

more specific
```
x * 0 = 0                            0 repetitions
x * 1 = 0 + x                        1 repetition
x * 2 = 0 + x + x                    2 repetitions
x * 3 = 0 + x + x + x                3 repetitions
x * y = 0 + x + x + x + . . . + x    y repetitions
```

### Algorithm for x * y

An **algorithm** that can be translated to a computer program:

x * y:
```
r <- 0
Repeat y times, using an index i from 1 to y:
   r <- r + x

The result is the last value of r.
```

### Test: 2*3

we expect
```
2*3 = 0 + 2 + 2 + 2 = 6
```
Compute the following specific algorithm:
```
r <- 0
Repeat 3 times, using an index i from 1 to 3:
   r <- r + 2
the last value of r is the result
```

i is 1:
```
r <- r + 2 
  <- (0) + 2
r <- 2
```
i is 2:
```
r <- r + 2 
  <- (2) + 2
r <- 4
```
i is 3:
```
r <- r + 2 
  <- (4) + 2
r <- 6
```
The final value of `r` is 6 as expected

### Test 2*0

we expect
```
2*0 = 0
```
Compute the following:
```
r <- 0
Repeat 0 times, using an index i from 1 to 0:
   r <- r + 2
the last value of r is the result
```
Since there are no (0) repetitions, the last value of r is 0, which is expected.

### Algorithm for x ^ y

The power of a number is based on the application of multiplication
```
x^y = x * x * x * . . . * x for y instances of x (repetition)
```
more general
```
x^y = 1 * x * x * x * . . . * x for y instances of x
```

more specific
```
x^0 = 1                            0 repetitions
x^1 = 1 * x                        1 repetition
x^2 = 1 * x * x                    2 repetitions
x^3 = 1 * x * x * x                3 repetitions
x^y = 1 * x * x * x * . . . * x    y repetitions
```


**Algorithm**: x ^ y
```
r <- 1
Repeat y times, using an index i from 1 to y:
   r <- r * x
The result is then the last value of r.
```

### Test: 2^3

we expect
```
2^3 = 1 * 2 * 2 * 2 = 8
```
Compute the following:
```
r <- 1
Repeat 3 times, using an index i from 1 to 3:
   r <- r * 2
the last value of r is the result
```

i is 1:
```
r <- r * 2 
  <- (1) * 2
r <- 2
```
i is 2:
```
r <- r * 2 
  <- (2) * 2
r <- 4
```
i is 3:
```
r <- r * 2 
  <- (4) * 2 <- 8
r <- 8
```
The final value of `r` is 8 as expected

### Test 2^0

we expect
```
2^0 = 1
```
Compute the following:
```
r <- 1
Repeat 0 times, using an index i from 1 to 0:
   r <- r * 2
the last value of r is the result
```
Since there are no (0) repetitions, the last value of r is 1, which is expected.



