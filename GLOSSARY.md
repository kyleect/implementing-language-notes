# Glossary

## Attribution

Portions of this content are derived from Wikipedia (CC BY-SA 4.0).

## Algebraic data type

https://en.wikipedia.org/wiki/Algebraic_data_type

## AST

> An abstract syntax tree (AST) is a data structure used in computer science to represent the structure of a program or code snippet. It is a tree representation of the abstract syntactic structure of text (often source code) written in a formal language. Each node of the tree denotes a construct occurring in the text. It is sometimes called just a syntax tree.
>
> Source: Wikipedia contributors, “Abstract syntax tree”, https://en.wikipedia.org/wiki/Abstract_syntax_tree, CC BY-SA 4.0. Unmodified.

An abstract syntax tree is a structure ([parse tree](#parse-tree)) that represents a simplified version of a program's source code. Comments would usually be excluded in an AST.

## Backpatching

In [compiler](#compiler) and [interpreter](#interpreter) implementations, backpatching refers to modifying the control flow graph or other data structures after the program has been compiled or interpreted.

https://stackoverflow.com/questions/15984671/what-does-backpatching-mean

## Backtracking

> Backtracking is a class of algorithms for finding solutions to some computational problems, notably constraint satisfaction or enumeration problems, that incrementally builds candidates to the solutions, and abandons a candidate ("backtracks") as soon as it determines that the candidate cannot possibly be completed to a valid solution.
>
> Source: Wikipedia contributors, “Backtracking”, https://en.wikipedia.org/wiki/Backtracking, CC BY-SA 4.0. Unmodified.

## Bytecode

> Bytecode (also called portable code or p-code) is an intermediate representation form of an instruction set designed for efficient execution by a software interpreter. Unlike human-readable[1] source code, bytecodes are compact numeric codes, constants, and references (normally numeric addresses) that encode the result of compiler parsing and performing semantic analysis of things like type, scope, and nesting depths of program objects.
>
> Source: Wikipedia contributors, “Bytecode”, https://en.wikipedia.org/wiki/Bytecode, CC BY-SA 4.0. Unmodified.

## Code Formatting

> Pretty-printing (or prettyprinting) is the application of any of various stylistic formatting conventions to text files, such as source code, markup, and similar kinds of content. These formatting conventions may entail adhering to an indentation style, using different color and typeface to highlight syntactic elements of source code, or adjusting size, to make the content easier for people to read, and understand. Pretty-printers for source code are sometimes called code formatters or beautifiers.
>
> Source: Wikipedia contributors, “Pretty Printing”, https://en.wikipedia.org/wiki/Pretty-printing, CC BY-SA 4.0. Unmodified.

Code formatting transforms input source in to formatted output source code.

## Comments

Comments is text in the source code ignored by the [compiler](#compiler) or [interpreter](#interpreter).

## Compiler

> In computing, a compiler is software that translates computer code written in one programming language (the source language) into another language (the target language). The name "compiler" is primarily used for programs that translate source code from a high-level programming language to a low-level programming language (e.g. assembly language, object code, or machine code) to create an executable program.
>
> Source: Wikipedia contributors, “Compiler”, https://en.wikipedia.org/wiki/Compiler, CC BY-SA 4.0. Unmodified.

A compiler is a program that translates high-level representation in to another lower level representation. This can be machine code or [byte code](#byte-code).

### Multi Pass Compiler

> A multi-pass compiler is a type of compiler that processes the source code or abstract syntax tree of a program several times. This is in contrast to a one-pass compiler, which traverses the program only once. Each pass takes the result of the previous pass as the input, and creates an intermediate output. In this way, the (intermediate) code is improved pass by pass, until the final pass produces the final code.
>
> Source: Wikipedia contributors, “Multi-pass Compiler”, https://en.wikipedia.org/wiki/Multi-pass_compiler, CC BY-SA 4.0. Unmodified.

A multi pass compiler will process source code in multiple steps. This allows for user defined identifers like functions to be used before their declared, as oposed to [single pass compilers](#single-pass-compiler).

### Single Pass Compiler

> In computer programming, a one-pass compiler is a compiler that processes each compilation unit only once, sequentially translating each source statement or declaration into something close to its final machine code. This is in contrast to a multi-pass compiler which converts the program into one or more intermediate representations in steps between source code and machine code, and which reprocesses the entire compilation unit in each sequential pass.
>
> Source: Wikipedia contributors, “One-pass compiler”, https://en.wikipedia.org/wiki/One-pass_compiler, CC BY-SA 4.0. Unmodified.

A single pass compiler will generally combine the lexing/parsing/compiling in to a single step. This was originally done because earlier computers didn't have the memory to store something like an [AST](#ast).

This comes with the trade offs: All user defined identifiers must be forward declared before use

## Compiler Errors

Compiler [errors](#error) happen at compile time and are typically reported by the [compiler](#compiler). They indicate that there are issues with the program that prevent it from being compiled.

## Composite data type

> In computer science, a composite data type or compound data type is a data type that consists of programming language scalar data types and other composite types that may be heterogeneous and hierarchical in nature. It is sometimes called a structure or a record or by a language-specific keyword used to define one such as struct. It falls into the aggregate type classification which includes homogenous collections such as the array and list.
>
> Source: Wikipedia contributors, “Composite data type”, https://en.wikipedia.org/wiki/Composite_data_type, CC BY-SA 4.0. Unmodified.

## Concrete Syntax Tree

See: [parse tree](#parse-tree)

## Context-Free grammar

> In formal language theory, a context-free grammar (CFG) is a formal grammar whose production rules can be applied to a nonterminal symbol regardless of its context. In particular, in a context-free grammar, each production rule is of the form
>
> ${\displaystyle A\ \to \ \alpha }$
>
> with ${\displaystyle A}$ a single nonterminal symbol, and ${\displaystyle \alpha }$ a string of terminals and/or nonterminals (${\displaystyle \alpha }$ can be empty). Regardless of which symbols surround it, the single nonterminal ${\displaystyle A}$ on the left hand side can always be replaced by ${\displaystyle \alpha }$ on the right hand side.
>
> Source: Wikipedia contributors, “Context-free grammar”, https://en.wikipedia.org/wiki/Context-free_grammar, CC BY-SA 4.0. Unmodified.

## Context-sensitive grammar

> A context-sensitive grammar (CSG) is a formal grammar in which the left-hand sides and right-hand sides of any production rules may be surrounded by a context of terminal and nonterminal symbols. Context-sensitive grammars are more general than context-free grammars, in the sense that there are languages that can be described by a CSG but not by a context-free grammar. Context-sensitive grammars are less general (in the same sense) than unrestricted grammars. Thus, CSGs are positioned between context-free and unrestricted grammars in the Chomsky hierarchy.
>
> Source: Wikipedia contributors, “Context-sensitive grammar”, https://en.wikipedia.org/wiki/Context-sensitive_grammar, CC BY-SA 4.0. Unmodified.

## Deterministic context-free grammar

> In formal grammar theory, the deterministic context-free grammars (DCFGs) are a proper subset of the context-free grammars. They are the subset of context-free grammars that can be derived from deterministic pushdown automata, and they generate the deterministic context-free languages. DCFGs are always unambiguous, and are an important subclass of unambiguous CFGs; there are non-deterministic unambiguous CFGs, however.
>
> DCFGs are of great practical interest, as they can be parsed in linear time and in fact a parser can be automatically generated from the grammar by a parser generator. They are thus widely used throughout computer science. Various restricted forms of DCFGs can be parsed by simpler, less resource-intensive parsers, and thus are often used. These grammar classes are referred to by the type of parser that parses them, and important examples are LALR, SLR, and LL.
>
> Source: Wikipedia contributors, “Deterministic context-free grammar”, https://en.wikipedia.org/wiki/Deterministic_context-free_grammar, CC BY-SA 4.0. Unmodified.

## Deterministic context-free language

> In formal language theory, deterministic context-free languages (DCFL) are a proper subset of context-free languages. They are context-free languages that can be accepted by a deterministic pushdown automaton. DCFLs are always unambiguous, meaning that they admit an unambiguous grammar. There are non-deterministic unambiguous CFLs, so DCFLs form a proper subset of unambiguous CFLs.
>
> DCFLs are of great practical interest, as they can be parsed in linear time, and various restricted forms of DCFGs admit simple practical parsers. They are thus widely used throughout computer science.
>
> Source: Wikipedia contributors, “Deterministic context-free language”, https://en.wikipedia.org/wiki/Deterministic_context-free_language, CC BY-SA 4.0. Unmodified.

## Effect System

> In computing, an effect system is a formal system that describes the computational effects of computer programs, such as side effects. An effect system can be used to provide a compile-time check of the possible effects of the program.
>
> The effect system extends the notion of type to have an "effect" component, which comprises an effect kind and a region. The effect kind describes what is being done, and the region describes with what (parameters) it is being done.
>
> Source: Wikipedia contributors, “Effect system”, https://en.wikipedia.org/wiki/Effect_system, CC BY-SA 4.0. Unmodified.

## Error

An unexpected behavior in the programs behavior. This can either be non-fatal (can be handled by the program) or fatal (program terminates/the error wasn't handled).

- [Syntactical](#syntactical-errors)
- [Compiler](#compiler-errors)
- [Runtime](#runtime-errors)

## Expression

> In computer science, an expression is a syntactic entity in a programming language that may be evaluated to determine its value of a specific semantic type. It is a combination of one or more constants, variables, functions, and operators that the programming language interprets (according to its particular rules of precedence and of association) and computes to produce ("to return", in a stateful environment) another value. In simple settings, the resulting value is usually one of various primitive types, such as string, boolean, or numerical (such as integer, floating-point, or complex).
>
> Source: Wikipedia contributors, “Expression (computer science)”, https://en.wikipedia.org/wiki/Expression_(computer_science), CC BY-SA 4.0. Unmodified.

An expression is a piece of code that generates a value. Expressions can be composed together.

- `1 + 1`
- `a`
- `multiply(1, 2)`

## Flow Typing

> In programming language theory, flow-sensitive typing (also called flow typing or occurrence typing) is a type system where the type of an expression depends on its position in the control flow.
>
> Source: Wikipedia contributors, “Flow-sensitive typing”, https://en.wikipedia.org/wiki/Flow-sensitive_typing, CC BY-SA 4.0. Unmodified.

## Formal grammar

> A formal grammar is a set of symbols and the production rules for rewriting some of them into every possible string of a formal language over an alphabet. A grammar does not describe the meaning of the strings—only their form.
>
> Source: Wikipedia contributors, “Formal grammar”, https://en.wikipedia.org/wiki/Formal_grammar, CC BY-SA 4.0. Unmodified.

## Formal language

> In logic, mathematics, computer science, and linguistics, a formal language is a set of strings whose symbols are taken from a set called "alphabet".
>
> Source: Wikipedia contributors, “Formal language”, https://en.wikipedia.org/wiki/Formal_language, CC BY-SA 4.0. Unmodified.

## Garbage Collection

> In computer science, garbage collection (GC) is a form of automatic memory management. The garbage collector attempts to reclaim memory that was allocated by the program, but is no longer referenced; such memory is called garbage. Garbage collection was invented by American computer scientist John McCarthy around 1959 to simplify manual memory management in Lisp.
>
> Source: Wikipedia contributors, “Garbage collection (computer science)”, https://en.wikipedia.org/wiki/Garbage_collection_(computer_science), CC BY-SA 4.0. Unmodified.

## Generic Types

> Generic programming is a style of computer programming in which algorithms are written in terms of data types to-be-specified-later that are then instantiated when needed for specific types provided as parameters. This approach, pioneered in the programming language ML in 1973,[1][2] permits writing common functions or data types that differ only in the set of types on which they operate when used, thus reducing duplicate code.
>
> Source: Wikipedia contributors, “Generic programming”, https://en.wikipedia.org/wiki/Generic_programming, CC BY-SA 4.0. Unmodified.

## Gradual Typing

> Gradual typing is a type system that allows for both static typing and dynamic typing but enforces types at runtime. Gradual typing allows software developers to choose either type paradigm as appropriate, from within a single language.
>
> Source: Wikipedia contributors, “Gradual typing”, https://en.wikipedia.org/wiki/Gradual_typing, CC BY-SA 4.0. Unmodified.

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

> The Language Server Protocol (LSP) is an open, JSON-RPC-based protocol for use between source-code editors or integrated development environments (IDEs) and servers that provide "language intelligence tools" programming language-specific features like code completion, syntax highlighting and marking of warnings and errors, as well as refactoring routines. The goal of the protocol is to allow programming language support to be implemented and distributed independently of any given editor or IDE. In the early 2020s, LSP quickly became a "norm" for language intelligence tools providers.
>
> Source: Wikipedia contributors, “Language Server Protocol”, https://en.wikipedia.org/wiki/Language_Server_Protocol, CC BY-SA 4.0. Unmodified.

The Language Server Protocol (LSP) is a JSON-RPC-based protocol for use between editors or IDEs and servers that provide: code completion, syntax highlighting and marking of warnings and errors, as well as refactoring routines.

https://microsoft.github.io/language-server-protocol/

## Lexer

> Lexical tokenization is conversion of a text into (semantically or syntactically) meaningful lexical tokens belonging to categories defined by a "lexer" program. In case of a natural language, those categories include nouns, verbs, adjectives, punctuations etc. In case of a programming language, the categories include identifiers, operators, grouping symbols, data types and language keywords. Lexical tokenization is related to the type of tokenization used in large language models (LLMs) but with two differences. First, lexical tokenization is usually based on a lexical grammar, whereas LLM tokenizers are usually probability-based. Second, LLM tokenizers perform a second step that converts the tokens into numerical values.
>
> Source: Wikipedia contributors, “Lexical analysis”, https://en.wikipedia.org/wiki/Lexical_analysis, CC BY-SA 4.0. Unmodified.

A lexer is responsible for breaking down the input source code into [tokens](#tokens).

## LL Grammar

> In formal language theory, an LL grammar is a context-free grammar that can be parsed by an LL parser, which parses the input from Left to right, and constructs a Leftmost derivation of the sentence (hence LL, compared with LR parser that constructs a rightmost derivation). A language that has an LL grammar is known as an LL language. These form subsets of deterministic context-free grammars (DCFGs) and deterministic context-free languages (DCFLs), respectively. One says that a given grammar or language "is an LL grammar/language" or simply "is LL" to indicate that it is in this class.
>
> LL parsers are table-based parsers, similar to LR parsers. LL grammars can alternatively be characterized as precisely those that can be parsed by a predictive parser – a recursive descent parser without backtracking – and these can be readily written by hand. This article is about the formal properties of LL grammars; for parsing, see LL parser or recursive descent parser.
>
> Source: Wikipedia contributors, “LL grammar”, https://en.wikipedia.org/wiki/LL_grammar, CC BY-SA 4.0. Unmodified.

## LL Parser

> In computer science, an LL parser is a top-down parser for a restricted context-free language. It parses the input from Left to right, performing Leftmost derivation of the sentence.
>
> An LL parser is called an LL(k) parser if it uses k tokens of lookahead when parsing a sentence. A grammar is called an LL(k) grammar if an LL(k) parser can be constructed from it. A formal language is called an LL(k) language if it has an LL(k) grammar. The set of LL(k) languages is properly contained in that of LL(k+1) languages, for each k ≥ 0. A corollary of this is that not all context-free languages can be recognized by an LL(k) parser.
>
> Source: Wikipedia contributors, “LL parser”, https://en.wikipedia.org/wiki/LL_parser, CC BY-SA 4.0. Unmodified.

## LR Parser

> In computer science, LR parsers are a type of bottom-up parser that analyse deterministic context-free languages in linear time.[1] There are several variants of LR parsers: SLR parsers, LALR parsers, canonical LR(1) parsers, minimal LR(1) parsers, and generalized LR parsers (GLR parsers). LR parsers can be generated by a parser generator from a formal grammar defining the syntax of the language to be parsed. They are widely used for the processing of computer languages.
>
> Source: Wikipedia contributors, “LR parser”, https://en.wikipedia.org/wiki/LR_parser, CC BY-SA 4.0. Unmodified.

| Invented By  |
| ------------ |
| Donald Knuth |

| Invented In |
| ----------- |
| 1968        |

## LALR

> An LALR parser[a] (look-ahead, left-to-right, rightmost derivation parser) is a type of parser for computer languages. It is a simplified version of a canonical LR parser.
>
> Source: Wikipedia contributors, “LALR parser”, https://en.wikipedia.org/wiki/LALR_parser, CC BY-SA 4.0. Unmodified.

> Generally, the LALR parser refers to the LALR(1) parser,[b] just as the LR parser generally refers to the LR(1) parser. The "(1)" denotes one-token lookahead, to resolve differences between rule patterns during parsing. Similarly, there is an LALR(2) parser with two-token lookahead, and LALR(k) parsers with k-token lookup, but these are rare in actual use. The LALR parser is based on the LR(0) parser, so it can also be denoted LALR(1) = LA(1)LR(0) (1 token of lookahead, LR(0)) or more generally LALR(k) = LA(k)LR(0) (k tokens of lookahead, LR(0)). There is in fact a two-parameter family of LA(k)LR(j) parsers for all combinations of j and k, which can be derived from the LR(j + k) parser,[9] but these do not see practical use.
>
> As with other types of LR parsers, an LALR parser is quite efficient at finding the single correct bottom-up parse in a single left-to-right scan over the input stream, because it does not need to use backtracking. Being a lookahead parser by definition, it always uses a lookahead, with LALR(1) being the most-common case.
>
> Source: Wikipedia contributors, LALR parser, https://en.wikipedia.org/wiki/LALR_parser, CC BY-SA 4.0. Unmodified.

| Invented By                |
| -------------------------- |
| Frank DeRemer/Tom Pennello |

| Invented In |
| ----------- |
| 1969/1979   |

## Lexeme

> What is called "lexeme" in rule-based natural language processing is not equal to what is called lexeme in linguistics. What is called "lexeme" in rule-based natural language processing can be equal to the linguistic equivalent only in analytic languages, such as English, but not in highly synthetic languages, such as fusional languages. What is called a lexeme in rule-based natural language processing is more similar to what is called a word in linguistics (not to be confused with a word in computer architecture), although in some cases it may be more similar to a morpheme.
>
> Source: Wikipedia contributors, “Lexical analysis”, https://en.wikipedia.org/wiki/Lexical_analysis, CC BY-SA 4.0. Unmodified.

## Literals

https://en.wikipedia.org/wiki/Literal_(computer_programming)

## Macros

> In computer programming, a macro (short for "macro instruction"; from Greek μακρο- 'long, large'[1]) is a rule or pattern that specifies how a certain input should be mapped to a replacement output. Applying a macro to an input is known as macro expansion.
>
> Source: Wikipedia contributors, “Macro (computer science)”, https://en.wikipedia.org/wiki/Macro_(computer_science), CC BY-SA 4.0. Unmodified.

### Hygenic Macros

> In computer science, hygienic macros are macros whose expansion is guaranteed not to cause the accidental capture of identifiers. They are a feature of programming languages such as Scheme,[1] Dylan,[2] Rust, Nim, and Julia. The general problem of accidental capture was well known in the Lisp community before the introduction of hygienic macros. Macro writers would use language features that would generate unique identifiers (e.g., gensym) or use obfuscated identifiers to avoid the problem. Hygienic macros are a programmatic solution to the capture problem that is integrated into the macro expander. The term "hygiene" was coined in Kohlbecker et al.'s 1986 paper that introduced hygienic macro expansion, inspired by terminology used in mathematics.
>
> Source: Wikipedia contributors, “Hygienic macro”, https://en.wikipedia.org/wiki/Hygienic_macro, CC BY-SA 4.0. Unmodified.

### X Macro

> X macros are an idiomatic usage of programming language macros for generating list-like structures of data or code. They are most useful when at least some of the lists cannot be composed by indexing, such as at compile time. They provide reliable maintenance of parallel lists whose corresponding items must be declared or executed in the same order.
>
> Source: Wikipedia contributors, “X macro”, https://en.wikipedia.org/wiki/X_macro, CC BY-SA 4.0. Unmodified.

## Operators

TODO

## Parser

A parser transforms a collection of [tokens](#tokens) in to an [AST](#ast) or [CST](#concrete-syntax-tree).

https://en.wikipedia.org/wiki/Parsing#Parser

## Parse Tree

> A parse tree or parsing tree[1] (also known as a derivation tree or concrete syntax tree) is an ordered, rooted tree that represents the syntactic structure of a string according to some context-free grammar. The term parse tree itself is used primarily in computational linguistics; in theoretical syntax, the term syntax tree is more common.
>
> Source: Wikipedia contributors, “Parse tree”, https://en.wikipedia.org/wiki/Parse_tree, CC BY-SA 4.0. Unmodified.

## Parsing Precedence

> In computer science, an operator-precedence parser is a bottom-up parser that interprets an operator-precedence grammar. For example, most calculators use operator-precedence parsers to convert from the human-readable infix notation relying on order of operations to a format that is optimized for evaluation such as Reverse Polish notation (RPN).
>
> Source: Wikipedia contributors, “Operator-precedence parser”, https://en.wikipedia.org/wiki/Operator-precedence_parser, CC BY-SA 4.0. Unmodified.

## Parametric polymorphism

> In programming languages and type theory, parametric polymorphism allows a single piece of code to be given a "generic" type, using variables in place of actual types, and then instantiated with particular types as needed.[1]: 340  Parametrically polymorphic functions and data types are sometimes called generic functions and generic datatypes, respectively, and they form the basis of generic programming.
>
> Source: Wikipedia contributors, “Parametric polymorphism”, https://en.wikipedia.org/wiki/Parametric_polymorphism, CC BY-SA 4.0. Unmodified.

## Pattern Matching

> In computer science, pattern matching is the act of checking a given sequence of tokens for the presence of the constituents of some pattern. In contrast to pattern recognition, the match usually must be exact: "either it will or will not be a match." The patterns generally have the form of either sequences or tree structures. Uses of pattern matching include outputting the locations (if any) of a pattern within a token sequence, to output some component of the matched pattern, and to substitute the matching pattern with some other token sequence (i.e., search and replace).
>
> Source: Wikipedia contributors, “Pattern matching”, https://en.wikipedia.org/wiki/Pattern_matching, CC BY-SA 4.0. Unmodified.

## Polymorphism

> In programming language theory and type theory, polymorphism allows a value or variable to have more than one type and allows a given operation to be performed on values of more than one type.[
>
> Source: Wikipedia contributors, “Polymorphism (computer science)”, https://en.wikipedia.org/wiki/Polymorphism_(computer_science), CC BY-SA 4.0. Unmodified.

## Pratt Parser

https://en.wikipedia.org/wiki/Operator-precedence_parser#Pratt_parsing

## Predicate

https://en.wikipedia.org/wiki/Predicate_(logic)

## Product Type

> In programming languages and type theory, a product of types is another, compounded, type in a structure. The "operands" of the product are types, and the structure of a product type is determined by the fixed order of the operands in the product. An instance of a product type retains the fixed order, but otherwise may contain all possible instances of its primitive data types. The expression of an instance of a product type will be a tuple, and is called a "tuple type" of expression. A product of types is a direct product of two or more types.
>
> Source: Wikipedia contributors, “Product type”, https://en.wikipedia.org/wiki/Product_type, CC BY-SA 4.0. Unmodified.

## Production Rules

> In computer science, a production or production rule is a rewrite rule that replaces some symbols with other symbols.[1] A finite set of productions
> ${\displaystyle P}$ is the main component in the specification of a formal grammar (specifically a generative grammar).
>
> Source: Wikipedia contributors, “Production (computer science)”, https://en.wikipedia.org/wiki/Production_(computer_science), CC BY-SA 4.0. Unmodified.

## Quantifier

https://en.wikipedia.org/wiki/Quantifier_(logic)

## Recursive descent parser

> In computer science, a recursive descent parser is a kind of top-down parser built from a set of mutually recursive procedures (or a non-recursive equivalent) where each such procedure implements one of the nonterminals of the grammar. Thus the structure of the resulting program closely mirrors that of the grammar it recognizes.
>
> Source: Wikipedia contributors, “Recursive descent parser”, https://en.wikipedia.org/wiki/Recursive_descent_parser, CC BY-SA 4.0. Unmodified.

## Runtime Errors

Runtime [errors](#error) happen during the programs execution and are typically errors that weren't/couldn't be caught at lexing/parsing/compile time.

## Shift Reduce Parser

> A shift-reduce parser is a class of efficient, table-driven bottom-up parsing methods for computer languages and other notations formally defined by a grammar. The parsing methods most commonly used for parsing programming languages, LR parsing and its variations, are shift-reduce methods.[1] The precedence parsers used before the invention of LR parsing are also shift-reduce methods. All shift-reduce parsers have similar outward effects, in the incremental order in which they build a parse tree or call specific output actions.
>
> Source: Wikipedia contributors, “Shift-reduce parser”, https://en.wikipedia.org/wiki/Shift-reduce_parser, CC BY-SA 4.0. Unmodified.

## Side Effect

> In computer science, an operation or expression is said to have a side effect if it has any observable effect other than its primary effect of reading the value of its arguments and returning a value to the invoker of the operation. Example side effects include modifying a non-local variable, a static local variable or a mutable argument passed by reference; performing I/O; or calling other functions with side-effects.
>
> Source: Wikipedia contributors, “Side effect (computer science)”, https://en.wikipedia.org/wiki/Side_effect_(computer_science), CC BY-SA 4.0. Unmodified.

## Spans

Spans represent a position within a given piece of text. This can be represented in various forms: line/column, start/end, start/length.

## Statement

> In computer programming, a statement is a syntactic unit of an imperative programming language that expresses some action to be carried out.[1] [vague] A program written in such a language is formed by a sequence of one or more statements. A statement may have internal components (e.g. expressions).
>
> Source: Wikipedia contributors, “Statement (computer science)”, https://en.wikipedia.org/wiki/Statement_(computer_science), CC BY-SA 4.0. Unmodified.

A statement is a piece of code that does not generate a value but does generate a side effect. Statements include declarations (variables, functions, structs, enums), expression statements, control flow statements, etc.

## Substructural type system

> Substructural type systems are a family of type systems analogous to substructural logics where one or more of the structural rules are absent or only allowed under controlled circumstances. Such systems can constrain access to system resources such as files, locks, and memory by keeping track of changes of state and prohibiting invalid states.
>
> Source: Wikipedia contributors, “Substructural type system”, https://en.wikipedia.org/wiki/Substructural_type_system, CC BY-SA 4.0. Unmodified.

## Subtyping

> In programming language theory, subtyping (also called subtype polymorphism or inclusion polymorphism) is a form of type polymorphism. A subtype is a datatype that is related to another datatype (the supertype) by some notion of substitutability, meaning that program elements (typically subroutines or functions), written to operate on elements of the supertype, can also operate on elements of the subtype.
>
> Source: Wikipedia contributors, “Subtyping”, https://en.wikipedia.org/wiki/Subtyping, CC BY-SA 4.0. Unmodified.

## Sum Type

See: [tagged union](#tagged-union)

## Syntactic Sugar

> In computer science, syntactic sugar is syntax within a programming language that is designed to make things easier to read or to express. It makes the language "sweeter" for human use: things can be expressed more clearly, more concisely, or in an alternative style that some may prefer. Syntactic sugar is usually a shorthand for a common operation that could also be expressed in an alternate, more verbose, form: The programmer has a choice of whether to use the shorter form or the longer form, but will usually use the shorter form since it is shorter and easier to type and read.
>
> Source: Wikipedia contributors, “Syntactic sugar”, https://en.wikipedia.org/wiki/Syntactic_sugar, CC BY-SA 4.0. Unmodified.

Syntactic sugar "sugar" is syntax in the language that will be expanded to other syntax at compile time.

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

> In formal languages, terminal and nonterminal symbols are parts of the vocabulary under a formal grammar. Vocabulary is a finite, nonempty set of symbols. Terminal symbols are symbols that cannot be replaced by other symbols of the vocabulary. Nonterminal symbols are symbols that can be replaced by other symbols of the vocabulary by the production rules under the same formal grammar.
>
> Source: Wikipedia contributors, “Terminal and nonterminal symbols”, https://en.wikipedia.org/wiki/Terminal_and_nonterminal_symbols, CC BY-SA 4.0. Unmodified.

## Tagged Union

> In computer science, a tagged union, also called a variant, variant record, choice type, discriminated union, disjoint union, sum type, or coproduct, is a data structure used to hold a value that could take on several different, but fixed, types. Only one of the types can be in use at any one time, and a tag field explicitly indicates which type is in use. It can be thought of as a type that has several "cases", each of which should be handled correctly when that type is manipulated. This is critical in defining recursive datatypes, in which some component of a value may have the same type as that value, for example in defining a type for representing trees, where it is necessary to distinguish multi-node subtrees and leaves. Like ordinary unions, tagged unions can save storage by overlapping storage areas for each type, since only one is in use at a time.
>
> Source: Wikipedia contributors, “Tagged union”, https://en.wikipedia.org/wiki/Tagged_union, CC BY-SA 4.0. Unmodified.

## Tokens

Tokens are the smallest meaningfully defined units in a programming language, such as [keywords](#keywords), [identifiers](#identifiers), [operators](#operators), and [literals](#literals).

https://en.wikipedia.org/wiki/Lexical_analysis

### Token Position Information

Lexers can record a token's position (see [span](#spans)) in the original source code, which is useful for generating error message and debugging.

## Type

A type denotes what kind a value is. e.g. string, number, boolean, object in a [type system](#type-system).

https://en.wikipedia.org/wiki/Data_type

## Type Checker

A typechecker verifies all that all the [types](#type) of a program and it's inputs are correct in a [type system](#type-system).

## Type Error

A type [error](#error) denotes a value violates a program or a language's typing rules during [typechecking](#type-checker).

## Type Inference

Type inference is the detection of a variable/function return/function parameter's [type](#type) without adding a type in the source code. The type is determined by it's use e.g. what value is being assigned, what operation is being performed (`a + 1` means `a` is a number), what argument is passed.

## Type System

> A programming language consists of a system of allowed sequences of symbols (constructs) together with rules that define how each construct is interpreted. For example, a language might allow expressions representing various types of data, expressions that provide structuring rules for data, expressions representing various operations on data, and constructs that provide sequencing rules for the order in which to perform operations.
>
> Source: Wikipedia contributors, “Type system”, https://en.wikipedia.org/wiki/Type_system, CC BY-SA 4.0. Unmodified.

## Universal quantification

> In mathematical logic, a universal quantification is a type of quantifier, a logical constant which is interpreted as "given any", "for all", "for every", or "given an arbitrary element". It expresses that a predicate can be satisfied by every member of a domain of discourse. In other words, it is the predication of a property or relation to every member of the domain. It asserts that a predicate within the scope of a universal quantifier is true of every value of a predicate variable.
>
> Source: Wikipedia contributors, “Universal quantification”, https://en.wikipedia.org/wiki/Universal_quantification, CC BY-SA 4.0. Unmodified.

**∀**

See: [Type Systems](#type-system)

https://gist.github.com/kyleect/7f0580432d738bc61e78e69ac2e7a9ac
