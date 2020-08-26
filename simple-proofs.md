## Algorithms for x * y

The `"What"` is the product of two whole numbers:
**x * y**

It's mathematical definition:
```
x * y = 0 + x + x + x . . . for y instances of x 
                            and y is a whole number
```

The `"How"` is one of several algorithms for `x * y`:
```
r <- 0
Repeat y times, using an index i from 1 to y:
   r <- r + x

The result is the last value of r.
```

This one algorithm is obviously derived directly from the mathematical definition.  This algorithm is not efficient, but it is used as an example.  Later, we can prove a different algorithm for `x * y`.

To Prove: for all whole numbers in `x` and `y`, the algorithm computes the product `x * y`.
### Termination:
The algorithm repeats y times and terminates as described in line 2.

### Correctness (produces the expected result)

Does the algorithm produce the expected result, the `"What"`?

**By Induction**:

The **Invariant**, the truth: The property of the loop is itself the definition of `x * y` which is assumed to be true when the loop terminates at `i = y`.  Line 3 in the loop represents this truth as `r <- r + x`.  The property of this statement says, "the result is the addition of the previous result plus x", and it is expected to be the value of `x * y` for any value of y.  Since that is when the loop terminates, then the result is `x * y`.

Thus, the Invariant is a mathematical definition; and a propery of the loop.
``` 
mathematical property <-> Loop property
x * y <-> r <- r + x, after y repetitions
x * y <-> r, at the end of the loop
```

Base Case:
`x * y`: when y is `0`, 
```
x * y
x * 0
0
```

In the algorithm, when y is `0`:

* r is 0 in line 1
* when y is 0, line 3 is never executed (Repeat 0 times)
* the result r is 0

Thus:
```
0 <-> 0
```

Inductive Case: 

`x * y`: for y=k, 
assume `x * k` is true

In the algorithm: for y=k, 
assume `r <- x * k` is true

Prove that that the Loop Invariant is also true for `y = k + 1`

`x * y`: for y = k + 1,

```
x * y
x * (k + 1)
```

In the algorithm: for y = k + 1, 
the previous r was `x * k` when y was k
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