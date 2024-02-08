# C++ Compiler
A comprehensive, custom-built compiler for a subset of the **C++** programming language, designed to optimize **performance** and enhance **code efficiency**. This project encompasses a full-featured **compiler pipeline**, including **lexical analysis**, **assembling**, **parsing**, **semantic analysis**, and **code generation**. 

## Features
- **Lexical Analysis**: Accurate tokenization of C++ code into meaningful symbols
- **Assembler**: Efficiently translates assembly code into executable machine code
- **Parsing**: Robust syntax analysis using LR(1) parsing
- **Semantic Analysis**: In-depth validation of syntax trees against C++ language rules
- **Code Generation**: Generation of efficient machine code for MIPS

## Language Specifications
This compiler suite supports a tailored subset of C++ language specifications, focusing on core features essential for fundamental programming concepts and efficient execution. The supported features include:

- **Variable Declarations**: limited to `int` or `int*`, with all declarations requiring an unsigned integer constant or `NULL` initializer
- **Control Structures**: supports `if` (with mandatory `else` clause), `while`, and `return` statements
- **Statements and Expressions**: valid expressions include variable names, memory allocation (`new`), unary `&` and `*`, and binary operators `+ - * / % == != <= >= < >`
- **Memory Management**: dynamic allocation and deallocation are implemented through `new` and `delete []`
- **Function Design**: a single `return` statement is required at the end of functions

### Lexical Syntax
The compiler supports a rigorous lexical syntax that includes identifiers (`ID`), numeric literals (`NUM`), various symbols (`LPAREN`, `RPAREN`, `LBRACE`, `RBRACE`), keywords (`RETURN`, `IF`, `ELSE`, `WHILE`), and operators (`PLUS`, `MINUS`, `STAR`). Tokens are case-sensitive and follow specific rules to ensure a clear distinction between different types, with whitespace and comments being ignored during tokenization for a clean and unambiguous token sequence.

### Context-free Syntax
A precise context-free grammar is implemented, which structures programs into procedures, declarations, control structures, and expressions. The grammar supports basic data types (`int`, `int*`), control flow statements (`if`, `else`, `while`), function declarations with strict parameter and return types, and dynamic memory management through `new` and `delete` operations. The grammar enforces a clear separation between `declarations` and `statements` within functions.

### Context-sensitive Syntax
The compiler also enforces context-sensitive rules to ensure semantic correctness, such as unique procedure names, declaration before use, proper type matching in expressions and assignments, and strict function call conventions. Recursion is supported, but mutual recursion is not, maintaining a straightforward call hierarchy.

### Semantics
Following the lexical, context-free, and context-sensitive syntax rules, the compiler guarantees that programs are not only syntactically valid but also semantically meaningful, identical to the standard C++ semantics. This ensures that valid programs in the language subset can be seamlessly integrated into C++ environments, offering predictable and consistent behaviour.

## Contact to View Source Code
Due to the proprietary nature and extensive effort involved in developing this suite, access to the source code is restricted under intellectual property considerations. For inquiries or interest in collaboration, please reach out directly. I am currently working on implementing newer C++ features such as init-statements, structured bindings, and concepts, and any suggestions for improvements are highly appreciated. Please [contact me](mailto:a6abdulm@uwaterloo.ca).
