# 6.100L Lecture 1 – Introduction to Computation and Python

## What is Computation?
- **Declarative Knowledge**: Facts (e.g., "The Earth orbits the Sun").
- **Imperative Knowledge**: Procedures/recipes (e.g., how to bake a cake).
- **Programming**: Writing *recipes* to generate *facts*.

---

## Numerical Example: Square Root Approximation
- Given a number `x`, the square root `y` satisfies `y * y = x`.
- Start with a guess `g`:
  1. If `g * g` is close to `x`, return `g`.
  2. Else, update guess: `g = (g + x/g) / 2`.
  3. Repeat until convergence.

**Example**:
```
x = 16, initial g = 3
1. g = 3         → g² = 9         → x/g = 5.33      → new g = 4.17
2. g = 4.17      → g² = 17.36     → x/g = 3.837     → new g = 4.0035
3. g = 4.0035    → g² = 16.03     → x/g = 3.997     → new g = 4.000002
```

---

## Algorithms: Definition
- A **sequence of steps** to solve a problem.
- Includes:
  1. A clear set of steps.
  2. A defined flow of control.
  3. A stopping condition.

> **Analogy**: A cake recipe is an algorithm.

---

## Computers: Machines That Execute Algorithms
- Two capabilities:
  - Perform simple operations very quickly.
  - Store and retrieve large amounts of data.
- **Types of Computers**:
  - **Fixed Program** (pre-1940s): Limited to predefined tasks.
  - **Stored Program**: Stores instructions in memory and executes them.

### Key Insight:
> Programs are data too!

---

## Components of a Computer (Simplified)
- **Memory**: Stores data and programs.
- **Control Unit**: Manages instruction execution.
- **Arithmetic/Logic Unit (ALU)**: Performs calculations and logic.
- **Input/Output**: Interfaces for user and data interaction.

---

## Programming Language Concepts

### 1. **Primitives**
- Basic data types and operations (e.g., numbers, strings, +, -, *).

### 2. **Syntax**
- Rules defining valid expressions.
  - Valid: `"hi" * 5`
  - Invalid: `"hi"5`

### 3. **Static Semantics**
- Valid syntax but incorrect usage.
  - Example: `"hi" + 5` (valid syntax, but undefined behavior)

### 4. **Semantics**
- Meaning of syntactically correct statements.
- Programs must have one well-defined meaning (unlike natural language).

---

## Common Programming Errors
- **Syntactic Errors**: Grammar mistakes (e.g., missing `:`).
- **Static Semantic Errors**: Type mismatches or invalid operations.
- **Logic Errors**: Program runs but doesn’t do what was intended.

---

## Python Basics

### Programs
- **Definitions**: Set up functions and values.
- **Commands**: Instructions for the interpreter to execute.
- Can be run via **interactive shell** or **script file**.

---

## Programming Environment: Anaconda
- **Editor**: For writing code (.py files)
- **Shell/Console**: For running code and seeing output

---

## Objects in Python

### Scalar (Atomic)
- `int`: Whole numbers (e.g., `5`, `-100`)
- `float`: Real numbers (e.g., `3.14`)
- `bool`: Boolean values (`True`, `False`)
- `NoneType`: Special object representing "nothing"

```python
type(5)        # int
type(3.0)      # float
type(True)     # bool
type(None)     # NoneType
```

### Non-Scalar (Structured)
- Strings: `"hello"`
- Lists, Dictionaries, etc.

---

## Type Conversions (Casting)
- `float(3)` → `3.0`
- `int(3.9)` → `3` *(truncates)*
- `round(3.9)` → `4`
```python
float(round(7.2))    # 7.0
int(7.9)             # 7
```

---

## Expressions
- Combine objects with operators:
```python
3 + 2              # 5 (int)
5 / 3              # 1.666... (float)
type((4+2)*6-1)    # int
```
- Python stores the result, not the expression.

### Operator Precedence
- `**` > `* / %` > `+ -`
- Use parentheses to control evaluation order.

---

## Arithmetic Operators Summary
| Operator | Description               |
|----------|---------------------------|
| `+`      | Addition                  |
| `-`      | Subtraction               |
| `*`      | Multiplication            |
| `/`      | Division (always float)  |
| `//`     | Floor division            |
| `%`      | Modulus (remainder)       |
| `**`     | Exponentiation            |
