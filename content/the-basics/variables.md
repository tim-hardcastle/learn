# Variables

## Definition

A variable can hold a value. Variables are by default immutable to prevent from changing the value. If you want to change the value later you can declare the variable as mutable with `mut`.

The syntatic structure of a variable definition:
```ebnf
<name> ::= [a-zA-Z_][a-zA-Z0-9_]+
<expression> ::= <literal> | ...
<variable_declaration> ::= "let" "mut"? <name> (":" <typename>)? = <expression> ";"
```

Sample of a variable definition:

```back
let age = 42;
```

Backlang can automaticly deduce the type of the variable but if you want to specify the type, here is how:

```back
let name: string = "Bob";
```

You can also specify the type by a literal type specifier:

```back
let pi = 3.1451d;
```

A list of all basic primitive datatypes can be found [here](/#/learn/primitive-datatypes).

## Assignments

You can only assign mutable variables. If you try to change an immutable variable the compiler throws an error.

The syntactic structure of assignments:
```ebnf
<assignment> ::= <name> "=" <expression> ";"
```

A simple example:
```back
let mut day = "Monday";
day = "Tuesday";
```

## Exercises

1. Declare an immutable variable which stores the value of pi.
2. Try to reassign the value of this to `42`. 
    - Why is this not allowed?
    - How can you allow the reassignment of a variables value?
3. What is the difference between `char` and `string`?
