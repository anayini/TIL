# Parsing Technqiues

## Recursive Descent Parsing

##### Simple Parsing Method:
1. Code cleanly maps to the production rules
```

   Terminal -> Match and Consume token
   Nonterminal -> Call function for that production rule
   | -> Switch statement
   * or + -> Loops
```

2. Can be easily hand written
3. Allows for easy error catching and reporting
4. Is not as powerful as some other parsing strategies
5. C#'s parser is a hand written recursive descent parser,
which demonstrates that this technique is at least powerful enough
to parse production level programming languages


#### Pratt Parsers
1. A type of recursive descent parser that focuses on associating
precendent with tokens rather than function calls.
2.  Uses a map from TokenType to Int to encode precendence values

#### LL Parsers
1. A type of recursive descent parser powerful enough to Match
a subset of context free grammars
2.  Typically described as LL(k) where k is the number of tokens
of lookahead needed to parse the grammar.
3.  K=1 parsers are easy to hand write, but it becomes harder for K > 1.
4. Many production level languages are written using handwritten LL parsers.

#### Packrat Parsers
1.  Similar to a recursive descent parser.
2.  Runs in linear time, but has larger storage requirements.
3.  Based on parsing expression grammars (a formal grammar similar to CFGs)

## Parser Combinators
1.  A way of designing a parser through the composition of smaller parsers.
2.  Tend to result in much more readable parsers.

## Compiler compilers / Parser generators
1.  Typically allow users to write a grammar in a DSL as input and get a parser as output.
2.  Less control over the parser and its internal state / error messaging
3.  Because of 2. this is why many production level languages use hand written recursive descent parsers.

## Error Productions
1.  A way to encode common syntax errors within a grammar.
2.  Make special rules that match common syntax errors.
3.  When parsing them we can handle them specially, instead of getting
confused and just being unable to parse!
