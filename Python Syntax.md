# Python Syntax

# Execute Python Syntax

As we learned in the previous page, Python syntax can be executed by writing directly in the Command Line:

>>> print("Hello, World!")Hello, World!

Or by creating a python file on the server, using the .py file extension, and running it in the Command Line:

C:\Users\*Your Name*>python myfile.py

# Python Indentation

Indentation refers to the spaces at the beginning of a code line.

Where in other programming languages the indentation in code is for readability only, the indentation in Python is very important.

Python uses indentation to indicate a block of code.

# Example [Get your own Python Server](https://www.w3schools.com/python/python_server.asp)

[Try it Yourself »](https://www.w3schools.com/python/trypython.asp?filename=demo_indentation)

```python
if 5 > 2:  print("Five is greater than two!")
```

output:  Five is greater than two!

---

Python will give you an error if you skip the indentation:

# Example

Syntax Error:

[Try it Yourself »](https://www.w3schools.com/python/trypython.asp?filename=demo_indentation_test)

```python
if 5 > 2:print("Five is greater than two!")
```

output:

File "demo_indentation_test.py", line 2

print("Five is greater than two!")

^

IndentationError: expected an indented block

---

The number of spaces is up to you as a programmer, the most common use is four, but it has to be at least one.

# Example

```python
if 5 > 2:
 print("Five is greater than two!") 
if 5 > 2:
        print("Five is greater than two!") 
```

output: 

Five is greater than two!

Five is greater than two!

[Try it Yourself »](https://www.w3schools.com/python/trypython.asp?filename=demo_indentation2)

---

You have to use the same number of spaces in the same block of code, otherwise Python will give you an error:

# Example

Syntax Error:

```python
if 5 > 2:
 print("Five is greater than two!")
        print("Five is greater than two!")
```

output: 

File "demo_indentation2_error.py", line 3

print("Five is greater than two!")

^

IndentationError: unexpected indent

[Try it Yourself »](https://www.w3schools.com/python/trypython.asp?filename=demo_indentation2_error)

---

# Python Variables

In Python, variables are created when you assign a value to it:

# Example

Variables in Python:

[Try it Yourself »](https://www.w3schools.com/python/trypython.asp?filename=demo_syntax_variables)

```python
x = 5
y = "Hello, World!"
```

output :

5

Hello, World!

---

# Comments

Python has commenting capability for the purpose of in-code documentation.

Comments start with a #, and Python will render the rest of the line as a comment:

# Example

Comments in Python:

[Try it Yourself »](https://www.w3schools.com/python/trypython.asp?filename=demo_comment)

```python
#This is a comment.
print("Hello, World!")
```

output: Hello, World!

---

🐍