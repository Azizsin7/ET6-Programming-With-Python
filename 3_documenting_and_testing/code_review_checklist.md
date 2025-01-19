# Code Review Checklist

Writing a good function involves a lot of detail, way too much to remember right
away! This checklist can help you review your own or your classmates' code until
the details become a habit.

## Behavior

### Files

- [x] The file name describes the function's behavior
- [x] There is a module docstring in the function file
- [x] The test file's name matches the function file name -
  `/tests/test_file_name.py`
- [x] There is a module docstring in the tests file

### Unit Tests

- [x] The test class has a helpful name in PascalCase
- [x] The test class has a docstring
- Every unit test has
  - [x] A helpful name
  - [x] A clear docstring
  - [x] Only one assertion
  - [x] There is no logic in the unit test
- [x] All tests pass
- [x] There are tests for defensive assertions
- [x] There are tests for boundary cases

### Function Docstring

- [x] The function's behavior is described
- The function's arguments are described:
  - [x] Type
  - [x] Purpose
  - [x] Other assumptions (eg. if it's a number, what's the expected range?)
- The return value is described
  - [x] Type
  - [x] Other assumptions are documented
- The defensive assertions are documented using `Raises:`
  - [x] Each assumption about an argument is checked with an assertion
  - [x] Each assertion checks for _only one_ assumption about the argument
- [x] Include 3 or more (passing!) doctests

### The Function

- [x] The function's name describes it's behavior
- [x] The function's name matches the file name
  - _It's ok to have extra helper functions if necessary, like with mergesort_
- [x] The function has correct type annotations
- [x] The function is not called at the top level of the function file
  - _Recursive solutions **can** call the function from **inside** the function body_

## Strategy

### Do's

- [x] Variable names help to understand the strategy
- [x] Any comments are clear and describe the strategy
- [x] Lines of code are spaced to help show different stages of the strategy

### Don'ts

- [x] The function's strategy _is not_ described in any docstrings or tests
- [x] Comments explain the _strategy_, **not** the _implementation_
- [x] The function _does not_ have more comments than code
  - If it does, consider finding a new strategy or a simpler implementation

## Implementation

- [x] The code passes the formatting checks
- [x] The code passes all Ruff linting checks
- [x] The code has no (reasonable) Pylint errors
  - In code review, you can decide when fixing a Pylint error is helpful and
    when it's too restricting.
- [x] Variables are named with snake_case
- [x] Variable names are clear and helpful
- [x] The code follows the strategy as simply as possible
- [x] The implementation is as simple as possible given the strategy
- [x] There are no commented lines of code
- [x] There are no `print` statements anywhere
- [x] The code includes defensive assertions
- [x] Defensive assertions include as little logic as possible
