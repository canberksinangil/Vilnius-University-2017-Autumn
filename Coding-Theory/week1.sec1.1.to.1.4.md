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

> Short Way: Imagine that you have got 2 keys and you have got 6 boxes and you want to put these keys into the boxes. My question is how many **different** ways can you put the keys into the boxes?

> You can use combinations C(6 , 2).

#### Case 3

'4' quantity for 1 = 6! / 4!x2! = 15

#### Case 4

'6' quantity for 1 = 6! / 6! = 1

If we sum all cases 1 +15 +15 +1 = 32 maximum different cases.

| Order | Case 1   | Case 2   | Case 3   | Case 4   |
| ----- | -------- | -------- | -------- | -------- |
| 1.    | 000000   |          |          |          |
| 2.    |          | 000011   |          |          |
| 3.    |          | 001100   |          |          |
| 4.    |          | 110000   |          |          |
| 5.    |          | 000110   |          |          |
| 6.    |          | 011000   |          |          |
| 7.    |          | 000101   |          |          |
| 8.    |          | 001001   |          |          |
| 9.    |          | 010001   |          |          |
| 10.   |          | 100001   |          |          |
| 11.   |          | 101000   |          |          |
| 12.   |          | 100100   |          |          |
| 13.   |          | 100010   |          |          |
| 14.   |          | 010100   |          |          |
| 15.   |          | 001010   |          |          |
| 16.   |          | 010010   |          |          |
| 17.   |          |          | 111100    |          |
| 18.   |          |          | 001111    |          |
| 19.   |          |          | 011110    |          |
| 20.   |          |          | 110011    |          |
| 21.   |          |          | 110110    |          |
| 22.   |          |          | 110101    |          |
| 23.   |          |          | 011011    |          |
| 24.   |          |          | 111001    |          |
| 25.   |          |          | 111010    |          |
| 26.   |          |          | 011101    |          |
| 27.   |          |          | 100111    |          |
| 28.   |          |          | 101110    |          |
| 29.   |          |          | 101011    |          |
| 30.   |          |          | 101101    |          |
| 31.   |          |          | 010111    |          |
| 32.   |          |          |           | 111111   |

### Exercise 1.2.4

> Explain why a channel with *p* = 0 is uninteresting.

If every time encoder (transmitter) transmits 0, decoder (receiver) receives 0 and vice versa which means our channel is %100 reliable and makes probability of channel equals to '1' (***p* = 1**). There is no need to change any digits.

One the other hand If every time encoder (transmitter) transmits 1, decoder (receiver) receives 0 and vice versa which means our channel is %100 **unreliable** and makes probability of channel equals to '0' (***p* = 0**). There is need to change every digit. For instance, encoder sent 1 but decoder received 0 and we have already known channel with ***p* = 0**. Every digit is changed by decoder.

To sum up, there is no importance when channel is with ***p* = 0** or ***p* = 1**.

### Exercise 1.2.5

> Explain how to convert a channel is with 0 < *p* <= 1/2 into a channel with 1/2 <= *p* < 1.

We replace each '0' with a '1' and each '1' with '0'.

Let's explain why we replace?

If a channel is with *p* <= 1/2, %50 or more digits is received wrong.

How we can handle with this?

If we change every digit, the channel becomes with 1/2 <= *p*.

In conclusion, when we change every digit, they change as %50 or more correct and the channel becomes with 1/2 <= *p* < 1.

### Exercise 1.2.6

> What can be said about a channel with *p*=1/2?

*p*=1/2 means there is %50 chance to receive correct or %50 incorrect.


### Exercise 1.3.4

> Let *C* be the code of all words legth 3. Determine which codeword was most likely sent if 001 is recived.

### Exercise 1.3.5

> Add a parity check digit to the codewords in the code **Exercise 1.3.4**, and use the resulting code *C* to answer the following  questions.

  (a) If 1101 is received can we detect an eror?
  
  (b) If 1101 is received what codewords were most likely to have been trasmitted?
  
  (c) Is any word of legth 4 that is nott in the code, cloeset to a unique codeword?

### Exercise 1.3.6

> Repea each codewoord in the code *C* defined in **Exercise 1.3.4** three times to form a repetition code of length 9. Find the closest codewords to the following recieved words:

  (a) 001000001
  
  (b) 011001011
  
  (c) 101000101
  
  (d) 100000010
 
### Exercise 1.3.7
 
> Find the maximum number of length *n* = 4 in a code in which any single error can be detected.
 
### Exercise 1.3.8
 
> Repeat **Exercise 1.3.7** for *n* = 5, *n* = 6 and for general *n*.

### Exercise 1.3.8

> Find the information rate for each of the codes in **Exercise 1.3.4, Exercise 1.3.5, Exercise 1.3.6**.
  
