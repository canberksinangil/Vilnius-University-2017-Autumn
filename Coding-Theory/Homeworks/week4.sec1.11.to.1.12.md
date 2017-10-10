# Coding Theory Homework

## Week 4 (Section 1.11 - 1.12)

### Exercise 1.11.2

> Let *C* = {001, 101, 110}. Determine whether *C* will detect the error patterns

> (a) 011

> (b) 001

> (c) 000.

**' * ' shows same codewords in *C*.**

For 011;

| Order | Codewords *v* | Error Pattern *u* | *v* + *u* |
| ----- | --------------| ----------------- | --------- |
| 1.    |  001          |  011              | 010       |
| 2.    |  101          |  011              | 110*      |
| 3.    |  110          |  011              | 101*      |

We cannot detect any error pattern. Because at least one of these sums in *C*.

For 001;

| Order | Codewords *v* | Error Pattern *u* | *v* + *u* |
| ----- | ------------- | ----------------- | --------- |
| 1.    |  001          |  001              | 000       |
| 2.    |  101          |  001              | 100       |
| 3.    |  110          |  001              | 111       |

None of these sums in *C* so we can detect error pattern. Error pattern is *u* = 001.

For 000;

| Order | Codewords *v* | Error Pattern *u* | *v* + *u* |
| ----- | ------------- | ----------------- | --------- |
| 1.    |  001          |  000              | 001*      |
| 2.    |  101          |  000              | 101*      |
| 3.    |  110          |  000              | 110*      |

We cannot detect any error pattern. Because at least one of these sums in *C*.

### Exercise 1.11.4

> Which eror patterns will the code *C* = *K*<sup>*n*</sup> detect?

We cannot detect any error pattern. Because at least one of these sums have to be in *C*.

### Exercise 1.11.5

> (i) Let *C* be a code contains the zero word as a codeword. Prove that if the eror pattern *u* is a codeword, then *C* will not detect *u*.

> (ii) Prove that n code will detect the zero eror pattern *u* = 0.

We cannot detect any error pattern. Because all of these sums will be same as the codeword itself. (CCC + 000 = CCC)

### Exercise 1.11.7

> Determine the eror patterns detected by each code in **Exercise 1.9.7** by using the **IMLD** tables constructed there

> ### Exercise 1.9.7

> Construct the IMLD table for each of the following codes.

> (b) *C* = {000, 001, 010, 011}

|*M*| = 4 

*n* = 3      

*C* = {000, 001, 010, 011}

| Order | Received *w* | 000 + *w* | 001 + *w* | 010 + *w* | 011 + *w* | Decode *v* |
| ----- | ------------ | --------- | --------- | --------- | --------- | ---------- |
| 1.    | 000          | 000       | 001       | 010       | 011       | 000        |
| 2.    | 100*         | 100       | 101       | 110       | 111       | 000        |
| 3.    | 010          | 010       | 011       | 000       | 001       | 010        |
| 4.    | 001          | 001       | 000       | 011       | 010       | 001        |
| 5.    | 110*         | 110       | 111       | 100       | 101       | 010        |
| 6.    | 101*         | 101       | 100       | 111       | 110       | 001        |
| 7.    | 011          | 011       | 010       | 001       | 000       | 011        |
| 8.    | 111*         | 111       | 110       | 101       | 100       | 011        |

*u* = {100, 110, 101, 111}.

### Exercise 1.11.10

> Find the eror patterns detected by each following codes and compare your answers with those **Exercise 1.11.7**.

> (b) *C* = {000, 001, 010, 011}

### Exercise 1.11.12

> Find the distance of each of following codes.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

#### For (b) *C* = {000, 001, 010, 011};

*d*(000, 001) = 1  
*d*(000, 010) = 1  
*d*(000, 011) = 2  
*d*(001, 010) = 2  
*d*(001, 011) = 1  
*d*(010, 011) = 1  

The distance for *C* is *d* = 1.

#### For (e) *C* = {00000, 11111};

*d*(00000, 11111) = 5  

The distance for *C* is *d* = 5.

#### For (f) *C* = {00000, 11100, 00111, 11011};

*d*(00000, 11110) = 4  
*d*(00000, 01111) = 4  
*d*(00000, 11011) = 4  
*d*(11110, 01111) = 2  
*d*(11110, 11011) = 2  
*d*(01111, 11011) = 2  

The distance for *C* is *d* = 4.

#### For (g) *C* = {00000, 11110, 01111, 10001};

*d*(00000, 11110) = 4  
*d*(00000, 01111) = 4  
*d*(00000, 10001) = 2  
*d*(11110, 01111) = 2  
*d*(11110, 10001) = 4  
*d*(01111, 10001) = 4  

The distance for *C* is *d* = 4.

### Exercise 1.11.13

> Find the distance of code formed by adding a parity check digit to *K*<sup>*n*</sup>.

### Exercise 1.11.19

> For each code in *C* in **Exercise 1.11.12** find the eror patterns which **Theorem 1.11.14** guarantees *C* will detect.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

### Exercise 1.11.20

> Let *C* be the code consisting of all words of length 4 which have even weight. Find the error pattern *C* detects.

### Exercise 1.12.5

> Let *C* = {001, 101, 110}. Does *C* correct the error pattern *u* = 010? What about *u* = 000?

### Exercise 1.12.7

> Prove that the zero error pattern is always corrected.

### Exercise 1.12.8

> Which error patterns will the code *C* = *K*<sup>*n*</sup> correct?

### Exercise  1.12.12

> For each following codes *C*

> (i) determine the error patterns that *C* will correct (the **IMLD** tables for these codes were constructed in **Exercise 1.9.7**), and

> (b) *C* = {000, 001, 010, 011}

> (ii) find the error patterns that **Theorem 1.12.9** guarantees that *C* corrects.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}

> ### Exercise 1.9.7

> Construct the IMLD table for each of the following codes.

> (b) *C* = {000, 001, 010, 011}

### Exercise 1.12.14

> For each code in **Exercise 1.12.12**, find an error pattern of weight [(*d* - 1) / 2] + 1 that *C* does not correct.

> (b) *C* = {000, 001, 010, 011}

> (e) *C* = {00000, 11111}

> (f) *C* = {00000, 11100, 00111, 11011}

> (g) *C* = {00000, 11110, 01111, 10001}
