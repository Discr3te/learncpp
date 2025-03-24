# 1.1 Statements and the structure of a program

## Statements

**Statement:** a type of instruction that causes the program to perform some action.
* Statements are the most common type of instruction, serving as the smallest units of computation in the language, similar to sentences in natural language.
* Most C++ statements end with a semicolon, though not all. 
* A single statement in C++ can translate into multiple machine language instructions.

## Functions and the `main` function

**Function:** a collection of statements that get executed sequentially (in order, from top to bottom).
* Every C++ program must have a special function named **main** (all lower case letters).
* Functions are typically written to do specific job or perform som useful action.
* A pair of parentheses `()` is used after the function name to imply that the name is a function.

**Identifier:** the name of a function

## Dissecting Hello world!

```cpp
#include <iostream>

int main()
{
  std::cout << "Hello world!";
  return 0;
}
```

Line 1: Preprocessor directive (#include), imports the iostream library for console input/output. Without it, line 5 would cause a compile error.

Line 2: Blank line, ignored by the compiler, used for readability.

Line 3: Defines the main function, which every C++ program must have. It returns an integer (int).

Lines 4-7: Marks the function body of main with opening { and closing } curly braces.

Line 5: First statement in main, displays "Hello world!" on the console using std::cout.

Line 6: Return statement that returns 0 to the operating system, indicating successful program execution.
