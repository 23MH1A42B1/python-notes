# Python Strings

# Strings

Strings in python are surrounded by either single quotation marks, or double quotation marks.

'hello' is the same as "hello".

You can display a string literal with the `print()` function:

# Example

```python
print("Hello")
print('Hello')
```

output:

Hello

Hello

---

# Quotes Inside Quotes

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

# Example

```python
print("It's alright")
print("He is called 'Johnny'")
print('He is called "Johnny"')
```

output:

It's alright

He is called 'Johnny'

He is called "Johnny"

---

# Assign String to a Variable

Assigning a string to a variable is done with the variable name followed by an equal sign and the string:

# Example

```python
a = "Hello"
print(a)
```

output:

Hello

---

# Multiline Strings

You can assign a multiline string to a variable by using three quotes:

# Example

You can use three double quotes:

```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```

output:

Lorem ipsum dolor sit amet,

consectetur adipiscing elit,

sed do eiusmod tempor incididunt

ut labore et dolore magna aliqua.

Or three single quotes:

# Example

```python
a = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''
print(a)
```

output:

Lorem ipsum dolor sit amet,

consectetur adipiscing elit,

sed do eiusmod tempor incididunt

ut labore et dolore magna aliqua.

---

**Note:** in the result, the line breaks are inserted at the same position as in the code.

---

# Strings are Arrays

Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters.

However, Python does not have a character data type, a single character is simply a string with a length of 1.

Square brackets can be used to access elements of the string.

# Example

Get the character at position 1 (remember that the first character has the position 0):

```python
a = "Hello, World!"
print(a[1])
```

output:

e

---

# Looping Through a String

Since strings are arrays, we can loop through the characters in a string, with a `for` loop.

# Example

Loop through the letters in the word "banana":

```python
for x in "banana":
  print(x)
```

output:

b

a

n

a

n

a

---

# String Length

To get the length of a string, use the `len()` function.

# Example

The `len()` function returns the length of a string:

```python
a = "Hello, World!"
print(len(a))
```

output:

13

---

# Check String

To check if a certain phrase or character is present in a string, we can use the keyword `in`.

# Example

Check if "free" is present in the following text:

```python
txt = "The best things in life are free!"
print("free" in txt)
```

output:

True

Use it in an `if` statement:

# Example

Print only if "free" is present:

```python
txt = "The best things in life are free!"
if "free" in txt:
  print("Yes, 'free' is present.")
```

output:

Yes, 'free' is present.

---

# Check if NOT

To check if a certain phrase or character is NOT present in a string, we can use the keyword `not in`.

# Example

Check if "expensive" is NOT present in the following text:

```python
txt = "The best things in life are free!"
print("expensive" not in txt)
```

output:

True

---

Use it in an `if` statement:

# Example

print only if "expensive" is NOT present:

```python
txt = "The best things in life are free!"
if "expensive" not in txt:
  print("No, 'expensive' is NOT present.")
```

output:

No, 'expensive' is NOT present.

---

# Slicing

You can return a range of characters by using the slice syntax.

Specify the start index and the end index, separated by a colon, to return a part of the string.

# Example

Get the characters from position 2 to position 5 (not included):

```python
b = "Hello, World!"
print(b[2:5])
```

output:

llo

---

**Note:** The first character has index 0.

---

# Slice From the Start

By leaving out the start index, the range will start at the first character:

# Example

Get the characters from the start to position 5 (not included):

```python
b = "Hello, World!"
print(b[:5])
```

output:

Hello

---

# Slice To the End

By leaving out the *end* index, the range will go to the end:

# Example

Get the characters from position 2, and all the way to the end:

```python
b = "Hello, World!"
print(b[2:])
```

---

# Negative Indexing

Use negative indexes to start the slice from the end of the string:

# Example

Get the characters:

From: "o" in "World!" (position -5)

To, but not included: "d" in "World!" (position -2):

```python
b = "Hello, World!"
print(b[-5:-2])
```

output:

orl

---

# **Python - Modify Strings**

Python has a set of built-in methods that you can use on strings.

---

# Upper Case

# Example

The `upper()` method returns the string in upper case:

```python
a = "Hello, World!"
print(a.upper())
```

output:

HELLO, WORLD!

---

# Lower Case

# Example

The `lower()` method returns the string in lower case:

```python
a = "Hello, World!"
print(a.lower())
```

output:

hello, world!

---

# Remove Whitespace

Whitespace is the space before and/or after the actual text, and very often you want to remove this space.

# Example

The `strip()` method removes any whitespace from the beginning or the end:

```python
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"
```

output:

Hello, World!

---

# Replace String

# Example

