# 1.7 Keywords and naming identifiers

## Identifier naming rules
Rules that must be followed when naming identifiers:
* The identifier can not be a keyword. Keywords are reserved.
* The identifier can only be composed of letters (lower or upper case), numbers, and the underscore character. That means the name can not contain symbols (except the underscore) nor whitespace (spaces or tabs).
* The identifier must begin with a letter (lower or upper case) or an underscore. It can not start with a number.
* C++ is case sensitive, and thus distinguishes between lower and upper case letters. `nvalue` is different than `nValue` is different than `NVALUE`.

## Identifier naming best practices

1. It is  conventional in C++ that variable names should begin with a lowercase letter. If the variable name is a single word or acronym, the whole thing should be written in lowercase letters.
   ```cpp
   int value; // conventional

   int Value; // unconventional (should start with lower case letter)
   int VALUE; // unconventional (should start with lower case letter and be in all lower case)
   int VaLuE; // unconventional (see your psychiatrist) ;)

   // multi-word function name
   int my_variable_name;   // conventional (separated by underscores/snake_case)
   int my_function_name(); // conventional (separated by underscores/snake_case)

   int myVariableName;     // conventional (intercapped/camelCase)
   int myFunctionName();   // conventional (intercapped/camelCase)

   int my variable name;   // invalid (whitespace not allowed)
   int my function name(); // invalid (whitespace not allowed)

   int MyVariableName;     // unconventional (should start with lower case letter)
   int MyFunctionName();   // unconventional (should start with lower case letter)
   ```

2. Avoid naming your identifiers starting with an underscore. Although syntactically legal, these names are typically reserved for OS, library, and/or compiler use.
3. The name of your identifiers should make clear what the value they are holding means (particularly if the units aren’t obvious). Identifiers should be named in a way that would help someone who has no idea what your code does be able to figure it out as quickly as possible. In 3 months, when you look at your program again, you’ll have forgotten how it works, and you’ll thank yourself for picking variable names that make sense.
4. Avoid abbreviations, except when they are common and unambiguous (e.g. `num`, `cm`, `idx`).
5. For variable declarations, it can be useful to use a comment to describe what a variable is going to be used for, or to explain anything else that might not be obvious. For example, say we’ve declared a variable that is supposed to store the number of characters in a piece of text. Does the text “Hello World!” have 10, 11, 12 characters? It depends on whether we’re including whitespace or punctuation. Rather than naming the variable `numCharsIncludingWhitespaceAndPunctuation`, which is rather lengthy, a well placed comment on or above the declaration line should help the user figure it out:
   ```cpp
   // a count of the number of chars in a piece of text, including whitespace and punctuation
   int numChars {};
   ```