---
title: "Mini Compiler for Python"
collection: projects
---

## Summary

A project aimed at implementing a mini compiler for the Python programming language supporting the different phases of a typical compiler, namely lexical analysis, syntax analysis, semantic analysis, intermediate code generation and intermediate code optimization. The mini compiler implemented as part of this project supports the if, if-else, if-elif-else and for constructs, arithmetic, relational and logical operators, keywords, identifiers and various other features along with error detection and error handling mechanisms. This project was implemented as part of the Compiler Design Course during my Undergraduate Study.

## Implementation Details

The implemented mini compiler supports the different phases of a typical compiler as follows:

* Lexical Analysis: The lexical analysis phase includes the tokenization of the input program to generate a sequence of valid tokens for the Python programming language. It involves the use of regular expressions to identify and map different tokens.
* Syntax Analysis: The generated tokens are then passed onto the syntax analysis phase where it is checked whether the generated stream of tokens conform to the grammar of Python. For this purpose, the project involved the creation of a custom context free grammar defining the different constructs and rules intended to be supported by the mini compiler for Python.
* Semantic Analysis: The semantic analysis phase checks whether the code is semantically correct. For example, it checks whether the data variables are used in a way consistent with their definition, if the data variables being used have been previously declared, if a keyword has been used as an identifier, etc.
* Intermediate Code Generation: This phase generates an intermediate representation of the source code. The intermediate code has been generated by associating attributes with the non terminals used in the grammar rules. The generated intermediate code is represented in the quadruple format with the operator, argument 1, argument 2 and result fields.
* Intermediate Code Optimization: This phase applies various optimizations to the generated intermediate code. The Constant folding, Constant Propagation, Common Subexpression Elimination and Strength Reduction optimizations have been implemented as part of this mini compiler.

With respect to the syntax and semantics of the Python programming language, the implemented mini compiler handles and supports the following in a comprehensive manner:
 * The different types of comments - single and multi-line comments
 * The if, if-else and if-elif-else conditional constructs and the for looping construct
 * Arithmetic operators, Relational operators, Logical operators including support for short circuit 'or' and 'and', assignment operator, punctuators and separators. Further, the precedence and associativity rules for all the operators have been taken care of as expected for Python
 * Different keywords and ensuring that keywords cannot be used as identifiers
 * The range functions with all its variations
 * The different scenarios of indentation using tabs and spaces. A stack has been used to handle indentation and to generate the required Indent and Dedent tokens accurately. Support has also been provided to take care of specific cases like generation of required number of Dedent tokens at the end of the file, generation of required number of Dedent tokens when there is a decrease in indentation but there is no set of spaces or tabs to match as such.
 * The variations with respect to the use of identifiers, numbers and strings
 * A separate symbol table for every scope is created and is used to store and retrieve records for identifiers and temporaries used in the generated intermediate code.

### Intermediate Code Optimization

The following intermediate code optimizations have been implemented as part of the mini compiler:
 * **Constant Folding**:
    * Expressions that can be evaluated at compile time because the arguments forming the expressions are constants, are evaluated and the resulting value is assigned to the appropriate variable.
    * Algebraic identities are also constant folded by this optimization. Algebraic identities are equations that are always true regardless of the value assigned to the variables.
    * Example for algebraic identity constant folding: a + 0 = 0 + a = a
 * **Constant Propagation**:
    * If the value of the variable is a constant that is known at compile time, this value is propagated and substituted whenever this variable is encountered.
    * This is usually followed by the constant folding optimization
 * **Common Subexpression Elimination**:
    * An occurrence of an expression E is called a common subexpression, if E is previously computed and the values constituting the expression E have not changed since the previous computation.
    * All such future occurrences of the expression can be eliminated as there is no need to recompute the value of the expression.
    * The Variables that are assigned to these future occurrences of the expression are assigned to the temporary that holds the value of the original expression E.
 * **Strength Reduction**:
    * Here, an expensive operation is replaced by a cheaper operation.
    * The cost being talked about here is with respect to the evaluation of the expression by the underlying hardware
    * Example:
        * a*2 => a<<1
        * a/2 => a>>1

### Error Handling

The following error detection and handling strategies have been implemented as part of the mini compiler:
 * If a keyword is used as an identifier, an error is prompted to the user.
 * If there is mismatch with respect to the indentation, an error is prompted to the user.
 * If the length of an identifier exceeds 79 characters, an error message prompting this is shown to the user and the identifier is truncated to the first 79 characters.
 * If an undeclared variable is used as part of an expression, a syntax error is thrown prompting the use of an undeclared variable.
 * If an invalid operator like the increment, decrement operator, etc is used as part of an expression, a syntax error is thrown.