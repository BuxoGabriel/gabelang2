# Gabelang
## Overview: Gabelang2
Gabelang2 is a toy programming language written in gabelang, which is also a toy programming language

## Overview

Gabelang2 is a programming language written in my programming language [Gabelang](https://github.com/buxogabriel/gabelang) for my programming languages class at Brooklyn College
Gabelang has 3 kinds of statements

1. Let statements: These are for assignment and initialization of variables
2. Reassignment statements: These are for reassigning initialized variables
3. Expression statements: These simply evaluate and print their result

## How To Run Gabelang2

### Prerequisites

Gabelang2 is written in the gabelang programming language and so the first step is to install gabelang as a prerequisite

Gabelang is written in rust and can be downloaded from cargo or built from source

#### From Cargo

1. Install cargo and the rust toolchain as as a dependency
2. Install gabelang through cargo

```sh
curl https://sh.rustup.rs -sSf | sh
cargo install gabelang
```

#### From Source

1. Install cargo and the rust tookchain as a dependency
2. Clone the [Gabelang](https://github.com/buxogabriel/gabelang) github repo
3. Build and Install from source using cargo

```sh
curl https://sh.rustup.rs -sSf | sh
git clone https://github.com/buxogabriel/gabelang
cd gabelang
cargo build
cargo install --path .
```

### Running Gabelang2

Once gabelang is installed you can run the gabelang 2 repl by

1. clone the [Gabelang2](https://github.com/buxogabriel/gabelang2) github repo
2. run gabelang2.gabe with gabelang
3. you should now have the gabelang2 repl running!

```sh
git clone https://github.com/buxogabriel/gabelang2
cd gabelang2
gabelang gabelang2.gabe
```

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
let x_2 = 0;

### Output 2
x_2 = 0
___

### Input 3
let x = 0
let y = x;
let z = ---(x+y);

### Output 3
0
___

### Input 4
let x = 1;
let y = 2;
let z = ---(x+y)*(x+-y);

### Output 4
x = 1
y = 2
z = 3
___

### Input 5
let x = 1;
let y = 2;
let z = x+y;
### Output 4
3
