# Notes
---
These are rough notes for my understanding. At the end, I'll also make a mind map to connect concepts & visualize everything, since I've found kinesthetic & visual learning to be the most effective for my learning style.  

## 1.1
Lexical Analysis -> transformation from source code to tokens 
- done by a "lexer" 
- Source Code: a set of  instructions that guides a computer program's execution

What are tokens? -> small, easily categorizable data structures that are then fed to parser
- In Monkey language, whitespace doesn't show as tokens 

## 1.2 
The first step is building a lexer for Monkey, our programming language. 

1st step: defining tokens 
- ex. Identifiers, operates, keywords, etc. 

Every token needs two pieces of info: 1) type (what kind of token is this? number or keyword etc.), 2) value - needs a field that holds the *literal* value of the token 

TokenType should be defined as string - easy to debug + but keep in mind that it is worse for performance compared to an int or byte

## 1.3
Building our own lexer 
- Input = source code -> output = tokens that represent source code 
- creating a NextToken() method which: goes through source code token by token -> uses "string" as the type 
- in prod enviroment, should attach filenames + line numbers for debugging, but too complex for these purposes 