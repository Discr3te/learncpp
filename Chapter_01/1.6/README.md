# 1.6 Uninitialized variables and undefined behavior

## Uninitialized variables

**Uninitialized variable:** a variable that has not been given a known value (through initialization or assignment).
* Initialized = The object is given a known value at the point of definition.
* Assignment = The  object is given a known value beyond the point of definition.
* Uninitialized = The object has not been given a known value yet.

```cpp
// define an integer variable named x
int x; // this variable is uninitialized because we haven't given it a value

// print the value of x to the screen
std::cout << x << '\n'; // who knows what we'll get, because x is uninitialized

```
## Undefined behavior

**Undefined behavior (abbreviated UB):** the result of executing code whose behavior is not well-defined by the C++ language.

Code implementing undefined behavior may exhibit any of the following symptoms:
* Your program produces different results every time it is run.
* Your program consistently produces the same incorrect result.
* Your program behaves inconsistently (sometimes produces the correct result, sometimes not).
* Your program seems like it’s working but produces incorrect results later in the program.
* Your program crashes, either immediately or later.
* Your program works on some compilers but not others.
* Your program works until you change some other seemingly unrelated code.

## Implementation-defined behavior and unspecified behavior

**Implementation:** a specific compiler and the associated standard library it come with.

**Unspecified behavior:** almost identical to implementation-defined behavior in that the behavior is left up to the implementation to define, but the implementation is not required to document the behavior.