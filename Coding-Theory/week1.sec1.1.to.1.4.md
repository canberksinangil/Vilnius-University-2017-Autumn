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

*C* = {00, 10, 01 ,11}.

Before the answer let's calculate number of possibilities. We have '4' different options to select each time and for 6 length we have to choose 3 times which means 4x4x4= 64 maximum different possibilities.


| Order | First  | Second | Third | Structure |
| ----- | ------ | ------ | ----- | --------- |
| 1.    | 00     | 00     | 00    | x - x - x |
| 2.    | 10     | 10     | 10    | x - x - x |
| 3.    | 01     | 01     | 01    | x - x - x |
| 4.    | 11     | 11     | 11    | x - x - x |
| 5.    | 00     | 00     | 10    | x - x - y |
| 6.    | 00     | 00     | 01    | x - x - y |
| 7.    | 00     | 00     | 11    | x - x - y |
| 8.    | 10     | 10     | 00    | x - x - y |
| 9.    | 10     | 10     | 01    | x - x - y |
| 10.   | 10     | 10     | 11    | x - x - y |
| 11.   | 01     | 01     | 00    | x - x - y |
| 12.   | 01     | 01     | 10    | x - x - y |
| 13.   | 01     | 01     | 11    | x - x - y |
| 14.   | 11     | 11     | 00    | x - x - y |
| 15.   | 11     | 11     | 10    | x - x - y |
| 16.   | 11     | 11     | 01    | x - x - y |
| 17.   | 00     | 10     | 10    | x - y - y |
| 18.   | 00     | 01     | 01    | x - y - y |
| 19.   | 00     | 11     | 11    | x - y - y |
| 20.   | 10     | 00     | 00    | x - y - y |
| 21.   | 10     | 01     | 01    | x - y - y |
| 22.   | 10     | 11     | 11    | x - y - y |
| 23.   | 01     | 00     | 00    | x - y - y |
| 24.   | 01     | 10     | 10    | x - y - y |
| 25.   | 01     | 11     | 11    | x - y - y |
| 26.   | 11     | 00     | 00    | x - y - y |
| 27.   | 11     | 10     | 10    | x - y - y |
| 28.   | 11     | 01     | 01    | x - y - y |
| 29.   | 00     | 10     | 00    | x - y - x |
| 30.   | 00     | 01     | 00    | x - y - x |
| 31.   | 00     | 11     | 00    | x - y - x |
| 32.   | 10     | 00     | 10    | x - y - x |
| 33.   | 10     | 01     | 10    | x - y - x |
| 34.   | 10     | 11     | 10    | x - y - x |
| 35.   | 01     | 00     | 01    | x - y - x |
| 36.   | 01     | 10     | 01    | x - y - x |
| 37.   | 01     | 11     | 01    | x - y - x |
| 38.   | 11     | 00     | 11    | x - y - x |
| 39.   | 11     | 10     | 11    | x - y - x |
| 40.   | 11     | 01     | 11    | x - y - x |
| 41.   | 00     | 10     | 01    | x - y - z |
| 42.   | 00     | 01     | 10    | x - y - z |
| 43.   | 00     | 10     | 11    | x - y - z |
| 44.   | 00     | 11     | 10    | x - y - z |
| 45.   | 00     | 01     | 11    | x - y - z |
| 46.   | 00     | 11     | 01    | x - y - z |
| 47.   | 10     | 00     | 01    | x - y - z |
| 48.   | 10     | 01     | 00    | x - y - z |
| 49.   | 10     | 00     | 11    | x - y - z |
| 50.   | 10     | 11     | 00    | x - y - z |
| 51.   | 10     | 01     | 11    | x - y - z |
| 52.   | 10     | 11     | 01    | x - y - z |
| 53.   | 01     | 00     | 10    | x - y - z |
| 54.   | 01     | 10     | 00    | x - y - z |
| 55.   | 01     | 10     | 11    | x - y - z |
| 56.   | 01     | 11     | 10    | x - y - z |
| 57.   | 01     | 00     | 11    | x - y - z |
| 58.   | 01     | 11     | 00    | x - y - z |
| 59.   | 11     | 00     | 10    | x - y - z |
| 60.   | 11     | 10     | 00    | x - y - z |
| 61.   | 11     | 10     | 01    | x - y - z |
| 62.   | 11     | 01     | 10    | x - y - z |
| 63.   | 11     | 00     | 01    | x - y - z |
| 64.   | 11     | 01     | 00    | x - y - z |
