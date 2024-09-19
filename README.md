# KEMET
#### Description: Kemet is an interpreted language inspired from the BASIC programming language which first appeared in 1964.

The interpreter is written in Python 3 and it currently can be used as an Interactive Prompt to evaluate expressions in real-time or to evaluate external files written in Kemet.

## Working with kemet
By executing the interpreter file (shell.py) you will be presented with this interface in the command line:
```

Kemet>

```
You can evaluate expressions by writing them after `Kemet>`:
```

Kemet> 1 + 2 + 3
6
Kemet> PRINT("hello world!")
hello world!
0
```

### Evaluating external files
It's possible to load external files written in Kemet by calling the RUN function inside the interpreter interface.
```
kemet> RUN("test.myopl")
Hello
0
```

## Basic kemet functionalities

### Working with mathematics expressions
Kemet supports the order of operations in mathematics.
The order of operations, which is used throughout mathematics, science, technology, and many computer programming languages, is expressed here:
<br>
1. exponentiation and root extraction
2. multiplication and division
3. addition and subtraction
<br>
This means that if, in a mathematical expression, a subexpression appears between two operators, the operator that is higher in the above list should be applied first.

```

kemet> 1 + 2 * 3
7
kemet> (1 + 2) * 3
9
kemet> 2^3 + 1
9

```
Note that the `^` operator is the power operator in kemet.

### Variables
You can make variables and assign them any value using the `VAR` keyword.

```
kemet> VAR a = 1
1
kemet> VAR b = 2.2
2.2
kemet> VAR b = "string"
"string"
```

### Comparison operators
Kemet also supports different comparison operators: equals, not equals, less than, greater than, etc.
Also, it supports the logical operators: AND, OR and NOT.

```
kemet> 1 > 0
1
kemet> 2 < -2
0
kemet> 2 != 2
0
kemet> 2 == 2
1
kemet> 1 OR 0
1
kemet> 1 AND 0
0
kemet> NOT 1
0
kemet> NOT 0
1

```
### If statements
You can also use if statements in kemet using the following syntax:
```
kemet > IF(1 > 0) THEN PRINT("Hello")
Hello
0

```
Note that if the expression inside of the if statement evaluates to true then the expression after the `THEN` keyword will be executed, and you can also use the `ELSE` keyword to execute another expression if the expression inside the if statement is evaluated to false or 0.
```
kemet > IF(1 < 0) THEN PRINT("Hello") ELSE PRINT("Oops")
Oops
0

```
You can also use else-if statements.

```
kemet > IF(1 < 0) THEN PRINT("Hello") ELSE IF(1 > 0) THEN PRINT("Oops")
Oops
0

```

### FOR and WHILE statements
You can use the FOR and WHILE statements for looping in kemet:
```

kemet > FOR i = 5 TO 10 STEP 1 THEN PRINT("Hello")
Hello
Hello
Hello
Hello
Hello
[0, 0, 0, 0, 0]

kemet> WHILE TRUE THEN PRINT("Oops infinite loop")
infinite loop
....

```

### Functions
In kemet you can define functions using the `FUN` keyword.

```

kemet > FUN test(a) -> a + 1
<function test>
kemet > test(1)
2

```

