## Compute in Small Steps

Humans and computers compute in small steps.  Larger problems can be solved by combining results from small computations.

Before the invention of the computers, humans who worked doing calculations were called `Computers`.

But humans are limited in speed and memory; computers were created to perform the job of `Computers` when the job required lots of data that needed to be computed into useful results.

## Compute only Numbers using Basic Arithmetic

Humans defined Math and Arithmetic in small increments by creating definitions of the properties of numbers. These definitions allowed a human to memorize them and to compute them just by using mental recall.

From those smaller Math definitions, larger definitions were created.  The proof or steps that lead to the new definition is considered an algorithm--the series of small definitions or computations that lead to the new definition or `solution`.

## Use Tools and Algorithms when Problems take Longer to Compute

Some problems are more difficult to compute because the problem involves a large quantity of numbers and therefore requires many small steps to arrive at the result.  Memorization then became a limiting factor for humans.  

Humans then invented the paper and pencil to record intermediate results as a memory aid.  The use of paper and pencil was the beginning in the evolution to using more powerful tools that eventually led to the creation of the digital computer.

Example:
To compute the sum of three and two, you don't need to write down the following steps because you already memorized the solution and quickly know the answer.

```
sum of three and two
    3 + 2
is    5
```

But if you were asked to sum two very large numbers, you may find the need to write down both numbers in specific areas of your paper.  This allows the human to keep track of intermediate computations and eventually arrive at the result.

We were thought to align the numbers in the following form:
```
    7345235
  +   96734 
   --------
         
```

Then arrive at the result by adding the two pairs of digits starting from right to left, and keeping track of the digit 1 that results when the previous addition is 10 or grater.
```
     11
    7345235
  +   96734
   --------
    7441969
```

**Question**: What new tools were used in the previous exercise?
**Question**: Can you write down the algorithm that you were taught by your teachers that allowed to solve the above problem?

## Memory Recall Tools

### Ability to Distinguish Different Numbers and Digits
In the previous exercise we intentionally used `different locations` of the paper to `distinguish` the two different numbers being added.  We also `aligned` them in such way that pairs of digits were `selected` in each `step`.

**Note**:
The paper didn't do the calculation, we (human) did the actual calculation on each pair of digits and we wrote the intermediate results in other areas of the paper.

The paper and its different locations were used as tools.

Digital computers use similar tools.  For example the computer memory is a very long sequence of registers, each register is `located` by an address number.  So there are many different locations where different numbers can be stored, and then can be computed.

The computer memory doesn't perform the calculations either; the computer's processing unit (CPU) performs the calculations.  The CPU also reads numbers from the various memory registers, places them in other convenient registers, performs the calculation, and finally writes the result in a chosen register.

This is very similar to how humans act as computers using paper and pencil.

### Following Algorithms

We then followed the algorithm that we learned from our teachers in elementary school.  And we were successful.

I don't remember my teachers ever writing the algorithm for adding two large integers.  The teacher instead would use the whiteboard or paper to demonstrate computations visually.  We would observe and would follow those steps, and eventually memorize them.

Computers, at least the fundamental computers, don't have eyes and don't learn like we do.  But they can follow any algorithm we write as programs.

We will write algorithms that can be translated to algorithms that a computer can follow

## Basic Definitions in Arithmetic (Domain Knowledge)

The domain knowledge in computers is only Arithmetic.  We must understand it first, before we can solve problems in other
domain knowledge areas.

### Addition, Subtraction, Multiplication, Division

The operators (functions) are `binary`; that is, they take two operands (arguments)

```
a + b
a - b
a * b  (multiplication)
a / b  (division)
```

When there are more than two operands, associate them by two, as required by the `binary` operators

```
Associate Property:
a + b + c = (a + b) + c = a + (b + c)

The association can be started from left or right
```

## Problem

What is the sum of 3 5 8 and 2?

### Write down your proposed solution using your domain knowledge

```
3 + 5 + 8 + 2 = ?
```

### Write down necessary smaller steps using your domain knowledge

Associate two operands at a time from left
```
(3 + 5) + 8 + 2
   8    + 8 + 2
    (8 + 8) + 2
      16    + 2
       (16 + 2)
          18
```          

### Result of the computation

```
3 + 5 + 8 + 2 = 18
```

### Variables

The previous steps were using a memory helper by writing down the intermediate result.  You can use a variable to keep
track of the intermediate result.

You can assign a value to a variable, for example `result`.  **Note**: the operator `=` or `<-` indicate setting the contents of variable `x` to the
given value.
```
result = 5
or 
result <- 5

```

You can replace the contents of the variable with other values or expressions.  The expressions can contain the previous value
of the variable

```
r = 5
r = r + 2
is equivalent to
r = 5 + 2
finally
r is 7

the final result of r is 7, by replacing the previous value 5 on the right hand side of the = operator
```

Now, let's try using memory helpers in the previous problem to store the temporary computations
```
(3 + 5) + 8 + 2
assign the first computation to r
r = 3 + 5
r = 8

continue with the steps
      r + 8 + 2
    (r + 8) + 2
replace r with the next computation
r = r + 8
r = 8 + 8
r = 16

continue with the steps
          r + 2
replace r with the next computation
r = r + 2
r = 16 + 2
r = 18

the result of all the operations are contained in r
           r
           18
```

## Definitions from Smaller Definition (More Domain Knowledge)

The power of a number is defined from the definition of multiplication
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

Using variables
```
r = 1                              0 repetitions
r = r * x = 1 * x                  1 repetition
r = r * x = (1 * x) * x            2 repetitions
r = r * x = (1 * x * x) * x        3 repetitions
r = r * x = (1 * x * x . . .) * x  y repetitions
```

## Algorithms

An algorithm is the description of the steps used to compute the solution.  

The solution is typically a definition or mathematical equation.  The symbol `=` indicates equality.

An algorithm that uses variables, uses the symbol `=` to indicate an assignment of a value to a variable.  It replaces the current value of the variable.

### Power definition:
```
x^y = 1 * x * x * x * . . . * x    for y repetitions
```

### Algorithm:
```
r = 1
repeat y times:
   r = r * x
The result is then the last value of r.
```

### Test: 2^3

we expect
```
2^3 = 1 * 2 * 2 * 2 = 8
```
Compute the following:
```
r = 1
repeat 3 times:
   r = r * 2
the last value of r is the result
```

1 iteration:
```
r = r * 2 
  = (1) * 2
r = 2
```
2nd iteration:
```
r = r * 2 
  = (2) * 2
r = 4
```
3rd iteration:
```
r = r * 2 
  = (4) * 2 = 8
r = 8
```
The final value of `r` is 8 as expected

### Test 2^0

we expect
```
2^0 = 1
```
Compute the following:
```
r = 1
repeat 0 times:
   r = r * 2
the last value of r is the result
```
Since there are no (0) repetitions, the last value of r is 1, which is expected.


```flow
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op
​```

