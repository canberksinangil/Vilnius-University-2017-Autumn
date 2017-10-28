# Coding Theory Homework

## Week 5 (Section 2.1 - 2.2)

### Exercise 2.1.1

>  Determine which of the following codes are linear.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

#### For (b) *C* = {000, 001, 010, 011}
`
* 001 + 010 = 010 ✔
* 001 + 011 = 010 ✔
* 010 + 011 = 001 ✔

It is linear code.
`
#### For (e) *C* = {00000, 11111}
`
It is linear code.
`
#### For (f) *C* = {00000, 11100, 00111, 11011}
`
* 11100 + 00111 = 11011 ✔
* 11100 + 11011 = 00111 ✔
* 00111 + 11011 = 11100 ✔

It is linear code.
`
#### For (g) *C* = {00000, 11110, 01111, 10001}
`
* 11110 + 01111 = 10001 ✔
* 11110 + 10001 = 01111 ✔
* 01111 + 10001 = 11110 ✔

It is linear code.
`
### Exercise 2.1.3

> Find the distance of each linear code in **Exercise 2.1.1**. Check answers with **Exercise 1.11.12**.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

> **Exercise 1.11.12**

> #### For (b) *C* = {000, 001, 010, 011};

> *d*(000, 001) = 1  
> *d*(000, 010) = 1  
> *d*(000, 011) = 2  
> *d*(001, 010) = 2  
> *d*(001, 011) = 1  
> *d*(010, 011) = 1  

> The distance for *C* is *d* = 1.

> #### For (e) *C* = {00000, 11111};

> *d*(00000, 11111) = 5  

> The distance for *C* is *d* = 5.

> #### For (f) *C* = {00000, 11100, 00111, 11011};

> *d*(00000, 11100) = 3  
> *d*(00000, 00111) = 3  
> *d*(00000, 11011) = 4  
> *d*(11100, 00111) = 4  
> *d*(11100, 11011) = 3  
> *d*(00111, 11011) = 3  

> The distance for *C* is *d* = 3.

> #### For (g) *C* = {00000, 11110, 01111, 10001};

> *d*(00000, 11110) = 4  
> *d*(00000, 01111) = 4  
> *d*(00000, 10001) = 2  
> *d*(11110, 01111) = 2  
> *d*(11110, 10001) = 4  
> *d*(01111, 10001) = 4  

> The distance for *C* is *d* = 2.

#### For (b) *C* = {000, 001, 010, 011};
```
*w*(001) = 1  
*w*(010) = 1  
*w*(011) = 2

The distance for *C* is *d* = 1.
```
#### For (e) *C* = {00000, 11111};
```
*w*(11111) = 5

The distance for *C* is *d* = 5.
```
#### For (f) *C* = {00000, 11100, 00111, 11011};
```
*w*(11100) = 3  
*w*(00111) = 3  
*w*(11011) = 4

The distance for *C* is *d* = 3.
```
#### For (g) *C* = {00000, 11110, 01111, 10001};
```
*w*(11110) = 4  
*w*(01111) = 4  
*w*(10001) = 2

The distance for *C* is *d* = 2.
```
### Exercise 2.1.4

> Prove that the distance of a linear code is the weight of the nonzero codeword of least weight.

### Exercise 2.2.3

> For each of the following sets *S*, list the elements of linear code for <*S*>.

> (a) *S* = {010, 011, 111}

> (b) *S* = {1010, 0101, 1111}

> (c) *S* = {0101, 1010, 1100}

> (f) *S* = {10101, 01010, 11111, 00011, 10110 }

#### For (a) *S* = {010, 011, 111}
```
000  
010  
011  
111  
010 + 011 = 001  
010 + 111 = 101  
011 + 111 = 100  
010 + 011 + 111 = 110  
```
#### For (b) *S* = {1010, 0101, 1111}
```
0000  
1010  
0101  
1111  
1010 + 0101 = 1111  
1010 + 1111 = 0101  
0101 + 1111 = 1010  
1010 + 0101 + 1111 = 0000  
```
#### For (c) *S* = {0101, 1010, 1100}
```
0000  
0101  
1010  
1100  
0101 + 1010 = 1111  
0101 + 1100 = 1001  
1010 + 1100 = 0110  
0101 + 1010 + 1100 = 0011  
```
#### For (f) *S* = {10101, 01010, 11111, 00011, 10110 }

### Exercise 2.2.4 (a is a scalar, i.e. 0 or 1)
```
> Construct examples in *K*<sup>5</sup> of each of the following rules

> (a)  *u* · (*v* + *w*) = *u* · *v* + *u* · *w*

> (b) *a*(*v* · *w*) = (*av*) · *w* = *v* · (*aw*).
```
### Exercise 2.2.5

> Prove that the two rules in **Exercise 2.2.4** hold in *K*<sup>*n*</sup>.

### Exercise 2.2.7

> Find the dual code *C*<sup>⊥</sup> for each codes *C* =< *S* >. in **Exercise 2.2.3**. 

> (a) *S* = {010, 011, 111}

> (b) *S* = {1010, 0101, 1111}

> (c) *S* = {0101, 1010, 1100}

> (f) *S* = {10101, 01010, 11111, 00011, 10110 }


### Exercise 2.2.8

> Find an example of a nonzero word *v* such that *v* . *v* = 0. What can you say about the weight of such word?
