# Lecture 4: Loops over Strings, Guess-and-Check, Binary

## `break` Statement
- Exits the innermost loop immediately
- Skips remaining code in the block

**Example**:
```python
mysum = 0
for i in range(5, 11, 2):
    mysum += i
    if mysum == 5:
        break
    mysum += 1
print(mysum)
```

---

## Strings and Loops

**Check for 'i' or 'u' in a string**:
```python
s = "demo loops - fruit loops"
for char in s:
    if char in 'iu':
        print("There is an i or u")
```

---

## Guess-and-Check
- Use exhaustive enumeration
- Make a guess → Check it → Stop if found or continue

### Square Root Example
```python
x = int(input("Enter an integer: "))
guess = 0
while guess**2 < x:
    guess += 1
if guess**2 == x:
    print("Square root of", x, "is", guess)
else:
    print(x, "is not a perfect square")
```

### Handling Negative Input
```python
x = int(input("Enter a positive integer: "))
neg_flag = False
if x < 0:
    neg_flag = True
    x = -x
# Continue as above...
```

---

## Boolean Flags
Use Booleans like `found = False` to signal outcomes.

---

## Cube Root Example

### Positive Only:
```python
cube = int(input("Enter an integer: "))
for guess in range(cube+1):
    if guess**3 == cube:
        print("Cube root is", guess)
```

### Positive and Negative:
```python
cube = int(input("Enter an integer: "))
for guess in range(abs(cube)+1):
    if guess**3 == abs(cube):
        if cube < 0:
            guess = -guess
        print("Cube root is", guess)
```

---

## Word Problem Example
Alyssa, Ben, Cindy sell tickets:
```python
for alyssa in range(11):
    for ben in range(11):
        for cindy in range(11):
            if (alyssa + ben + cindy == 10 and 
                ben == alyssa - 2 and 
                cindy == 2 * alyssa):
                print(f"Alyssa: {alyssa}, Ben: {ben}, Cindy: {cindy}")
```

---

## More Efficient Solution
```python
for alyssa in range(1001):
    ben = max(alyssa - 20, 0)
    cindy = alyssa * 2
    if alyssa + ben + cindy == 1000:
        print(f"Alyssa: {alyssa}, Ben: {ben}, Cindy: {cindy}")
```

---

## Binary Numbers

### Motivation
```python
x = 0
for i in range(10):
    x += 0.1
print(x == 1)  # False due to float error
```

- Floating point operations introduce small errors.

---

## Decimal to Binary Conversion
```python
num = 1507
result = ''
if num == 0:
    result = '0'
while num > 0:
    result = str(num % 2) + result
    num = num // 2
print(result)
```

### Handling Negative Numbers
```python
is_neg = False
if num < 0:
    is_neg = True
    num = abs(num)
# Continue as above...
if is_neg:
    result = '-' + result
```
