# 1.3 Introduction to objects and variables

## Data and values

**Data:** any information that can be moved, processed, or stored by a computer.

**Value (Data value):** a single piece of data.
* Numbers (e.g. 5 or -6.7).
* Characters, which are placed between single-quotes (e.g. 'H' or '$'). Only a single symbol may be used.
* Text, which must be placed between double-quotes (e.g. "Hello" or "H"). Text can contain 0 or more characters.

**Literals:** values that are placed directly into the source code.

```cpp
#include <iostream> // for std::cout

int main()
{
  std::cout << 5;       // print the literal number `5`
  std::cout << -6.7;    // print the literal number `-6.7`
  std::cout << 'H';     // print the literal character `H`
  std::cout << "Hello"; // print the literal text `Hello`

  return 0;
}
```

## Objects and variables/variable creation

**Object:** represents a region of storage (typically RAM or a CPU register) that can hold a value

**Variable:** an object with a name

**Allocation:** process of reserving storage for an object's use

## Defining multiple variables

```cpp
int a;
int b;
// same as:
int a, b;

int a, int b; // wrong (compiler error)
int a; int b; // correct (but not recommended)

int a, double b;  // wrong (compiler error)
int a; double b;  // correct (but not recommended)
// correct (recommended)
int a;
double b; 
```
