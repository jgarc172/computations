## Algorithm for x * y

Let's prove one algorithm for `x * y`.

The "What" is a mathematical definition:
```
x * y = 0 + x + x + x . . . for y instances of x 
                            and y is a whole number
```

Here is one of several algorithms for `x * y` :

```{.line-numbers}
r <- 0
Repeat y times, using an index i from 1 to y:
   r <- r + x

The result is the last value of r.
```

To Prove: for all whole numbers in `x` and `y`, the algorithm computes the product `x * y`.
### Termination:
The algorithm repeats y times and terminates as described in line 2.

### Correctness (produces the expected result)

**By Induction**:

The Loop Invariant: The property of the loop is itself the definition of `x * y` which is assumed to be true, and `i` is `y`.  Line 3 in the loop represents this truth as `r <- r + x`.  The property of this statement says, "the result is the addition of the previous result plus x"

Thus, the Loop Invariant is
``` 
mathematical property <-> Loop property
x * y <-> r <- r + x, after y repetitions
x * y <-> r, at the end of the loop
```

Base Case:
`x * y`: when y is `0`, `x * y` is `x * 0` is `0`

In the algorithm:

* r is 0 in line 1
* when y is 0, line 3 is never executed (Repeat 0 times)
* the result r is 0

Thus:
```
0 <-> 0
```

Inductive Case: 

`x * y`: for y=k, assume `x * k` is true

In the algorithm: for y=k, assume `r <- x * k` is true

Prove that that the Loop Invariant is also true for `y = k + 1`

`x * y`: for y = k + 1,

```
x * y
x * (k + 1)
```

In the algorithm: for y = k + 1, the previous r was `x * k` when y was k
```
r <- r + x
r <- (x * k) + x
r <- x * (k + 1)
```

thus:
```
x * (k + 1) <-> x * (k + 1)
```

Summary:
The algorithm always produces the expected result for any `y`.

y = 0
```
x * 0 <-> r <- 0
```

y = k
```
x * k <-> r <- x * k
```

y = k + 1
```
x * (k + 1) <-> r <- x * (k + 1)
```