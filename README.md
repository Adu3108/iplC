# Compiler for C-like Language

This repository contains the project done as a part of the course CS 302 : Implementation of Programming Languages at IIT Bombay in Spring 2023.

## Problem Statement

This project aims to build a compiler for a subset of C programs. This is accomplished in 3 phases :-

### 1. Scanner and Parser

   In this phase, we build a scanner and a parser that outputs a parse tree for the input program on the basis of a context-free grammar. We have used [Flex](https://github.com/westes/flex), a fast lexical analyzer generator and [Bison](https://www.gnu.org/software/bison/), a general-purpose parser generator. These softwares can be installed using [homebrew](https://brew.sh).

   ```bash
   brew install flex
   brew install bison
   ```

   Scanner is constructed by writing a **Flex** script to detect tokens in the input program. Thereafter, we convert the given context-free grammar into a bison script and add actions to the bison script which aid in the construction of parse tree . Finally, this parse tree is visualized using the [graphviz tool](https://graphviz.org).

### 2. Symbol Table Creation, Abstract Syntax Tree Construction and Semantic Checks

   This phase is divided into 3 subtasks :-

   - **Symbol Table Creation** : In this task, we store the information contained in the declarations such as types, sizes and offsets of variables as well as types of functions in a structure called Symbol Table.

   - **Semantic Checks** : In this task, we perform various checks such as scope checking, type checking and overloading resolution to ensure that the input program is semantically correct.

   - **Abstract Syntax Tree** : In this task, we construct the Abstract Syntax Tree for a syntactically and semantically correct program.

### 3. Code Generator

   In this phase, we generate 32-bit x86 code with the help of the Abstract Syntax Tree and Symbol Table constructed in the previous phrase. In order to generate efficient x86 code, we employ the **Sethi-Ullman Algorithm**.

## References

[Bison Manual](https://www.gnu.org/software/bison/manual/bison.pdf)

[Flex Manual](https://people.iith.ac.in/ramakrishna/Compilers-Aug14/doc/flex.pdf)

[x86 Manual](https://docs.oracle.com/cd/E19641-01/802-1948/802-1948.pdf)
