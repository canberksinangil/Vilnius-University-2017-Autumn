# Coding Theory Homework

## Week 3 (Section 1.9 - 1.10)

### Exercise 1.9.5

> |*M*| = 2, *n* = 3, and *C* = {001, 101}. If *v* = 001 is sent, when will **IMLD** conclude this correctly, and when will **IMLD** incorrectly conclude that 101 was sent?

2<sup>3</sup> = 8 maximum different possibilities.

![Formula](https://github.com/devcan/Vilnius-University-2017-Autumn/blob/master/Coding-Theory/Images/decoding.sec.1.9.2.jpg)

**' * ' shows less weight.**

| Order | Received *w* | 001 + *w* | 101 + *w* | Decode *v* |
| ----- | ------------ | --------- | --------- | ---------- |
| 1.    | 000          | 001*      | 101       | 001        |
| 2.    | 100          | 101       | 001*      | 101        |
| 3.    | 010          | 011*      | 111       | 001        |
| 4.    | 001          | 000*      | 100       | 001        |
| 5.    | 110          | 111       | 011*      | 101        |
| 6.    | 101          | 100       | 000*      | 101        |
| 7.    | 011          | 010*      | 110       | 001        |
| 8.    | 111          | 110       | 010*      | 101        |

### Exercise 1.9.6

> Let |*M*| = 3 and *n* = 3. For each word *w* in *K*<sup>3</sup> that could be received, find the word *v* in de code *C* = {000, 001, 110} which **IMLD** will conclude was sent.

2<sup>3</sup> = 8 maximum different possibilities.

**' * ' shows less weight.**

**' ** ' shows at least one more same weight.**

**' !!! ' shows we need to request retransmission.**

| Order | Received *w* | 000 + *w* | 001 + *w* | 110 + *w* | Decode *v* |
| ----- | ------------ | --------- | --------- | --------- | ---------- |
| 1.    | 000          | 000*      | 001       | 110       | 000        |
| 2.    | 100          | 100**     | 101       | 010**     | !!!        |
| 3.    | 010          | 010**     | 011       | 100**     | !!!        |
| 4.    | 001          | 001       | 000*      | 111       | 001        |
| 5.    | 110          | 110       | 111       | 000*      | 110        |
| 6.    | 101          | 101       | 100*      | 011       | 001        |
| 7.    | 011          | 011       | 010*      | 101       | 001        |
| 8.    | 111          | 111       | 110       | 001*      | 110        |


### Exercise 1.9.7

> Construct the IMLD table for each of the following codes.

> (b) *C* = {000, 001, 010, 011}

|*M*| = 4 

*n* = 3      

*C* = {000, 001, 010, 011}

| Order | Received *w* | 000 + *w* | 001 + *w* | 010 + *w* | 011 + *w* | Decode *v* |
| ----- | ------------ | --------- | --------- | --------- | --------- | ---------- |
| 1.    | 000          | 000*      | 001       | 010       | 011       | 000        |
| 2.    | 100          | 100*      | 101       | 110       | 111       | 000        |
| 3.    | 010          | 010       | 011       | 000*      | 001       | 010        |
| 4.    | 001          | 001       | 000*      | 011       | 010       | 001        |
| 5.    | 110          | 110       | 111       | 100*      | 101       | 010        |
| 6.    | 101          | 101       | 100*      | 111       | 110       | 001        |
| 7.    | 011          | 011       | 010       | 001       | 000*      | 011        |
| 8.    | 111          | 111       | 110       | 101       | 100*      | 011        |

### Exercise 1.10.2

> Suppose *p* = .90, |*M*| = 2, *n* = 3, *C* = {001, 101}, as in Exercise 1.9.5.

> (b) If *v* = 101 is sent, find the probability that **IMLD** will correctly conclude this after one transmission.

### Exercise 1.10.4

> Suppose *p* = .90 and *C* = {000, 001, 110}, as in Exercise 1.9.6. If *v* = 110 is sent, find the probability that IMLD will correctly conclude this, and the probability that IMLD will incorrectly conclude that 000 was sent.


### Exercise 1.10.5

> For each of the following codes *C* calculate *Φ*<sub>*p*</sub>(*C*, *v*) for each *v* in *C* using *p* = .90. (The **IMLD** tables for these codes were constructed in Exercise 1.9.7).

> (b) *C* = {000, 001, 010, 011}
