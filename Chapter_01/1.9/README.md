# 1.9 Introduction to literals and operators

## Literals

**Literal (a.k.a. literal constant):** a fixed value that has been inserted directly into the source code.

```cpp
std::cout << 5 << '\n'; // print the value of a literal

int x { 5 };
std::cout << x << '\n'; // print the value of a variable
```

## Operators

**Operation:** a process involving zero or mor input values (called operands) that produces a new value (called an output value).
* ```cpp
  std::cout << 1 + 2 << '/n';
  ```
  Output:
  >3

**Arity:** the number of operands that an operator takes a input.
* **Unary Operators:** act on one operand (-5)
* **Binary Operators:** act on two operands (3 + 4)
* **Ternary Operators:** act on three operands (conditional operator)
* **Nullary Operators:** act on zero operands (throw operator)

## Chaining operators

Operators in C++ can be chained, meaning the output of one operator can serve as the input for another. For example, in the expression `2 * 3 + 4`, multiplication is performed first (resulting in 6), and then addition is performed (resulting in 10). The order in which operators execute follows the same rules as in standard mathematics: Parentheses first, then Exponents, followed by Multiplication & Division, and finally Addition & Subtraction. This order is remembered by the acronym PEMDAS or the mnemonic “Please Excuse My Dear Aunt Sally.”

## Return values and side effects

In C++, most operators compute a return value from their operands (e.g., `-5` returns `-5` and `2 + 3` returns `5`). Some operators, like `delete` and `throw`, do not produce return values. Operators with observable effects beyond their return values are said to have side effects. For example, `x = 5` changes the value of `x`, and `std::cout << 5` prints `5` to the console.

In C++, the term "side effect" refers to these observable effects, which are often predictable and beneficial. Some operators, like the assignment operator (`=`) or the output operator (`<<`), are used primarily for their side effects. These operators can also return values, like `x = 5` returning `x` or `std::cout << 5` returning `std::cout`, enabling operator chaining. For example, `x = y = 5` first assigns `5` to `y` and then to `x`, while `std::cout << "Hello " << "world!"` prints both strings in sequence by chaining `std::cout`.