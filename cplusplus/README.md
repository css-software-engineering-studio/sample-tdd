# Getting Started

The purpose of the project is to let you practice using TDD (Test-Driven Development, aka Test-Driven Design).

To experience TDD, use the red-green-refactoring pattern to fully implement the IntegerToWordedString conversion function. This function takes an integer number and converts to a worded string (in whatever output language that you care to use for implementation though the initial test is based on English). The project source is explicitly stubbed out to a minimum implementation that only defines main program, the conversion function declaration, and two unit tests.

The code must do two things:
1. Correctly implement the desired functionality.

    Automated unit tests will help ensure this goal. 

2. Be easy for others to read and understand. 

    Refactoring the code to be "beautiful" production-quality code will help ensure this goal. See Robert Martin's excellent book [*Clean code: a handbook of agile software craftsmanship*](https://learning.oreilly.com/library/view/clean-code-a/9780136083238/). You should be proud to show the code to a peer. 

Code that meets both of these goals is critical for production code, 

Fully implement the specifications for 32-bit numbers. 

# Functional Specification

> ## IntegerToWordedString
>
> ### Description
>
> Converts an integer number to its equivalent worded name as string
> such as the integer number `1` being represented as the string `one`.
>
> ### Synopsis
>
>       string IntegerToWordedString(int number);
>
> ### Parameters
>
> `number` - non-negative integer value to be converted
>
> (return) - worded name equivalent of the input `number`
>
> ### Notes
>
> The implementation as provided in the same does not define any requirements
> about how language, culture, or related concerns should / could be
> addressed by the code.

# Developing using the Project

## Project Structure

### `sample/Program.cpp`

A simple console app interface for the conversion code. The console app takes a single integer parameter and outputs the converted worded string value on the console.

### `sample/lib/Converter.hpp`

The utility header that includes the `IntegerToWordedString` as a public static function.

### `sample-tests/doctest.h`

The `doctest.h` file is the core component of the `doctest` Unit Testing framework, the fastest one available on C++. \
The next file, `ConverterTests.cpp`, has been set up already to utilize the `doctest` framework, where there is no further action required on your part. \
If you wish to learn more about the `doctest` framework in general, you can find such [on their github.](https://github.com/doctest/doctest)

### `sample-tests/lib/ConverterTests.cpp`

The complete set of unit tests for the `IntegerToWordedString` function that is the focus of this project. Note the starting set of unit tests contain one test `NotImplementedYet` that may be obsoleted if you implement the complete functionality or the conversion/specification.

## Building and Testing

While the system can be built and tested using different IDEs, this project was created and tested using VSCode. Testing was performed by running the full set of tests in the VSCode terminal window using the `g++` command -- specifically, executing `g++ -std=c++11 ConverterTests.cpp -o ConverterTests && ./ConverterTests` after changing the current directory to `sample-tests/lib` folder.

The first execution should result in final "red" state test status like:

> <span style='color:red;font-family:monospace;font-weight: bold'>Failed! - Failed: 1, Passed: 1, Skipped: 0, Total: 2</span>

## Using TDD to Implement the Feature

Follow the instructions in [IMPLEMENTATION.md](../IMPLEMENTATION.md).