The `replace()` method replaces a string with another string:

```python
a = "Hello, World!"
print(a.replace("H", "J"))
```

output:

Jello, World!

---

# Split String

The `split()` method returns a list where the text between the specified separator becomes the list items.

# Example

The `split()` method splits the string into substrings if it finds instances of the separator:

```python
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']
```

output:

['Hello', ' World!']

---

# **Python - String Concatenation**

# String Concatenation

To concatenate, or combine, two strings you can use the + operator.

# Example

Merge variable `a` with variable `b` into variable `c`:

```python
a = "Hello"
b = "World"
c = a + b
print(c)
```

output:

HelloWorld

---

# Example

To add a space between them, add a `" "`:

```python
a = "Hello"
b = "World"
c = a + " " + b
print(c)
```

output:

Hello World

---

## **Python - Format - Strings**

# String Format

As we learned in the Python Variables chapter, we cannot combine strings and numbers like this:

# Example

```python
age = 36
txt = "My name is John, I am " + age
print(txt)

```

Traceback (most recent call last):

File "demo_string_format_error.py", line 2, in <module>

txt = "My name is John, I am " + age

TypeError: must be str, not int

But we can combine strings and numbers by using *f-strings* or the `format()` method!

---

# F-Strings

F-String was introduced in Python 3.6, and is now the preferred way of formatting strings.

To specify a string as an f-string, simply put an `f` in front of the string literal, and add curly brackets `{}` as placeholders for variables and other operations.

# Example

Create an f-string:

```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)
```

output:

My name is John, I am 36

---

# Placeholders and Modifiers

A placeholder can contain variables, operations, functions, and modifiers to format the value.

# Example

Add a placeholder for the `price` variable:

```python
price = 59
txt = f"The price is {price} dollars"
print(txt)
```

output:

The price is 59 dollars

---

A placeholder can include a *modifier* to format the value.

A modifier is included by adding a colon `:` followed by a legal formatting type, like `.2f` which means fixed point number with 2 decimals:

# Example

Display the price with 2 decimals:

```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)
```

output:

The price is 59.00 dollars

---

A placeholder can contain Python code, like math operations:

# Example

Perform a math operation in the placeholder, and return the result:

```python
txt = f"The price is {20 * 59} dollars"
print(txt)
```

output:

The price is 1180 dollars

---

## **Python - Escape Characters**

# Escape Character

To insert characters that are illegal in a string, use an escape character.

An escape character is a backslash `\` followed by the character you want to insert.

An example of an illegal character is a double quote inside a string that is surrounded by double quotes:

# Example

You will get an error if you use double quotes inside a string that is surrounded by double quotes:

```python
txt = "We are the so-called "Vikings" from the north."
```

output:

File "demo_string_escape_error.py", line 1

txt = "We are the so-called "Vikings" from the north."

^

SyntaxError: invalid syntax

---

To fix this problem, use the escape character `\"`:

# Example

The escape character allows you to use double quotes when you normally would not be allowed:

```python
txt = "We are the so-called \"Vikings\" from the north."
```

output:

We are the so-called "Vikings" from the north.

---

# Escape Characters

Other escape characters used in Python:

| Code | Result | Try it |
| --- | --- | --- |
| \' | Single Quote | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_escape2) |
| \\ | Backslash | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_backslash) |
| \n | New Line | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_newline) |
| \r | Carriage Return | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_r) |
| \t | Tab | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_t) |
| \b | Backspace | [Try it »](https://www.w3schools.com/python/showpython.asp?filename=demo_string_b) |
| \f | Form Feed |  |
| \ooo | Octal value | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_octal) |
| \xhh | Hex value | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_string_hex) |

---

# String Methods

Python has a set of built-in methods that you can use on strings.

**Note:** All string methods return new values. They do not change the original string.

