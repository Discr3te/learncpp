# 1.4 Variable assignment and initialization

## Variable assignment

**Assignment:** giving a variable a value (in a separate statement) using the `=` operator.
* Assignment Operator: `=`
* Used whenever we want to change the value held by a variable
* ```cpp
  int width;  // define a variable named width
  width = 5;  // copy assignment of value 5 into variable width

  std::cout << width; // prints 5

  width = 7; // change value stored in variable width to 7

  std::cout << width; //prints 7
  ```
  Output:
  >57

**Copy-assignment:** assignment copies the value on the right-hand side of the `=` operator to the variable ont he left-hand side of the operator.

## Variable initialization

**Initialization:** the process of specifying an initial value for an object.
* The syntax used to initialize an object is called an **initializer** (`{}`)
* ```cpp
  int width { 5 };    // define variable width and initialize with initial value 5
  std::cout << width; // prints 5
  ```

## Different forms of initialization

```cpp
// Different forms of initialization:
  int a;         // default-initialization (no initializer)

  // Traditional initialization forms
  int b = 5;     // copy-initialization (initial value after equals sign)
  int c ( 6 );   // direct-initialization (initial value in parenthesis)

  // Modern initialization forms (preferred)
  int d { 7 };   // direct-list initialization (initial value in braces)
  int f {};      // value-initialization (empty braces), (used when you are immediately replacing that value)
  int f { 0 };   // zero-initialization (used only when you are going to use the 0)

  int height = { 6 }; // copy-list-initialization (rarely used)



  // list initialization disallows narrowing conversion:

  // An integer can only hold non-fractional values
  int w1 { 4.5 }; // compile error: list init does not allow narrowing conversion of 4.5 to 4
  w1 = 4.5;       // okay: copy-assignment allows narrowing conversions of 4.5 to 4

  int w2 = 4.5;   // compiles: copy-init initializes width with 4
  int w3(4.5);    // compiles: direct-init initializes width with 4



  // initializing multiple variables:
  int a, b; // create variables a and b, but do not initialize them

  int a = 5, b = 6;          // copy-initialization
  int c( 7 ), d( 8 );        // direct-initialization
  int e { 9 }, f { 10 };     // direct-list-initialization
  int i {}, j {};            // value-initialization

  int a, b = 5;     // wrong: a is not initialized to 5!
  int a = 5, b = 5; // correct: a and b are initialized to 5
```

## The `[[maybe_unused]]` attribute (c++17)

```cpp
// unused initialized variable warning: [[maybe_unused]] C++17
[[maybe_unused]] double pi { 3.14159 };  // Don't complain if pi is unused
[[maybe_unused]] double gravity { 9.8 }; // Don't complain if gravity is unused
[[maybe_unused]] double phi { 1.61803 }; // Don't complain if phi is unused

std::cout << pi << '\n';
std::cout << phi << '\n';

// The compiler will no longer warn about gravity not being used
```
