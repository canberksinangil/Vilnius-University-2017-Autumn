# Coding Theory Homework

## Week 2 (Section 1.5 - 1.8)

### Exercise 1.6.2

> Calculate *ϕ*<sub>*.97*</sub>(*v*, *w*) for each fo the following pairs of *v* and *w*:

> (b) *v* = 1110101, *w* = 1110101

> (e) *v* = 1011010, *w* = 0000010

> (g) *v* = 111101, *w* = 000010.

Our formula is:

***ϕ*<sub>*p*</sub>(*v*, *w*) = *p*<sup>*n-d*</sup>(1-*p*)<sup>*d*</sup>**

  * *p* = Reliability (probability of incorret digits).
  * *v* = Transmitted.
  * *w* = Received.
  * *n* = Length.
  * *d* = Positions (incorret digits).

According to the formula let's calculate for each codewords.

For (b);

*ϕ*<sub>*.97*</sub>(1110101, 1110101)

  * *p* = 0.97
  * *v* = 1110101
  * *w* = 1110101
  * *n* = 7
  * *d* = 0 (There is no inncorret digits rececived).

*ϕ*<sub>*.97*</sub>(1110101, 1110101)= *p*<sup>7</sup>

(0.97)<sup>7</sup> = 0.80798284478113


For (e);

*ϕ*<sub>*.97*</sub>(1011010, 0000010)

For (g);

*ϕ*<sub>*.97*</sub>(111101, 000010)

### Exercise 1.6.9

> Which of the codewords 110110, 110101, 000111, 1000111, 101000 is most likely to have been sent if *w* = 011001 is received.

### Exercise 1.6.10

> In Theorem 1.6.3 we assume that 1/2 < p < 1. What would change in the statement of Theorem 1.6.3 if we replace the assumption with 

> (a) 0 < p < 1/2,

> (b) p = 1/2?

### Exercise 1.7.1

> Show that if *v* is a word in *K<sup>n</sup>* then *v* + *v* = 0.

### Exercise 1.7.2

> Show that if *v* and *w* are words in *K<sup>n</sup>* and *v* + *w* = 0 then *v* = *w*.

### Exercise 1.7.3

> Show that if *u*, *v* and *w* are words in *K<sup>n</sup>* and *u* + *v* = *w* then *u* + *w* = *v*.

### Exercise 1.8.1

> Compute the weight of each of the following words, and the distance between each pair of them: *v<sub>1</sub>* = 1001010, *v<sub>2</sub>* = 0110101, *v<sub>3</sub>* = 0011110, and *v<sub>4</sub>* = *v<sub>2</sub>* + *v<sub>3</sub>*.

### Exercise 1.8.2

> Let *u* = 01011, *v* = 11010, *w* = 01100. Compare each of the following pairs in quantities.

> (a) *wt*(*v* + *w*), and *wt*(*v*) + *wt*(*w*),

> (b) *d*(*v*,*w*), and *d*(*v*,*u*) + *d*(*u*,*w*).

### Exercise 1.8.3

> 1. 0 <= *wt*(*v*) <= *n*
> 2. *wt*(0) = 0
> 3. If *wt*(*v*) = 0, then *v* = 0.
> 4. 0 <= *d*(*v*,*w*) <= *n*.
> 5. *d*(*v*,*v*) = 0
> 6. If *d*(*v*,*w*) = 0, then *v* = *w*.
> 7. *d*(*v*,*w*) = *d*(*w*, *v*)
> 8. *wt*(*v* + *w*) <= *wt*(*v*) + *wt*(*w*)
> 9. *d*(*v*, *w*) <= *d*(*v*, *u*) + *d*(*u*, *w*)
> 10. *wt*(*av*) = *a* * *wt*(*v*)
> 11. *d*(*av*,*aw*) = *a* * *d*(*v*,*w*).

> Construct an example *K<sup>5</sup>* of each of the eleven rules above.

### Exercise 1.8.4

> 8. *wt*(*v* + *w*) <= *wt*(*v*) + *wt*(*w*)
> 9. *d*(*v*, *w*) <= *d*(*v*, *u*) + *d*(*u*, *w*)
> 10. *wt*(*av*) = *a* * *wt*(*v*)
> 11. *d*(*av*,*aw*) = *a* * *d*(*v*,*w*).

> Prove each of the four rules above.