| Method | Description |
| --- | --- |
| [capitalize()](https://www.w3schools.com/python/ref_string_capitalize.asp) | Converts the first character to upper case |
| [casefold()](https://www.w3schools.com/python/ref_string_casefold.asp) | Converts string into lower case |
| [center()](https://www.w3schools.com/python/ref_string_center.asp) | Returns a centered string |
| [count()](https://www.w3schools.com/python/ref_string_count.asp) | Returns the number of times a specified value occurs in a string |
| [encode()](https://www.w3schools.com/python/ref_string_encode.asp) | Returns an encoded version of the string |
| [endswith()](https://www.w3schools.com/python/ref_string_endswith.asp) | Returns true if the string ends with the specified value |
| [expandtabs()](https://www.w3schools.com/python/ref_string_expandtabs.asp) | Sets the tab size of the string |
| [find()](https://www.w3schools.com/python/ref_string_find.asp) | Searches the string for a specified value and returns the position of where it was found |
| [format()](https://www.w3schools.com/python/ref_string_format.asp) | Formats specified values in a string |
| format_map() | Formats specified values in a string |
| [index()](https://www.w3schools.com/python/ref_string_index.asp) | Searches the string for a specified value and returns the position of where it was found |
| [isalnum()](https://www.w3schools.com/python/ref_string_isalnum.asp) | Returns True if all characters in the string are alphanumeric |
| [isalpha()](https://www.w3schools.com/python/ref_string_isalpha.asp) | Returns True if all characters in the string are in the alphabet |
| [isascii()](https://www.w3schools.com/python/ref_string_isascii.asp) | Returns True if all characters in the string are ascii characters |
| [isdecimal()](https://www.w3schools.com/python/ref_string_isdecimal.asp) | Returns True if all characters in the string are decimals |
| [isdigit()](https://www.w3schools.com/python/ref_string_isdigit.asp) | Returns True if all characters in the string are digits |
| [isidentifier()](https://www.w3schools.com/python/ref_string_isidentifier.asp) | Returns True if the string is an identifier |
| [islower()](https://www.w3schools.com/python/ref_string_islower.asp) | Returns True if all characters in the string are lower case |
| [isnumeric()](https://www.w3schools.com/python/ref_string_isnumeric.asp) | Returns True if all characters in the string are numeric |
| [isprintable()](https://www.w3schools.com/python/ref_string_isprintable.asp) | Returns True if all characters in the string are printable |
| [isspace()](https://www.w3schools.com/python/ref_string_isspace.asp) | Returns True if all characters in the string are whitespaces |
| [istitle()](https://www.w3schools.com/python/ref_string_istitle.asp) | Returns True if the string follows the rules of a title |
| [isupper()](https://www.w3schools.com/python/ref_string_isupper.asp) | Returns True if all characters in the string are upper case |
| [join()](https://www.w3schools.com/python/ref_string_join.asp) | Joins the elements of an iterable to the end of the string |
| [ljust()](https://www.w3schools.com/python/ref_string_ljust.asp) | Returns a left justified version of the string |
| [lower()](https://www.w3schools.com/python/ref_string_lower.asp) | Converts a string into lower case |
| [lstrip()](https://www.w3schools.com/python/ref_string_lstrip.asp) | Returns a left trim version of the string |
| [maketrans()](https://www.w3schools.com/python/ref_string_maketrans.asp) | Returns a translation table to be used in translations |
| [partition()](https://www.w3schools.com/python/ref_string_partition.asp) | Returns a tuple where the string is parted into three parts |
| [replace()](https://www.w3schools.com/python/ref_string_replace.asp) | Returns a string where a specified value is replaced with a specified value |
| [rfind()](https://www.w3schools.com/python/ref_string_rfind.asp) | Searches the string for a specified value and returns the last position of where it was found |
| [rindex()](https://www.w3schools.com/python/ref_string_rindex.asp) | Searches the string for a specified value and returns the last position of where it was found |
| [rjust()](https://www.w3schools.com/python/ref_string_rjust.asp) | Returns a right justified version of the string |
| [rpartition()](https://www.w3schools.com/python/ref_string_rpartition.asp) | Returns a tuple where the string is parted into three parts |
| [rsplit()](https://www.w3schools.com/python/ref_string_rsplit.asp) | Splits the string at the specified separator, and returns a list |
| [rstrip()](https://www.w3schools.com/python/ref_string_rstrip.asp) | Returns a right trim version of the string |
| [split()](https://www.w3schools.com/python/ref_string_split.asp) | Splits the string at the specified separator, and returns a list |
| [splitlines()](https://www.w3schools.com/python/ref_string_splitlines.asp) | Splits the string at line breaks and returns a list |
| [startswith()](https://www.w3schools.com/python/ref_string_startswith.asp) | Returns true if the string starts with the specified value |
| [strip()](https://www.w3schools.com/python/ref_string_strip.asp) | Returns a trimmed version of the string |
| [swapcase()](https://www.w3schools.com/python/ref_string_swapcase.asp) | Swaps cases, lower case becomes upper case and vice versa |
| [title()](https://www.w3schools.com/python/ref_string_title.asp) | Converts the first character of each word to upper case |
| [translate()](https://www.w3schools.com/python/ref_string_translate.asp) | Returns a translated string |
| [upper()](https://www.w3schools.com/python/ref_string_upper.asp) | Converts a string into upper case |
| [zfill()](https://www.w3schools.com/python/ref_string_zfill.asp) | Fills the string with a specified number of 0 values at the beginning |

---