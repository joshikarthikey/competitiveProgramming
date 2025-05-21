# Lecture 3: Iteration 

## Zelda, Lost Woods Example
- Repeating a choice like “go right” keeps you in the loop.
- Must change direction to exit.
- Demonstrated using `if` and `while`.

## While Loops
- Repeats code block while a condition is `True`.
- If the condition never becomes `False`, creates an infinite loop.

```python
while <condition>:
    <code>
```

## Examples
```python
# Lost Forest example
where = input("Go left or right? ")
while where == "right":
    where = input("Go left or right? ")
print("You got out!")

# Countdown
n = int(input("Enter a non-negative integer: "))
while n > 0:
    print('x')
    n -= 1
```

## Infinite Loop Example
```python
while True:
    print("noooooo")
```

## Counter Example
Expand Lost Forest example with a counter to show a sad face if entered loop more than 2 times.

## For Loops
- Iterates through a sequence of values.

```python
for <variable> in <sequence>:
    <code>
```

## Range Function
- `range(start, stop, step)`
- `start` defaults to 0, `step` to 1

```python
for i in range(5):         # 0 to 4
for i in range(1, 4, 1):   # 1 to 3
for i in range(4, 0, -1):  # 4 to 1
```

## Running Sum Example
```python
mysum = 0
for i in range(10):
    mysum += i
print(mysum)
```

## Factorial Examples
```python
# While loop
x = 4
i = 1
factorial = 1
while i <= x:
    factorial *= i
    i += 1
print(f'{x} factorial is {factorial}')

# For loop
x = 4
factorial = 1
for i in range(1, x+1):
    factorial *= i
print(f'{x} factorial is {factorial}')
```
