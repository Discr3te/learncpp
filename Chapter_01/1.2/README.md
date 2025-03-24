# 1.2 Comments

**Comment:** a programmer-readable note that is inserted directly into the source code of the program
* Comments are ignored by the compiler and are for the programmer's use only.

## Single-line comments

```cpp
std::cout << "Hello world!";  // Everything from here to the end of the line is ignored
```

## Multi-line comments

```cpp
/* This is a multi-line comment.
   This line will be ignored.
   So will this one. */

/* This is a multi-line /* comment */ this is not inside the comment */
// The above comment ends at the first */, not the second */
```