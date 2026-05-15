## Overview: Gabelang2
Gabelang2 is a toy programming language written in gabelang, which is also a toy programming language

## Toy Language Grammer

Program:
	Assignment*

Assignment:
	Identifier = Exp;
    let Identifier = Exp;

Exp: 
	Exp + Term | Exp - Term | Term

Term:
	Term * Fact  | Fact

Fact:
	( Exp ) | - Fact | + Fact | Literal | Identifier

Identifier:
     	Letter [Letter | Digit]*

Letter:
	a|...|z|A|...|Z|_

Literal:
	0 | NonZeroDigit Digit*
		
NonZeroDigit:
	1|...|9

Digit:
	0|1|...|9

## Example Inputs and Outputs

### Input 1
x = 001;

### Output 1
error
___

### Input 2
x_2 = 0;

### Output 2
x_2 = 0
___

### Input 3
x = 0
y = x;
z = ---(x+y);

### Output 3
error
___

### Input 4
let x = 1;
y = 2;
z = ---(x+y)*(x+-y);

### Output 4
x = 1
y = 2
z = 3
___

### Input 5
let x = 1;
y = 2;
let z = x+ y;
### Output 4
error, normal variables in let expression

