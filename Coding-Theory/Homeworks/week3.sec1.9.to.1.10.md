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


| Order | Received *w* | 001 + *w* | 101 + *w* | Decode *v* |
| ----- | ------------ | --------- | --------- | ---------- |
| 1.    | 000          | 001*      | 101       | 001        |
| 2.    | **100**      | 101       | 001*      | **101**    |
| 3.    | 010          | 011*      | 111       | 001        |
| 4.    | 001          | 000*      | 100       | 001        |
| 5.    | **110**      | 111       | 011*      | **101**    |
| 6.    | **101**      | 100       | 000*      | **101**    |
| 7.    | 011          | 010*      | 110       | 001        |
| 8.    | **111**      | 110       | 010*      | **101**    |

*L*(101) = {100, 110, 101, 111}

#### ***ϕ*<sub>*p*</sub>(*v*, *w*) = *p*<sup>*n-d*</sup>(1-*p*)<sup>*d*</sup>**

  * *p* = Reliability (probability of incorrect digits).
  * *v* = Transmitted.
  * *w* = Received.
  * *n* = Length.
  * *d* = Number of disagreement in *w* (incorrect digits).
  
#### ***Φ*<sub>*p*</sub>(*C*, *v*) = Σ<sub>*w∈L*(*v*)</sub>*Φ*<sub>*p*</sub>(*v*, *w*)**

*Φ*<sub>*p*</sub>(*C*, 101) = *Φ*<sub>*p*</sub>(101, 100) + *Φ*<sub>*p*</sub>(101, 110) + *Φ*<sub>*p*</sub>(101, 101) + *Φ*<sub>*p*</sub>(101, 111)

*n* = 3

> *Φ*<sub>*p*</sub>(101, 100) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

> *Φ*<sub>*p*</sub>(101, 110) = *p*<sup>1</sup>(1-*p*)<sup>2</sup>

> *Φ*<sub>*p*</sub>(101, 101) = *p*<sup>3</sup>(1-*p*)<sup>0</sup>

> *Φ*<sub>*p*</sub>(101, 111) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 101) = *p*<sup>2</sup>(1-*p*) + *p*(1-*p*)<sup>2</sup> + *p*<sup>3</sup> + *p*<sup>2</sup>(1-*p*)

*Φ*<sub>*p*</sub>(*C*, 101) = *p*<sup>3</sup> + 2*p*<sup>2</sup>(1-*p*) + *p*(1-*p*)<sup>2</sup>

*Φ*<sub>*p*</sub>(*C*, 101) = 0.90<sup>3</sup> + 2 * 0.90<sup>2</sup>(1 - 0.90) + 0.90(1 - 0.90)<sup>2</sup>

*Φ*<sub>*p*</sub>(*C*, 101) = 0.729 + 0.162 + 0.009

*Φ*<sub>*p*</sub>(*C*, 101) = 0.9 (assuming *p* = 0.90)

### Exercise 1.10.4

> Suppose *p* = .90 and *C* = {000, 001, 110}, as in Exercise 1.9.6. If *v* = 110 is sent, find the probability that IMLD will correctly conclude this, and the probability that IMLD will incorrectly conclude that 000 was sent.

| Order | Received *w* | 000 + *w* | 001 + *w* | 110 + *w* | Decode *v* |
| ----- | ------------ | --------- | --------- | --------- | ---------- |
| 1.    | 000          | 000*      | 001       | 110       | 000        |
| 2.    | 100          | 100**     | 101       | 010**     | !!!        |
| 3.    | 010          | 010**     | 011       | 100**     | !!!        |
| 4.    | 001          | 001       | 000*      | 111       | 001        |
| 5.    | **110**      | 110       | 111       | 000*      | **110**    |
| 6.    | 101          | 101       | 100*      | 011       | 001        |
| 7.    | 011          | 011       | 010*      | 101       | 001        |
| 8.    | **111**      | 111       | 110       | 001*      | **110**    |

#### ***ϕ*<sub>*p*</sub>(*v*, *w*) = *p*<sup>*n-d*</sup>(1-*p*)<sup>*d*</sup>**

#### ***Φ*<sub>*p*</sub>(*C*, *v*) = Σ<sub>*w∈L*(*v*)</sub>*Φ*<sub>*p*</sub>(*v*, *w*)**

*L*(110) = {110, 111}

*Φ*<sub>*p*</sub>(*C*, 110) = *Φ*<sub>*p*</sub>(110, 110) + *Φ*<sub>*p*</sub>(110, 111) 

> *Φ*<sub>*p*</sub>(110, 110) = *p*<sup>3</sup>(1-*p*)<sup>0</sup>

> *Φ*<sub>*p*</sub>(110, 111) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 110) = *p*<sup>3</sup>(1-*p*)<sup>0</sup> + *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 110) = *p*<sup>3</sup> + *p*<sup>2</sup>(1-*p*)

*Φ*<sub>*p*</sub>(*C*, 110) = 0.90<sup>3</sup> + 0.90<sup>2</sup>(1 - 0.90)

*Φ*<sub>*p*</sub>(*C*, 110) = 0.729 + 0.081

