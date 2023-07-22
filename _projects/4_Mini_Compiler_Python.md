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
* Intermediate Code Generation: This phase generates an intermediate representation of the source code. This mini compiler, specifically generates and represents the intermediate code in the quadruple format with the operator, argument 1, argument 2 and result fields.
* Intermediate Code Optimization: This phase applies various optimizations to the generated intermediate code. This mini compiler, specifically supports the Constant folding, Constant Propagation, Common Subexpression Elimination and Strength Reduction optimizations.

The implemented mini compiler handles and supports the following, with respect to the syntax and semantics of the Python programming language:
 * The different types of comments - single and multi-line comments have been handled comprehensively
 * 
