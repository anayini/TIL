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
