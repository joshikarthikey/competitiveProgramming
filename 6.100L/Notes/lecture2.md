# 6.100L Lecture 2: Strings, Input/Output, and Branching

## Strings
- Strings are sequences of characters, case-sensitive.
- Enclosed in single `'` or double `"` quotes.
- Can be concatenated (`+`) or repeated (`*`).

```python
a = "me"
b = "myself"
c = a + b          # "memyself"
d = a + " " + b    # "me myself"
silly = a * 3      # "mememe"
```
---

## String Operations
- `len(s)` gives the length of a string.
- Indexing with `s[i]`, supports negative indices.
- Slicing: `s[start:stop:step]`
- Strings are **immutable**.

```python
s = "abc"
s[::-1]  # reverse string
```

---

## Slicing to Get a Substring

- Strings can be sliced using the syntax: `string[start:stop:step]`
- This retrieves characters starting at `start`, up to but **not including** `stop`, taking every `step` character.
- If only `[start:stop]` is provided, `step` defaults to `1`.
- If only one number is given, it's just indexing a single character.
- You can omit any of the three values:
  - `s[:]` gives the entire string.
  - `s[::-1]` gives the reversed string.

### Example

```python
s = "abcdefgh"

# Index positions:
#  Forward:  0  1  2  3  4  5  6  7
#  Reverse: -8 -7 -6 -5 -4 -3 -2 -1

s[3:6]      # 'def'        (from index 3 to 5)
s[3:6:2]    # 'df'         (from index 3 to 5, skipping every other)
s[:]        # 'abcdefgh'   (entire string)
s[::-1]     # 'hgfedcba'   (reversed string)
s[4:1:-2]   # 'ec'         (from index 4 to 2, stepping -2)
```

---

## Input/Output
### Printing
```python
print("Hello", 123)                  # Output: Hello 123
print("The number is " + str(5))     # Concatenation
```

### Input
```python
x = input("Enter something: ")       # Always returns a string
y = int(input("Enter a number: "))   # Cast to int
```

## Newton's Method (Cube Root Approximation)
```python
x = int(input('Find cube root of: '))
g = int(input('Initial guess: '))
next_g = g - ((g**3 - x) / (3 * g**2))
```

---

## f-Strings (Python 3.6+)
```python
name = "Ana"
print(f"Hello, {name}!")
```

---

## Branching
### Comparison Operators
- `==`, `!=`, `<`, `>`, `<=`, `>=`

### Logical Operators
- `not`, `and`, `or`

### if/elif/else
```python
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

### Nested Branching & Indentation
```python
if x == y:
    if y != 0:
        print("x / y =", x/y)
```
