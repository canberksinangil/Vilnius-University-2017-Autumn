# Coding Theory Homework

## Week 1 (Section 1.1 - 1.4)

### Exercise 1.2.1

> List all words of length 3; of length 4; of length 5.

We have two options first one is '0' second one is '1' in that case we can calculate our all possibilities like 2^n.

According to the exercises 

* 2 ^ 3 = 8	 	maximum different possibilities. 
* 2 ^ 4 = 16	maximum different possibilities.
* 2 ^ 5 = 32	maximum different possibilities.

| Order | Length 3 | Length 4 | Length 5 |
| ----- | -------- | -------- | -------- |
| 1.    | 000      | 0000     |00000     |
| 2.    | 001      | 0001     | 00001    |
| 3.    | 010      | 0010     | 00010    |
| 4.    | 011      | 0011     | 00011    |
| 5.    | 100      | 0100     | 00100    |
| 6.    | 101      | 0101     | 00101    |
| 7.    | 110      | 0110     | 00110    |
| 8.    | 111      | 0111     | 00111    |
| 9.    |          | 1000     | 01000    |
| 10.   |          | 1001     | 01001    |
| 11.   |          | 1010     | 01010    |
| 12.   |          | 1011     | 01011    |
| 13.   |          | 1100     | 01100    |
| 14.   |          | 1101     | 01101    |
| 15.   |          | 1110     | 01110    |
| 16.   |          | 1111     | 01111    |
| 17.   |          |          | 10000    |
| 18.   |          |          | 10001    |
| 19.   |          |          | 10010    |
| 20.   |          |          | 10011    |
| 21.   |          |          | 10100    |
| 22.   |          |          | 10101    |
| 23.   |          |          | 10110    |
| 24.   |          |          | 10111    |
| 25.   |          |          | 11000    |
| 26.   |          |          | 11001    |
| 27.   |          |          | 11010    |
| 28.   |          |          | 11011    |
| 29.   |          |          | 11100    |
| 30.   |          |          | 11101    |
| 31.   |          |          | 11110    |
| 32.   |          |          | 11111    |

### Exercise 1.2.2

> Find a formula for the total number of words of length *n*.

2 ^ n

### Exercise 1.2.3

> Let *C* be the code consisting of all words of length 6 having an even number of ones. List the codewords in *C*.

First of all we have a condition, codewords must have even quantity of '1'. Which means quantity of '1' can be 0, 2, 4 or 6. According to the condition let's calculate possibilities.

#### Case 1

'0' quantity for 1 = 6! / 6! = 1

#### Case 2

'2' quantity for 1 = 6! / 2!x4! = 15

>Short way: Imagine that you have got 2 keys and you have got 6 boxes and you want to put these keys into the boxes. My question is how many **different** ways you can put the keys into the boxes?

>You can use combinations C(6 , 2)

#### Case 3

'4' quantity for 1 = 6! / 4!x2! = 15

#### Case 4

'6' quantity for 1 = 6! / 6! = 1



