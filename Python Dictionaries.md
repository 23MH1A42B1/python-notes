# Python Dictionaries

thisdict = {  "brand": "Ford",  "model": "Mustang",  "year": 1964}

# Dictionary

Dictionaries are used to store data values in key:value pairs.

A dictionary is a collection which is ordered*, changeable and do not allow duplicates.

As of Python version 3.7, dictionaries are *ordered*. In Python 3.6 and earlier, dictionaries are *unordered*.

Dictionaries are written with curly brackets, and have keys and values:

# Example

Create and print a dictionary:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

output:

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

---

# Dictionary Items

Dictionary items are ordered, changeable, and do not allow duplicates.

Dictionary items are presented in key:value pairs, and can be referred to by using the key name.

# Example

Print the "brand" value of the dictionary:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict["brand"])
```

output:

Ford

---

# Ordered or Unordered?

As of Python version 3.7, dictionaries are *ordered*. In Python 3.6 and earlier, dictionaries are *unordered*.

When we say that dictionaries are ordered, it means that the items have a defined order, and that order will not change.

Unordered means that the items do not have a defined order, you cannot refer to an item by using an index.

---

# Changeable

Dictionaries are changeable, meaning that we can change, add or remove items after the dictionary has been created.

---

# Duplicates Not Allowed

Dictionaries cannot have two items with the same key:

# Example

Duplicate values will overwrite existing values:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(thisdict)
```

output:

{'brand': 'Ford', 'model': 'Mustang', 'year': 2020}

---

# Dictionary Length

To determine how many items a dictionary has, use the `len()` function:

# Example

Print the number of items in the dictionary:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(len(thisdict))
```

output:

3

---

# Dictionary Items - Data Types

The values in dictionary items can be of any data type:

# Example

String, int, boolean, and list data types:

```python
thisdict = {
  "brand": "Ford",
  "electric": False,
  "year": 1964,
  "colors": ["red", "white", "blue"]
}
```

---

# type()

From Python's perspective, dictionaries are defined as objects with the data type 'dict':

<class 'dict'>

---

# The dict() Constructor

It is also possible to use the dict() constructor to make a dictionary.

# Example

Using the dict() method to make a dictionary:

```python
thisdict = dict(name = "John", age = 36, country = "Norway")
print(thisdict)
```

output:

{'name': 'John', 'age': 36, 'country': 'Norway'}

---

# Accessing Items

You can access the items of a dictionary by referring to its key name, inside square brackets:

# Example

```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
print(x)

```

output:

Mustang

---

# Get Keys

The `keys()` method will return a list of all the keys in the dictionary.

# Example

Get a list of the keys:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = thisdict.keys()

print(x)
```

output:

dict_keys(['brand', 'model', 'year'])

---

# Get Values

The `values()` method will return a list of all the values in the dictionary.

# Example

Get a list of the values:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = thisdict.values()

print(x)

```

output:

dict_values(['Ford', 'Mustang', 1964])

---

# Get Items

The `items()` method will return each item in a dictionary, as tuples in a list.

# Example

Get a list of the key:value pairs

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = thisdict.items()

print(x)

```

output:

dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])

---

**Python - Change Dictionary Items**

# Change Values

You can change the value of a specific item by referring to its key name:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
```

---

# Update Dictionary

The `update()` method will update the dictionary with the items from the given argument.

The argument must be a dictionary, or an iterable object with key:value pairs.

# Example

Update the "year" of the car by using the `update()` method:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})

print(thisdict)

```

output:

{'brand': 'Ford', 'model': 'Mustang', 'year': 2020}

---

**Python - Add Dictionary Items**

# Adding Items

Adding an item to the dictionary is done by using a new index key and assigning a value to it:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
```

output:

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 'red'}

---

# Update Dictionary

The `update()` method will update the dictionary with the items from a given argument. If the item does not exist, the item will be added.

The argument must be a dictionary, or an iterable object with key:value pairs.

# Example

Add a color item to the dictionary by using the `update()` method:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"color": "red"})

print(thisdict)
```

output:

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 'red'}

---

# Removing Items

There are several methods to remove items from a dictionary:

# Example

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
print(thisdict)
```

output:

{'brand': 'Ford', 'year': 1964}

---

# Loop Through a Dictionary

You can loop through a dictionary by using a `for` loop.

When looping through a dictionary, the return value are the *keys* of the dictionary, but there are methods to return the *values* as well.

# Example

```python
thisdict =	{
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
for x in thisdict:
  print(x)
```

output:

brand

model

year

---

# Copy a Dictionary

You cannot copy a dictionary simply by typing `dict2 = dict1`, because: `dict2` will only be a *reference* to `dict1`, and changes made in `dict1` will automatically also be made in `dict2`.

There are ways to make a copy, one way is to use the built-in Dictionary method `copy()`.

# Example

Make a copy of a dictionary with the `copy()` method:

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = thisdict.copy()
print(mydict)
```

output:

{'brand': 'Ford', 'model': 'Mustang', 'year': 1964}

---

# Nested Dictionaries

A dictionary can contain dictionaries, this is called nested dictionaries.

# Example

```python
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}

print(myfamily)

```

output:

{'child1': {'name': 'Emil', 'year': 2004}, 'child2': {'name': 'Tobias', 'year': 2007}, 'child3': {'name': 'Linus', 'year': 2011}}

---

# Access Items in Nested Dictionaries

To access items from a nested dictionary, you use the name of the dictionaries, starting with the outer dictionary:

# Example

Print the name of child 2:

```python
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}

print(myfamily["child2"]["name"])
```

output:

Tobias

---

# Loop Through Nested Dictionaries

You can loop through a dictionary by using the `items()` method like this:

# Example

Loop through the keys and values of all nested dictionaries:

```python
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}

for x, obj in myfamily.items():
    print(x)
    
    for y in obj:
        print(y + ':', obj[y])

```

output:

```
child1
name: Emil
year: 2004
child2
name: Tobias
year: 2007
child3
name: Linus
year: 2011
```

---

# Dictionary Methods

Python has a set of built-in methods that you can use on dictionaries.

| Method | Description |
| --- | --- |
| [clear()](https://www.w3schools.com/python/ref_dictionary_clear.asp) | Removes all the elements from the dictionary |
| [copy()](https://www.w3schools.com/python/ref_dictionary_copy.asp) | Returns a copy of the dictionary |
| [fromkeys()](https://www.w3schools.com/python/ref_dictionary_fromkeys.asp) | Returns a dictionary with the specified keys and value |
| [get()](https://www.w3schools.com/python/ref_dictionary_get.asp) | Returns the value of the specified key |
| [items()](https://www.w3schools.com/python/ref_dictionary_items.asp) | Returns a list containing a tuple for each key value pair |
| [keys()](https://www.w3schools.com/python/ref_dictionary_keys.asp) | Returns a list containing the dictionary's keys |
| [pop()](https://www.w3schools.com/python/ref_dictionary_pop.asp) | Removes the element with the specified key |
| [popitem()](https://www.w3schools.com/python/ref_dictionary_popitem.asp) | Removes the last inserted key-value pair |
| [setdefault()](https://www.w3schools.com/python/ref_dictionary_setdefault.asp) | Returns the value of the specified key. If the key does not exist: insert the key, with the specified value |
| [update()](https://www.w3schools.com/python/ref_dictionary_update.asp) | Updates the dictionary with the specified key-value pairs |
| [values()](https://www.w3schools.com/python/ref_dictionary_values.asp) | Returns a list of all the values in the dictionary |