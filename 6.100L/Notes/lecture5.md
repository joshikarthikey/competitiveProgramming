# 6.100L Lecture 5: Floats and Approximation Methods

## Motivation

```python
x = 0
for i in range(10):
    x += 0.1
print(x == 1)           # False
print(x, '==', 10*0.1)  # 0.9999999999999999 == 1.0
```

- Why? Because floats cannot always be represented exactly.

---

## Integers

- Binary representation of integers is straightforward.
- Can be handled using loops and modulus.

---

## Fractions in Binary

- Decimal: `0.abc = a*10^-1 + b*10^-2 + c*10^-3`
- Binary:  `0.abc = a*2^-1 + b*2^-2 + c*2^-3`

Example:  
`0.375 * 2^3 = 3` → Convert 3 to binary → `011`  
→ Binary: `0.011`

- Works if `x * 2^p` is a whole number.
- E.g., 3/8 works, 1/10 doesn't.

---

## Floating Point Representation

- Pair of integers: `(significant, exponent)`
  - (1, 1) → `1 * 2^1 = 2.0`
  - (1, -1) → `1 * 2^-1 = 0.5`
  - (125, -2) → `125 * 2^-2 = 31.25`

- Modern systems use 32-bit float (precision ≈ 10^-10)

---

## Problems with Float Comparisons

```python
x = 0
for i in range(10):
    x += 0.1
print(x == 1)  # False
```

### Moral:
**Never use `==` to compare floats.**  
Use: `abs(a - b) < epsilon`

---

## Approximation Methods

### Guess-and-check:
- Works for enumerable solutions.
- Limitation: slow and can't handle approximate results.

### Approximation Algorithm:
- Use a float increment.
- Stop when close enough (`|r^2 - x| < epsilon`)

```python
x = 36
epsilon = 0.01
guess = 0.0
increment = 0.0001
while abs(guess**2 - x) >= epsilon:
    guess += increment
print(guess)
```

### Parameters:
- `epsilon`: how close to target.
- `increment`: step size.

### Tradeoffs:
- Smaller increment = slower but more accurate.
- Larger epsilon = faster but less accurate.

---

## Overshooting Epsilon

- If `guess**2` overshoots `x`, loop doesn't exit.
- Fix: add a second condition to stop loop.

```python
while abs(guess**2 - x) >= epsilon and guess**2 <= x:
    ...
```

---

## Lessons Learned

- Don’t use `==` for floats.
- Always consider potential overshooting.
- Balance between performance and accuracy.

