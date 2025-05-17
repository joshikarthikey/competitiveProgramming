# Introduction to Computer Science and Programming Using Python

## Types of Knowledge

| Type             | Description                            |
|------------------|----------------------------------------|
| Declarative      | Statements of fact                     |
| Imperative       | Step-by-step instructions ("how-to")   |

Programming involves writing imperative knowledge to compute facts.

---

## Algorithms

An **algorithm** is a finite sequence of well-defined instructions.

**Key properties:**
1. Sequence of simple steps.
2. Flow control to dictate execution order.
3. Clear stopping condition.

### Example: Square Root Approximation
| Step | Guess `g` | `g * g` | `x / g` | New Guess `(g + x/g)/2` |
|------|-----------|---------|---------|--------------------------|
| 1    | 3         | 9       | 5.33    | 4.17                     |
| 2    | 4.17      | 17.36   | 3.837   | 4.0035                   |
| 3    | 4.0035    | 16.0277 | 3.997   | 4.000002                 |

---

## Computer Fundamentals

**Stored Program Computer:**
- Executes a sequence of stored instructions.
- Instructions include arithmetic, logic, data movement, and control.

**Architecture Components:**
| Component              | Role                               |
|------------------------|------------------------------------|
| Memory                 | Stores data and instructions        |
| Arithmetic Logic Unit  | Performs operations                 |
| Control Unit           | Directs execution flow              |
| Input/Output           | Interacts with external environment |

---

## Programming Languages

| Concept             | Programming Analog        | Example                             |
|---------------------|---------------------------|-------------------------------------|
| Primitive Constructs| Numbers, Strings, Operators| `"hi"`, `5`, `+`, `*`               |
| Syntax              | Grammar rules              | `"hi"*5` is valid; `"hi"5` is not   |
| Static Semantics    | Meaningful combinations    | `"hi" + 5` is syntactically valid but semantically wrong |
| Semantics           | Actual behavior             | `"The chicken is ready to eat"` — context needed         |

---

## Python Objects

### Scalar Types

| Type      | Example Values     |
|-----------|--------------------|
| `int`     | 1, -100, 300       |
| `float`   | 3.14, -1.22, 0.0   |
| `bool`    | `True`, `False`    |
| `NoneType`| `None`             |

### Non-Scalar Types
- Strings: `"abc"`
- Lists, Dictionaries (covered later)

Use `type()` to inspect object type.

---

## Type Conversion

| Expression              | Result  | Type   |
|-------------------------|---------|--------|
| `float(123)`            | 123.0   | float  |
| `int(7.9)`              | 7       | int    |
| `round(3.9)`            | 4       | int    |
| `float(round(7.2))`     | 7.0     | float  |

---

## Expressions and Operators

| Expression        | Evaluated Value | Type   |
|------------------|------------------|--------|
| `3 + 2`           | 5                | int    |
| `(4 + 2) * 6 - 1` | 35               | int    |
| `5 / 3`           | 1.666...         | float  |

**Operators:**
- Arithmetic: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- Precedence: `**` > `* / %` > `+ -`

---

## Variables and Assignments

- Use `=` to bind a name to a value.
- Names reference single values at a time.

**Example:**
```python
pi = 355 / 113
radius = 2.2
area = pi * (radius ** 2)
circumference = pi * (radius * 2)
```

| Line                     | Result              |
|--------------------------|---------------------|
| `pi = 355 / 113`         | `pi ≈ 3.1415929`     |
| `radius = 2.2`           | `radius = 2.2`       |
| `area = pi * radius**2`  | Area of circle       |
| `circumference = pi * 2 * radius` | Circumference |

**Note:** Reassigning variables doesn’t update dependent ones unless re-evaluated.
