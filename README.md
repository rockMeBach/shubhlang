# ShubhLang

A very basic coding language that I implemented last year using Java. It's named after my cousin Shubham who likes One Piece a lot, hence "ShubhLang".
As of now, you can only perform some arithmetic operations, declare variables, print stuff and all.
I was following "Crafting Interpreters" by Robert Nystrom (creator of Dart).

## How to use

- You can create variables using the keyword "var", for e.g., var a = 1;
- Every expression must end with a semicolon;
- You can either run the program without arguments (ShubhLang.java is the main class with the entry-point) which will start a REPL loop or you can create a file and write ShubhLang code in it then run with the filename as the argument.
- I use Eclipse so I have my run configurations there.

## How ShubhLang works (a high-level overview)

- It takes your code, runs it through a scanner which goes through your code and returns all the tokens in an ArrayList.
- Then the tokens are fed to a parser, which creates an AST (Abstract Syntax Tree) and returns a list of statements.
- Those statements are finally read by the interpreter which returns an output.
- ShubhLang uses a Tree-Walk interpreter. It also has a very basic error handling mechanism.
- All the token types can be found in the TokenTypes.java file.

## Grammar definition

- Assign     : Token name, Expr value
- Binary     : Expr left, Token operator, Expr right
- Grouping   : Expr expression
- Literal    : Object value
- Unary      : Token operator, Expr right
- Variable   : Token name
- Expression : Expr expression
- Print      : Expr expression
- Var        : Token name, Expr initializer