*Φ*<sub>*p*</sub>(*C*, 110) = 0.81 (assuming *p* = 0.90)

To decode 000 only 000 can be received.

> *Φ*<sub>*p*</sub>(110, 000) = *p*<sup>1</sup>(1-*p*)<sup>2</sup>

*Φ*<sub>*p*</sub>(*C*, 000) = *p*(1-*p*)<sup>2</sup>

*Φ*<sub>*p*</sub>(*C*, 000) = 0.90(1 - 0.90)<sup>2</sup>

*Φ*<sub>*p*</sub>(*C*, 000) = 0.009 (assuming *p* = 0.90)

### Exercise 1.10.5

> For each of the following codes *C* calculate *Φ*<sub>*p*</sub>(*C*, *v*) for each *v* in *C* using *p* = .90. (The **IMLD** tables for these codes were constructed in Exercise 1.9.7).

> (b) *C* = {000, 001, 010, 011}

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

#### ***ϕ*<sub>*p*</sub>(*v*, *w*) = *p*<sup>*n-d*</sup>(1-*p*)<sup>*d*</sup>**

#### ***Φ*<sub>*p*</sub>(*C*, *v*) = Σ<sub>*w∈L*(*v*)</sub>*Φ*<sub>*p*</sub>(*v*, *w*)**

#### *L*(000) = {000, 100}

*Φ*<sub>*p*</sub>(*C*, 000) = *Φ*<sub>*p*</sub>(000, 000) + *Φ*<sub>*p*</sub>(000, 100) 

> *Φ*<sub>*p*</sub>(000, 000) = *p*<sup>3</sup>(1-*p*)<sup>0</sup>

> *Φ*<sub>*p*</sub>(000, 100) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 000) = *p*<sup>3</sup>(1-*p*)<sup>0</sup> + *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 000) = *p*<sup>3</sup> + *p*<sup>2</sup>(1-*p*)

*Φ*<sub>*p*</sub>(*C*, 000) = 0.90<sup>3</sup> + 0.90<sup>2</sup>(1 - 0.90)

*Φ*<sub>*p*</sub>(*C*, 000) = 0.729 + 0.081

*Φ*<sub>*p*</sub>(*C*, 000) = 0.81 (assuming *p* = 0.90)


#### *L*(001) = {001, 101}

*Φ*<sub>*p*</sub>(*C*, 001) = *Φ*<sub>*p*</sub>(001, 001) + *Φ*<sub>*p*</sub>(001, 101)

> *Φ*<sub>*p*</sub>(001, 001) = *p*<sup>3</sup>(1-*p*)<sup>0</sup>

> *Φ*<sub>*p*</sub>(001, 101) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 001) = *p*<sup>3</sup>(1-*p*)<sup>0</sup> + *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 001) = *p*<sup>3</sup> + *p*<sup>2</sup>(1-*p*)

*Φ*<sub>*p*</sub>(*C*, 001) = 0.90<sup>3</sup> + 0.90<sup>2</sup>(1 - 0.90)

*Φ*<sub>*p*</sub>(*C*, 001) = 0.729 + 0.081

*Φ*<sub>*p*</sub>(*C*, 001) = 0.81 (assuming *p* = 0.90)

#### *L*(010) = {010, 110}

*Φ*<sub>*p*</sub>(*C*, 010) = *Φ*<sub>*p*</sub>(010, 010) + *Φ*<sub>*p*</sub>(010, 110)

> *Φ*<sub>*p*</sub>(010, 010) = *p*<sup>3</sup>(1-*p*)<sup>0</sup>

> *Φ*<sub>*p*</sub>(010, 110) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 010) = *p*<sup>3</sup>(1-*p*)<sup>0</sup> + *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 010) = *p*<sup>3</sup> + *p*<sup>2</sup>(1-*p*)

*Φ*<sub>*p*</sub>(*C*, 010) = 0.90<sup>3</sup> + 0.90<sup>2</sup>(1 - 0.90)

*Φ*<sub>*p*</sub>(*C*, 010) = 0.729 + 0.081

*Φ*<sub>*p*</sub>(*C*, 010) = 0.81 (assuming *p* = 0.90)


#### *L*(011) = {011, 111}

*Φ*<sub>*p*</sub>(*C*, 011) = *Φ*<sub>*p*</sub>(011, 011) + *Φ*<sub>*p*</sub>(011, 111)

> *Φ*<sub>*p*</sub>(011, 011) = *p*<sup>3</sup>(1-*p*)<sup>0</sup>

> *Φ*<sub>*p*</sub>(011, 111) = *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 011) = *p*<sup>3</sup>(1-*p*)<sup>0</sup> + *p*<sup>2</sup>(1-*p*)<sup>1</sup>

*Φ*<sub>*p*</sub>(*C*, 011) = *p*<sup>3</sup> + *p*<sup>2</sup>(1-*p*)

*Φ*<sub>*p*</sub>(*C*, 011) = 0.90<sup>3</sup> + 0.90<sup>2</sup>(1 - 0.90)

*Φ*<sub>*p*</sub>(*C*, 011) = 0.729 + 0.081

*Φ*<sub>*p*</sub>(*C*, 011) = 0.81 (assuming *p* = 0.90)
