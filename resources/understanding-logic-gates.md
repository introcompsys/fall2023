# Understanding Logic Gates

## What are logic gates?

Logic gates are used in digital circuits to preform logical functions in most electronics used today.

There are many types of logic gates, the four main gates we will look at are AND, OR, XOR, and NAND.

To understand how each one operates we can use truth tables to provide a better visual understanding.

Note: truth tables use 0's and 1's as input to get its output.

### AND Gate

AND gates use the logic of if input A and input B are both value 1 then the output is 1. So if either of input A or B are value 0 then the output is 0.

Truth Table:
| A | B | A AND B |
| --- | --- | :---: |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### OR Gate

OR gates use the logic of if input A or input B are value 1 then the output is 1. So if one of the inputs are 1 then the output; regardless of the other input, is also 1.

Truth Table:
| A | B | A OR B |
| --- | --- | :---: |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

### XOR Gate

XOR gates use the logic of if either input A or input B are value 1 then the output is 1 but if both are the same value then the output is 0. So if one of the inputs are a 1 then the output is 1, if both inputs are the same value then the output is 0.

Truth Table:
| A | B | A XOR B |
| --- | --- | :---: |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

### NAND Gate

NAND gates use the logic of if the inverse of input A has a value of 1 or if both input A and B are 0 then the output will be 1; otherwise, if the inverse of input A is 0 and input B is 1 then the output is 0.

Truth Table:
| A | B | A NAND B |
| --- | --- | :---: |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

## Some Practice to learn the logic operations better

A great way to understand and familiarize yourself with logic operators is to write functions for each logic gate in a program that take input A and B as parameters and return the output.

Here is an example of an AND gate program in python:

```{toggle}

def andgate(inputA, inputB) -> list:
    output = []
    for i in range(0,4):
        if(inputA[i] == 1 && inputB[i] == 1):
            output[i] == 1
        elif(inputA[i] != 1):
            output[i] == 0
    return output

```

## External resources

- [Online Logic Simulator](https://lodev.org/logicemu/)