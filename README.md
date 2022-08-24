# CHEMIT
#### Description: Chemit is an interpreted language inspired from the BASIC programming language which first appeared in 1964.

The interpreter is written in Python 3 and it currently can be used as an Interactive Prompt to evaluate expressions in real-time or to evaluate external files written in Chemit.

## Working with chemit
By executing the interpreter file (shell.py) you will be presented with this interface in the command line:
```

Chemit>

```
You can evaluate expressions by writing them after `Chemit>`:
```

Chemit> 1 + 2 + 3
6
Chemit> PRINT("hello world!")
hello world!
0
```

### Evaluating external files
It's possible to load external files written in Chemit by calling the RUN function inside the interpreter interface.
```
chemit> RUN("test.myopl")
Hello
0
```

## Basic chemit functionalities

### Working with mathematics expressions
Chemit supports the order of operations in mathematics.
The order of operations, which is used throughout mathematics, science, technology, and many computer programming languages, is expressed here:
<br>
1. exponentiation and root extraction
2. multiplication and division
3. addition and subtraction
<br>
This means that if, in a mathematical expression, a subexpression appears between two operators, the operator that is higher in the above list should be applied first.

```

chemit> 1 + 2 * 3
7
chemit> (1 + 2) * 3
9
chemit> 2^3 + 1
9

```
Note that the `^` operator is the power operator in chemit.

### Variables
You can make variables and assign them any value using the `VAR` keyword.

```
chemit> VAR a = 1
1
chemit> VAR b = 2.2
2.2
chemit> VAR b = "string"
"string"
```

### Comparison operators
Chemit also supports different comparison operators: equals, not equals, less than, greater than, etc.
Also, it supports the logical operators: AND, OR and NOT.

```
chemit> 1 > 0
1
chemit> 2 < -2
0
chemit> 2 != 2
0
chemit> 2 == 2
1
chemit> 1 OR 0
1
chemit> 1 AND 0
0
chemit> NOT 1
0
chemit> NOT 0
1

```
### If statements
You can also use if statements in chemit using the following syntax:
```
chemit > IF(1 > 0) THEN PRINT("Hello")
Hello
0

```
Note that if the expression inside of the if statement evaluates to true then the expression after the `THEN` keyword will be executed, and you can also use the `ELSE` keyword to execute another expression if the expression inside the if statement is evaluated to false or 0.
```
chemit > IF(1 < 0) THEN PRINT("Hello") ELSE PRINT("Oops")
Oops
0

```
You can also use else-if statements.

```
chemit > IF(1 < 0) THEN PRINT("Hello") ELSE IF(1 > 0) THEN PRINT("Oops")
Oops
0

```

### FOR and WHILE statements
You can use the FOR and WHILE statements for looping in chemit:
```

chemit > FOR i = 5 TO 10 STEP 1 THEN PRINT("Hello")
Hello
Hello
Hello
Hello
Hello
[0, 0, 0, 0, 0]

chemit> WHILE TRUE THEN PRINT("Oops infinite loop")
infinite loop
....

```

### Functions
In chemit you can define functions using the `FUN` keyword.

```

chemit > FUN test(a) -> a + 1
<function test>
chemit > test(1)
2

```

