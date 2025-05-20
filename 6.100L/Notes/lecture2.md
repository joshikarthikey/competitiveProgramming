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
