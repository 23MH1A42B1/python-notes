# Python Numbers

# Python Numbers

There are three numeric types in Python:

- `int`
- `float`
- `complex`

Variables of numeric types are created when you assign a value to them:

# Example

```python
x = 1    # int
y = 2.8  # float
z = 1j   # complex
```

To verify the type of any object in Python, use the `type()` function:

# Example

```python
print(type(x))
print(type(y))
print(type(z))
```

output:

<class 'int'>

<class 'float'>

<class 'complex'>

# Int

Int, or integer, is a whole number, positive or negative, without decimals, of unlimited length.

# Example

Integers:

```python
x = 1
y = 35656222554887711
z = -3255522

print(type(x))
print(type(y))
print(type(z))
```

output:

<class 'int'>

<class 'int'>

<class 'int'>

# Float

Float, or "floating point number" is a number, positive or negative, containing one or more decimals.

# Example

Floats:

```python
x = 1.10
y = 1.0
z = -35.59

print(type(x))
print(type(y))
print(type(z))
```

output:

<class 'float'>

<class 'float'>

<class 'float'>

Float can also be scientific numbers with an "e" to indicate the power of 10.

# Example

Floats:

```python
x = 35e3
y = 12E4
z = -87.7e100

print(type(x))
print(type(y))
print(type(z))
```

output:

<class 'float'>

<class 'float'>

<class 'float'>

---

# Complex

Complex numbers are written with a "j" as the imaginary part:

# Example

Complex:

```python
x = 3+5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(z))
```

output:

<class 'complex'>

<class 'complex'>

<class 'complex'>

---

# Type Conversion

You can convert from one type to another with the `int()`, `float()`, and `complex()` methods:

# Example

Convert from one type to another:

```python
x = 1    # int
y = 2.8  # float
z = 1j   # complex

#convert from int to float:
a = float(x)

#convert from float to int:
b = int(y)

#convert from int to complex:
c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
```

output:

1.0

2

(1+0j)

<class 'float'>

<class 'int'>

<class 'complex'>

**Note:** You cannot convert complex numbers into another number type.

---

# Random Number

Python does not have a `random()` function to make a random number, but Python has a built-in module called `random` that can be used to make random numbers:

# Example

Import the random module, and display a random number between 1 and 9:

```python
import random

print(random.randrange(1, 10))
```

output: 4

---

🐍