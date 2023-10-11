# Compiler for C-like Language

This repository contains the project done as a part of the course CS 302 : Implementation of Programming Languages at IIT Bombay in Spring 2023.

## Problem Statement

This project aims to build a compiler for a subset of C programs. This is accomplished in 3 phases :-

1. **Scanner and Parser**

   In this phase, we build a scanner and a parser that outputs an Abstract Syntax Tree for the input program on the basis of a context-free grammar. We have used [Flex](https://github.com/westes/flex), a fast lexical analyzer generator and [Bison](https://www.gnu.org/software/bison/), a general-purpose parser generator. These softwares can be installed using [homebrew](https://brew.sh).

   ```bash
   brew install flex
   brew install bison
   ```

   Scanner is constructed by writing a **Flex** script to detect tokens in the input program. Thereafter, we convert the given context-free grammar into a bison script and add actions to the bison script which aid in the construction of Abstract Syntax Tree. Finally, this AST is visualized using the [graphviz tool](https://graphviz.org).
