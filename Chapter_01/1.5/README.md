# 1.5 Introduction to iostream: cout, cin, and endl

**input/output library:** part of the C++ standard library that deals with basic input and output.
* ```cpp
  #include <iostream>

  // rest of code that sues iostream functionality here
  ```

## `std::cout` (character output)
`std::cout`: allows us to send data to the cosole to be printed as text.

**Insertion Operator** `<<`: used to send (or "insert") data into the output stream.

```cpp
std::cout << "Hello world!"; // print Hello world! to console
std::cout << "Hello" << " world!";  // print Hello world! to console

std::cout << 4; // print 4 to console

int x{ 5 }; // define integer variable x, initialized with value 5
std::cout << x; // print value of x (5) to console

std::cout << "x is equal to: " << x;  // prints x is equal to: 5
```
## Using `std::endl` (end line) to output a newline

**Newline:** an OS-specific character or sequence of characters that move the cursor to the start fo the next line.

`std::endl`: one way to output a newline is to output.
* ```cpp
  std::cout << "Hi!" << std::endl;  // std::endl will cause the cursor to move to the next line
  std::cout << "My name is Alex." << std:endl;
  ```
  Output:
  >Hi!\
  My name is Alex.

## `std::endl` vs `\n`

### `std::endl`
Inefficient, as it actually does two jobs: it outputs a newline(moving the cursor to the next line of the console), and it flushes the buffer (which is slow). If we output multiple lines o text ending with st::endl, we will get multiple flushes, which is slow and probably unnecessary.

### `\n`
We use `\n` (inside either single or double quotes) to output a newline without flushing the output buffer.

```cpp
int x{ 5 };
std::cout << "x is equal to: " << x << '\n'; // single quoted (by itself) (conventional)
std::cout << "Yep." << "\n";                 // double quoted (by itself) (unconventional but okay)
std::cout << "And that's all, folks!\n";     // between double quotes in existing text (conventional)
```
## `std::cin` (character input)

`std::cin`: used to read input form keyboard

**Extraction Operator** `>>`: put the input data in a variable.

```cpp
std::cout << "Enter a number: "; // ask user for a number

int x{};       // define variable x to hold user input (and value-initialize it)
std::cin >> x; // get number from keyboard and store it in variable x

std::cout << "You entered " << x << '\n';
```
## `std::cout`/`std::cin` is buffered

**Buffer:** a temporary storage location in a program's memory for data that is being moved or processed.

* Periodically, the buffer is flushed, meaning all of the data collected in the buffer is transferred to its destination.

* Both std::cout and std::cin is buffered.

### `std::cout`

Outputting dat is a two stage process:
* The data from each output request is added (to the end) of the an output buffer.
* Later, data from (the front of) the output buffer is flushed to the output device (the console)

### `std::cin`

Inputting data is a two stage process:
* The individual characters you enter as input are added to the end of an input buffer (inside `std::cin`). The enter key (pressed to submit the data) is also stored as a `\n` character.
* The extraction operator removes character form the front of the input buffer and converts them into a value that assigned (via copy-assignment) to the associated variable. This variable can then be used in subsequent statements.
