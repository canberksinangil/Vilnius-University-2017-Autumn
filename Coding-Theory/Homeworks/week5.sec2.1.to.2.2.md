# Coding Theory Homework

## Week 5 (Section 2.1 - 2.2)

### Exercise 2.1.1

>  Determine which of the following codes are linear.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

#### For (b) *C* = {000, 001, 010, 011}

* 001 + 010 = 010 ✔
* 001 + 011 = 010 ✔
* 010 + 011 = 001 ✔

It is linear code.

#### For (e) *C* = {00000, 11111}

It is linear code.

#### For (f) *C* = {00000, 11100, 00111, 11011}

* 11100 + 00111 = 11011 ✔
* 11100 + 11011 = 00111 ✔
* 00111 + 11011 = 11100 ✔

It is linear code.

#### For (g) *C* = {00000, 11110, 01111, 10001}

* 11110 + 01111 = 10001 ✔
* 11110 + 10001 = 01111 ✔
* 01111 + 10001 = 11110 ✔

It is linear code.

### Exercise 2.1.3

> Find the distance of each linear code in **Exercise 2.1.1**. Check answers with Exercise **1.11.12**.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

### Exercise 2.1.4

> Prove that the distance of a linear code is the weight of the nonzero codeword of least weight.

### Exercise 2.2.3

> For each of the following sets *S*, list the elements of linear code for <*S*>.

> (a) *S* = {010, 011, 111}

> (b) *S* = {1010, 0101, 1111}

> (c) *S* = {0101, 1010, 1100}

> (f) *S* = {10101, 01010, 11111, 00011, 10110 }

### Exercise 2.2.4 (a is a scalar, i.e. 0 or 1)

> Construct examples in *K*<sup>s</sup> of each of the following rules

> (a)  *u* · (*v* + *w*) = *u* · *v* + *u* · *w*

> (b) *a*(*v* · *w*) = (*av*) · *w* = *v* · (*aw*).

### Exercise 2.2.5

> Prove that the two rules in **Exercise 2.2.4* hold in *K*<sup>*n*</sup>.

### Exercise 2.2.7

> Find the dual code *C*<sup>⊥</sup> for each codes *C* =< *S* >. in **Exercise 2.2.3. 

> (a) *S* = {010, 011, 111}

> (b) *S* = {1010, 0101, 1111}

> (c) *S* = {0101, 1010, 1100}

> (f) *S* = {10101, 01010, 11111, 00011, 10110 }


### Exercise 2.2.8

> Find an example of a nonzero word *v* such that *v* . *v* = 0. What can you say about the weight of such word?
