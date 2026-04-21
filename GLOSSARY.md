# Glossary

## AST

An abstract syntax tree is a structure that represents a simplified version of a program's source code.

## Backpatching

In compiler and interpreter implementations, backpatching refers to modifying the control flow graph or other data structures after the program has been compiled or interpreted.

## Backtracking

https://en.wikipedia.org/wiki/Backtracking

## Context-Free grammar

https://en.wikipedia.org/wiki/Context-free_grammar

## Context-sensitive grammar

https://en.wikipedia.org/wiki/Context-sensitive_grammar

## Deterministic context-free grammar

https://en.wikipedia.org/wiki/Deterministic_context-free_grammar

## Deterministic context-free language

https://en.wikipedia.org/wiki/Deterministic_context-free_language

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

## Lexer

A lexer is responsible for breaking down the input source code into [tokens](#tokens).

## LL Grammar

In formal language theory, an LL grammar is a context-free grammar that can be parsed by an LL parser, which parses the input from Left to right, and constructs a Leftmost derivation of the sentence (hence LL, compared with LR parser that constructs a rightmost derivation). A language that has an LL grammar is known as an LL language. These form subsets of deterministic context-free grammars (DCFGs) and deterministic context-free languages (DCFLs), respectively. One says that a given grammar or language "is an LL grammar/language" or simply "is LL" to indicate that it is in this class.

LL parsers are table-based parsers, similar to LR parsers. LL grammars can alternatively be characterized as precisely those that can be parsed by a predictive parser – a recursive descent parser without backtracking – and these can be readily written by hand. This article is about the formal properties of LL grammars; for parsing, see LL parser or recursive descent parser.

## LL Parser

LL parser is a top-down parser for a restricted context-free language. It parses the input from Left to right, performing Leftmost derivation of the sentence.

An LL parser is called an LL(k) parser if it uses k tokens of lookahead when parsing a sentence. A grammar is called an LL(k) grammar if an LL(k) parser can be constructed from it.

A formal language is called an LL(k) language if it has an LL(k) grammar. The set of LL(k) languages is properly contained in that of LL(k+1) languages, for each k ≥ 0.[1] A corollary of this is that not all context-free languages can be recognized by an LL(k) parser.

## LR

| Invented By  |
| ------------ |
| Donald Knuth |

| Invented In |
| ----------- |
| 1968        |

## LALR

| Invented By                |
| -------------------------- |
| Frank DeRemer/Tom Pennello |

| Invented In |
| ----------- |
| 1969/1979   |

Generally, the LALR parser refers to the LALR(1) parser, just as the LR parser generally refers to the LR(1) parser The "(1)" denotes one-token lookahead, to resolve differences between rule patterns during parsing.

Similarly, there is an LALR(2) parser with two-token lookahead, and LALR(k) parsers with k-token lookup, but these are rare in actual use.

## Parser

A parser transforms a collection of [tokens](#tokens) in to an abstract syntax tree ([AST](#ast)).

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

## Shift Reduce Parser

https://en.wikipedia.org/wiki/Shift-reduce_parser

## Spans

Spans represent a position within a given piece of text. This can be represented in various forms: line/column, start/end, start/length.

## Syntactical Errors

Syntax errors occur when the input source code fails to comply to language rules during the lexing or parsing process.

## Terminal and nonterminal symbols

https://en.wikipedia.org/wiki/Terminal_and_nonterminal_symbols

## Tokens

Tokens are the smallest meaningfully defined units in a programming language, such as keywords, identifiers, operators, and literals.

### Token Position Information

Lexers can record a token's position (see [span](#spans)) in the original source code, which is useful for generating error message and debugging.

## Universal quantification

**∀**

https://en.wikipedia.org/wiki/Universal_quantification
