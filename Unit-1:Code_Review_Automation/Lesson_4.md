# What is Code Coverage?

## Code Coverage Definition

Methodology that quantitatively measures how comprehensive a code base's tests are.
Increasing code coverage often increases stability and reduces bugs.

#### Codes Lines Types

1. Syntax Lines
2. Logic Lines
3. Branch Lines

#### Code Coverage Formula =

total # of non-systax lines with tests
/
total # of non-systax lines

## Branch Coverage Definition

Instead Measuring how many lines of code, it measures **groups of lines**.

Ex:

- main branch
- body of a loop
- a if statement

## When to care about code coverage

- Your product has users and those users might leave if they are affected by by bugs
- Your working with developers that aren't immediately trustworthy like contactors/interns
- Your working on a very large code base with many testable components

### Common mistakes

- **too many** tests for **uncertain features**

## Rules - Organizational - Code Coverage Policies

1. Code coverage must not decrease - taking over existing codebase
2. Code owners for test files

## When to use Code Coverage

If you are working in a large code base using **TDD**, hiring **interns/contractors** or have **user sensitive to bugs**, it's time to measure code coverage.

## Open Source Solution

- Codecov
- COVERALLS
- CODE CLIMATE
