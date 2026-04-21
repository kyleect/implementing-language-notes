# Glossary

## AST

An abstract syntax tree is a structure ([parse tree](#parse-tree)) that represents a simplified version of a program's source code. Comments would usually be excluded in an AST.

https://en.wikipedia.org/wiki/Abstract_syntax_tree

## Backpatching

In [compiler](#compiler) and [interpreter](#interpreter) implementations, backpatching refers to modifying the control flow graph or other data structures after the program has been compiled or interpreted.

https://stackoverflow.com/questions/15984671/what-does-backpatching-mean

## Backtracking

https://en.wikipedia.org/wiki/Backtracking

## Bytecode

https://en.wikipedia.org/wiki/Bytecode

## Comments

Comments is text in the source code ignored by the [compiler](#compiler) or [interpreter](#interpreter).

## Compiler

A compiler is a program that translates high-level representation in to another lower level representation. This can be machine code or [byte code](#byte-code).

### Multi Pass Compiler

A multi pass compiler will process source code in multiple steps. This allows for user defined identifers like functions to be used before their declared, as oposed to [single pass compilers](#single-pass-compiler).

https://en.wikipedia.org/wiki/Multi-pass_compiler

### Single Pass Compiler

A single pass compiler will generally combine the lexing/parsing/compiling in to a single step. This was originally done because earlier computers didn't have the memory to store something like an [AST](#ast).

This comes with the trade offs: All user defined identifiers must be forward declared before use

https://en.wikipedia.org/wiki/One-pass_compiler

## Compiler Errors

Compiler [errors](#error) happen at compile time and are typically reported by the [compiler](#compiler). They indicate that there are issues with the program that prevent it from being compiled.

## Concrete Syntax Tree

A concrete syntax tree is a structure ([parse tree](#parse-tree)) that represents the entirety of the original source code, [comments](#comments) included.

## Context-Free grammar

https://en.wikipedia.org/wiki/Context-free_grammar

## Context-sensitive grammar

https://en.wikipedia.org/wiki/Context-sensitive_grammar

## Deterministic context-free grammar

https://en.wikipedia.org/wiki/Deterministic_context-free_grammar

## Deterministic context-free language

https://en.wikipedia.org/wiki/Deterministic_context-free_language

## Error

An unexpected behavior in the programs behavior. This can either be non-fatal (can be handled by the program) or fatal (program terminates/the error wasn't handled).

- [Syntactical](#syntactical-errors)
- [Compiler](#compiler-errors)
- [Runtime](#runtime-errors)

## Expression

An expression is a piece of code that generates a value. Expressions can be composed together.

- `1 + 1`
- `a`
- `multiply(1, 2)`

https://en.wikipedia.org/wiki/Expression_(computer_science)

## Formal grammar

https://en.wikipedia.org/wiki/Formal_grammar

## Formal language

https://en.wikipedia.org/wiki/Formal_language

## Grammar

A language grammar is a formal description of the syntax of a programming language. This can be abstract or codified.

### [BNF](https://en.wikipedia.org/wiki/Backus%E2%80%93Naur_form)

```bnf
<postal-address> ::= <name-part> <street-address> <zip-part>

      <name-part> ::= <personal-part> <last-name> <opt-suffix-part> <EOL> | <personal-part> <name-part>

  <personal-part> ::= <first-name> | <initial> "."

 <street-address> ::= <house-num> <street-name> <opt-apt-num> <EOL>

       <zip-part> ::= <town-name> "," <state-code> <ZIP-code> <EOL>

<opt-suffix-part> ::= "Sr." | "Jr." | <roman-numeral> | ""
    <opt-apt-num> ::= "Apt" <apt-num> | ""
```

### [EBNF](https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form)

```ebnf
digit excluding zero = "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9" ;
digit                = "0" | digit excluding zero ;
```

## Identifiers

https://en.wikipedia.org/wiki/Identifier_(computer_languages)

## Interpreter

In computing, an interpreter is software that executes source code without first compiling it to machine code.

https://en.wikipedia.org/wiki/Interpreter_(computing)

## Keywords

https://en.wikipedia.org/wiki/Reserved_word

## Language Server Protocol

The Language Server Protocol (LSP) is a JSON-RPC-based protocol for use between editors or IDEs and servers that provide: code completion, syntax highlighting and marking of warnings and errors, as well as refactoring routines.

https://microsoft.github.io/language-server-protocol/
https://en.wikipedia.org/wiki/Language_Server_Protocol

## Lexer

A lexer is responsible for breaking down the input source code into [tokens](#tokens).

https://en.wikipedia.org/wiki/Lexical_analysis

## LL Grammar

In formal language theory, an LL grammar is a [context-free grammar](#context-free-grammar) that can be parsed by an [LL parser](#ll-parser), which parses the input from Left to right, and constructs a Leftmost derivation of the sentence (hence LL, compared with [LR parser](#lr-parser) that constructs a rightmost derivation). A language that has an [LL grammar](#ll-grammar) is known as an LL language. These form subsets of deterministic context-free grammars ([DCFGs](#deterministic-context-free-grammar)) and deterministic context-free languages ([DCFLs](#deterministic-context-free-language)), respectively. One says that a given grammar or language "is an LL grammar/language" or simply "is LL" to indicate that it is in this class.

LL parsers are table-based parsers, similar to LR parsers. LL grammars can alternatively be characterized as precisely those that can be parsed by a predictive parser – a recursive descent parser without backtracking – and these can be readily written by hand. This article is about the formal properties of LL grammars; for parsing, see LL parser or recursive descent parser.

## LL Parser

LL [parser](#parser) is a top-down parser for a restricted [context-free language](#context-free-grammar). It parses the input from Left to right, performing Leftmost derivation of the sentence.

An LL parser is called an LL(k) parser if it uses k tokens of lookahead when parsing a sentence. A grammar is called an LL(k) grammar if an LL(k) parser can be constructed from it.

A formal language is called an LL(k) language if it has an LL(k) grammar. The set of LL(k) languages is properly contained in that of LL(k+1) languages, for each k ≥ 0.[1] A corollary of this is that not all context-free languages can be recognized by an LL(k) parser.

https://en.wikipedia.org/wiki/LL_grammar

## LR Parser

| Invented By  |
| ------------ |
| Donald Knuth |

| Invented In |
| ----------- |
| 1968        |

https://en.wikipedia.org/wiki/LR_parser

## LALR

| Invented By                |
| -------------------------- |
| Frank DeRemer/Tom Pennello |

| Invented In |
| ----------- |
| 1969/1979   |

Generally, the LALR [parser](#parser) refers to the LALR(1) parser, just as the [LR parser](#lr-parser) generally refers to the LR(1) parser The "(1)" denotes one-[token](#tokens) lookahead, to resolve differences between rule patterns during parsing.

Similarly, there is an LALR(2) parser with two-token lookahead, and LALR(k) parsers with k-token lookup, but these are rare in actual use.

https://en.wikipedia.org/wiki/LALR_parser

## Lexeme

https://en.wikipedia.org/wiki/Lexical_analysis#Disambiguation_of_%22lexeme%22

## Literals

TODO

## Operators

TODO

## Parser

A parser transforms a collection of [tokens](#tokens) in to an [AST](#ast) or [CST](#concrete-syntax-tree).

https://en.wikipedia.org/wiki/Parsing#Parser

## Parse Tree

https://en.wikipedia.org/wiki/Parse_tree

## Parsing Precedence

https://en.wikipedia.org/wiki/Operator-precedence_parser

## Pratt Parser

https://en.wikipedia.org/wiki/Operator-precedence_parser#Pratt_parsing

## Predicate

https://en.wikipedia.org/wiki/Predicate_(logic)

## Production Rules

https://en.wikipedia.org/wiki/Production_(computer_science)

## Quantifier

https://en.wikipedia.org/wiki/Quantifier_(logic)

## Recursive descent parser

https://en.wikipedia.org/wiki/Recursive_descent_parser

## Runtime Errors

Runtime [errors](#error) happen during the programs execution and are typically errors that weren't/couldn't be caught at lexing/parsing/compile time.

## Shift Reduce Parser

https://en.wikipedia.org/wiki/Shift-reduce_parser

## Spans

Spans represent a position within a given piece of text. This can be represented in various forms: line/column, start/end, start/length.

## Statement

An statement is a piece of code that does not generate a value but does generate a side effect. Statements include declarations (variables, functions, structs, enums), expression statements, control flow statements, etc.

https://en.wikipedia.org/wiki/Statement_(computer_science)

### Declaration Statement

A declaration statement declares/defines something e.g. variable, function.

```typescript
function noop() {}

const PI = 3;
```

### Expression Statement

An expression statement is an expression that's then consumed by a statement delimiter e.g. semicolon.

```typescript
1 + 1; // Produces no value
```

### Control Flow Statement

```typescript
if ("Hello".length > 2) {
  //...
} else {
  //...
}
```

## Syntactical Errors

Syntax [errors](#error) occur when the input source code fails to comply to language rules during the [lexing](#lexer) or [parsing](#parser) process.

## Terminal and nonterminal symbols

https://en.wikipedia.org/wiki/Terminal_and_nonterminal_symbols

## Tokens

Tokens are the smallest meaningfully defined units in a programming language, such as [keywords](#keywords), [identifiers](#identifiers), [operators](#operators), and [literals](#literals).

https://en.wikipedia.org/wiki/Lexical_analysis

### Token Position Information

Lexers can record a token's position (see [span](#spans)) in the original source code, which is useful for generating error message and debugging.

## Type

A type denotes what kind a value is. e.g. string, number, boolean, object in a [type system](#type-system).

## Type Checker

A typechecker verifies all that all the [types](#type) of a program and it's inputs are correct in a [type system](#type-system).

## Type Error

A type [error](#error) denotes a value violates a program or a language's typing rules during [typechecking](#type-checker).

## Type Inference

Type inference is the detection of a variable/function return/function parameter's [type](#type) without adding a type in the source code. The type is determined by it's use e.g. what value is being assigned, what operation is being performed (`a + 1` means `a` is a number), what argument is passed.

## Type System

https://en.wikipedia.org/wiki/Type_system

## Universal quantification

**∀**

See: [Type Systems](#type-system)

https://en.wikipedia.org/wiki/Universal_quantification
https://gist.github.com/kyleect/7f0580432d738bc61e78e69ac2e7a9ac
