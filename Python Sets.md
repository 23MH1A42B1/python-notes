# Python Sets

myset = {"apple", "banana", "cherry"}

---

# Set

Sets are used to store multiple items in a single variable.

Set is one of 4 built-in data types in Python used to store collections of data, the other 3 are [List](https://www.w3schools.com/python/python_lists.asp), [Tuple](https://www.w3schools.com/python/python_tuples.asp), and [Dictionary](https://www.w3schools.com/python/python_dictionaries.asp), all with different qualities and usage.

A set is a collection which is *unordered*, *unchangeable**, and *unindexed*.

- **Note:** Set *items* are unchangeable, but you can remove items and add new items.

Sets are written with curly brackets.

# Example[Get your own Python Server](https://www.w3schools.com/python/python_server.asp)

Create a Set:

```python
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

output:

{'banana', 'cherry', 'apple'}

---

**Note:** Sets are unordered, so you cannot be sure in which order the items will appear.

---

# Set Items

Set items are unordered, unchangeable, and do not allow duplicate values.

---

# Unordered

Unordered means that the items in a set do not have a defined order.

Set items can appear in a different order every time you use them, and cannot be referred to by index or key.

---

# Unchangeable

Set items are unchangeable, meaning that we cannot change the items after the set has been created.

Once a set is created, you cannot change its items, but you can remove items and add new items.

---

# Duplicates Not Allowed

Sets cannot have two items with the same value.

# Example

Duplicate values will be ignored:

```python
thisset = {"apple", "banana", "cherry", "apple"}

print(thisset)
```

output:

{'banana', 'cherry', 'apple'}

---

**Note:** The values `True` and `1` are considered the same value in sets, and are treated as duplicates:

# Example

`True` and `1` is considered the same value:

```python
thisset = {"apple", "banana", "cherry", True, 1, 2}

print(thisset)
```

output:

{True, 2, 'banana', 'cherry', 'apple'}

---

**Note:** The values `False` and `0` are considered the same value in sets, and are treated as duplicates:

# Example

`False` and `0` is considered the same value:

```python
thisset = {"apple", "banana", "cherry", False, True, 0}

print(thisset)
```

output:

{False, True, 'cherry', 'apple', 'banana'}

---

# Get the Length of a Set

To determine how many items a set has, use the `len()` function.

# Example

Get the number of items in a set:

```python
thisset = {"apple", "banana", "cherry"}

print(len(thisset))

```

output:

3

---

# Set Items - Data Types

Set items can be of any data type:

# Example

String, int and boolean data types:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {1, 5, 7, 9, 3}
set3 = {True, False, False}
```

---

A set can contain different data types:

# Example

A set with strings, integers and boolean values:

```python
set1 = {"abc", 34, True, 40, "male"}
```

---

# type()

From Python's perspective, sets are defined as objects with the data type 'set':

<class 'set'>

# Example

What is the data type of a set?

```python
myset = {"apple", "banana", "cherry"}
print(type(myset))
```

output:

<class 'set'>

---

# The set() Constructor

It is also possible to use the set() constructor to make a set.

# Example

Using the set() constructor to make a set:

```python
thisset = set(("apple", "banana", "cherry")) # note the double round-bracketsprint(thisset)
print(thisset)
```

output:

{'cherry', 'apple', 'banana'}

---

# Python Collections (Arrays)

There are four collection data types in the Python programming language:

- [**List**](https://www.w3schools.com/python/python_lists.asp) is a collection which is ordered and changeable. Allows duplicate members.
- [**Tuple**](https://www.w3schools.com/python/python_tuples.asp) is a collection which is ordered and unchangeable. Allows duplicate members.
- **Set** is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.
- [**Dictionary**](https://www.w3schools.com/python/python_dictionaries.asp) is a collection which is ordered** and changeable. No duplicate members.
- Set *items* are unchangeable, but you can remove items and add new items.
- *As of Python version 3.7, dictionaries are *ordered*. In Python 3.6 and earlier, dictionaries are *unordered*.

---

# **Python - Access Set Items**

# Access Items

You cannot access items in a set by referring to an index or a key.

But you can loop through the set items using a `for` loop, or ask if a specified value is present in a set, by using the `in` keyword.

# Example

Loop through the set, and print the values:

```python
thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)
```

output:

banana

apple

cherry

---

# Example

Check if "banana" is present in the set:

```python
thisset = {"apple", "banana", "cherry"}

print("banana" in thisset)
```

output:

True

---

# Example

Check if "banana" is NOT present in the set:

```python
thisset = {"apple", "banana", "cherry"}

print("banana" not in thisset)
```

output:

False

---

# Change Items

Once a set is created, you cannot change its items, but you can add new items.

---

# **Python - Add Set Items**

# Add Items

Once a set is created, you cannot change its items, but you can add new items.

To add one item to a set use the `add()` method.

# Example

Add an item to a set, using the `add()` method:

```python
thisset = {"apple", "banana", "cherry"}

thisset.add("orange")

print(thisset)
```

output:

{'cherry', 'orange', 'apple', 'banana'}

---

# Add Sets

To add items from another set into the current set, use the `update()` method.

# Example

Add elements from `tropical` into `thisset`:

```python
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical)

print(thisset)
```

output:

{'apple', 'mango', 'cherry', 'pineapple', 'banana', 'papaya'}

---

# Add Any Iterable

The object in the `update()` method does not have to be a set, it can be any iterable object (tuples, lists, dictionaries etc.).

# Example

Add elements of a list to at set:

```python
thisset = {"apple", "banana", "cherry"}
mylist = ["kiwi", "orange"]

thisset.update(mylist)

print(thisset)
```

output:

{'banana', 'cherry', 'apple', 'orange', 'kiwi'}

---

# **Python - Remove Set Items**

# Remove Item

To remove an item in a set, use the `remove()`, or the `discard()` method.

# Example

Remove "banana" by using the `remove()` method:

```python
thisset = {"apple", "banana", "cherry"}

thisset.remove("banana")

print(thisset)
```

output:

{'cherry', 'apple'}

---

**Note:** If the item to remove does not exist, `remove()` will raise an error.

# Example

Remove "banana" by using the `discard()` method:

```python
thisset = {"apple", "banana", "cherry"}

thisset.discard("banana")

print(thisset)
```

output:

{'apple', 'cherry'}

---

**Note:** If the item to remove does not exist, `discard()` will **NOT** raise an error.

You can also use the `pop()` method to remove an item, but this method will remove a random item, so you cannot be sure what item that gets removed.

The return value of the `pop()` method is the removed item.

# Example

Remove a random item by using the `pop()` method:

```python
thisset = {"apple", "banana", "cherry"}

x = thisset.pop()

print(x)

print(thisset)
```

output:

banana

{'cherry', 'apple'}

---

**Note:** Sets are *unordered*, so when using the `pop()` method, you do not know which item that gets removed.

# Example

The `clear()` method empties the set:

```python
thisset = {"apple", "banana", "cherry"}

thisset.clear()

print(thisset)
```

output:

set()

---

# Example

The `del` keyword will delete the set completely:

```python
thisset = {"apple", "banana", "cherry"}

del thisset

print(thisset)
```

output:

Traceback (most recent call last):

File "demo_set_del.py", line 5, in <module>

print(thisset) #this will raise an error because the set no longer exists

NameError: name 'thisset' is not defined

---

# **Python - Loop Sets**

# Loop Items

You can loop through the set items by using a `for` loop:

# Example

```python
thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)
```

output:

cherry

banana

apple

---

# **Python - Join Sets**

# Join Sets

There are several ways to join two or more sets in Python.

The `union()` and `update()` methods joins all items from both sets.

The `intersection()` method keeps ONLY the duplicates.

The `difference()` method keeps the items from the first set that are not in the other set(s).

The `symmetric_difference()` method keeps all items EXCEPT the duplicates.

---

# Union

The `union()` method returns a new set with all items from both sets.

# Example

Join set1 and set2 into a new set:

```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}

set3 = set1.union(set2)
print(set3)
```

output:

{'a', 3, 2, 'c', 1, 'b'}

---

You can use the `|` operator instead of the `union()` method, and you will get the same result.

# Example

Use `|` to join two sets:

```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}

set3 = set1 | set2
print(set3)
```

output:

{'a', 'b', 'c', 1, 3, 2}

---

# Join Multiple Sets

All the joining methods and operators can be used to join multiple sets.

When using a method, just add more sets in the parentheses, separated by commas:

# Example

Join multiple sets with the `union()` method:

```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = {"John", "Elena"}
set4 = {"apple", "bananas", "cherry"}

myset = set1.union(set2, set3, set4)
print(myset)
```

output:

{cherry, apple, 'c', John, banana, 3, 'b', Elena, 1, 2, 'a'}

---

When using the `|` operator, separate the sets with more `|` operators:

# Example

Use `|` to join two sets:

```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = {"John", "Elena"}
set4 = {"apple", "bananas", "cherry"}

myset = set1 | set2 | set3 |set4
print(myset)
```

output:

{Elena, 3, 'b', 'a', apple, 'c', John, 2, banana, cherry, 1}

---

# Join a Set and a Tuple

The `union()` method allows you to join a set with other data types, like lists or tuples.

The result will be a set.

# Example

Join a set with a tuple:

```python
x = {"a", "b", "c"}
y = (1, 2, 3)

z = x.union(y)
print(z)
```

output:

{'b', 'c', 'a', 3, 1, 2}

---

**Note:** The  `|` operator only allows you to join sets with sets, and not with other data types like you can with the  `union()` method.

---

# Update

The `update()` method inserts all items from one set into another.

The `update()` changes the original set, and does not return a new set.

# Example

The `update()` method inserts the items in set2 into set1:

```python
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set1.update(set2)
print(set1)
```

output:

{'b', 'c', 'a', 1, 3, 2}

---

**Note:** Both `union()` and `update()` will exclude any duplicate items.

---

# Intersection

Keep ONLY the duplicates

The `intersection()` method will return a new set, that only contains the items that are present in both sets.

# Example

Join set1 and set2, but keep only the duplicates:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set3 = set1.intersection(set2)
print(set3)
```

output:
{’apple’}

---

You can use the `&` operator instead of the `intersection()` method, and you will get the same result.

# Example

Use `&` to join two sets:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set3 = set1 & set2
print(set3)
```

output:

{'apple'}

---

**Note:** The `&` operator only allows you to join sets with sets, and not with other data types like you can with the `intersection()` method.

The `intersection_update()` method will also keep ONLY the duplicates, but it will change the original set instead of returning a new set.

# Example

Keep the items that exist in both `set1`, and `set2`:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set1.intersection_update(set2)

print(set1)
```

output:

{'apple'}

---

The values `True` and `1` are considered the same value. The same goes for `False` and `0`.

# Example

Join sets that contains the values `True`, `False`, `1`, and `0`, and see what is considered as duplicates:

```python
set1 = {"apple", 1,  "banana", 0, "cherry"}
set2 = {False, "google", 1, "apple", 2, True}

set3 = set1.intersection(set2)

print(set3)
```

output:

{False, True, 'apple'}

---

# Difference

The `difference()` method will return a new set that will contain only the items from the first set that are not present in the other set.

# Example

Keep all items from set1 that are not in set2:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set3 = set1.difference(set2)

print(set3)
```

output:

{'banana', 'cherry'}

---

You can use the `-` operator instead of the `difference()` method, and you will get the same result.

# Example

Use `-` to join two sets:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set3 = set1 - set2
print(set3)
```

output:

{'banana', 'cherry'}

---

**Note:** The `-` operator only allows you to join sets with sets, and not with other data types like you can with the `difference()` method.

The `difference_update()` method will also keep the items from the first set that are not in the other set, but it will change the original set instead of returning a new set.

# Example

Use the `difference_update()` method to keep the items that are not present in both sets:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set1.difference_update(set2)

print(set1)
```

output:

{'banana', 'cherry'}

---

# Symmetric Differences

The `symmetric_difference()` method will keep only the elements that are NOT present in both sets.

# Example

Keep the items that are not present in both sets:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set3 = set1.symmetric_difference(set2)

print(set3)
```

output:
{'google', 'banana', 'microsoft', 'cherry'}

---

You can use the `^` operator instead of the `symmetric_difference()` method, and you will get the same result.

# Example

Use `^` to join two sets:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set3 = set1 ^ set2
print(set3)
```

output:

{'google', 'banana', 'microsoft', 'cherry'}

---

**Note:** The `^` operator only allows you to join sets with sets, and not with other data types like you can with the `symmetric_difference()` method.

The `symmetric_difference_update()` method will also keep all but the duplicates, but it will change the original set instead of returning a new set.

# Example

Use the `symmetric_difference_update()` method to keep the items that are not present in both sets:

```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}

set1.symmetric_difference_update(set2)

print(set1)
```

output:

{'google', 'banana', 'microsoft', 'cherry'}

---

# Set Methods

Python has a set of built-in methods that you can use on sets.

| Method | Shortcut | Description |
| --- | --- | --- |
| [add()](https://www.w3schools.com/python/ref_set_add.asp) |  | Adds an element to the set |
| [clear()](https://www.w3schools.com/python/ref_set_clear.asp) |  | Removes all the elements from the set |
| [copy()](https://www.w3schools.com/python/ref_set_copy.asp) |  | Returns a copy of the set |
| [difference()](https://www.w3schools.com/python/ref_set_difference.asp) | [`-`](https://www.w3schools.com/python/ref_set_difference.asp) | Returns a set containing the difference between two or more sets |
| [difference_update()](https://www.w3schools.com/python/ref_set_difference_update.asp) | [`-=`](https://www.w3schools.com/python/ref_set_difference_update.asp) | Removes the items in this set that are also included in another, specified set |
| [discard()](https://www.w3schools.com/python/ref_set_discard.asp) |  | Remove the specified item |
| [intersection()](https://www.w3schools.com/python/ref_set_intersection.asp) | [`&`](https://www.w3schools.com/python/ref_set_intersection.asp) | Returns a set, that is the intersection of two other sets |
| [intersection_update()](https://www.w3schools.com/python/ref_set_intersection_update.asp) | [`&=`](https://www.w3schools.com/python/ref_set_intersection_update.asp) | Removes the items in this set that are not present in other, specified set(s) |
| [isdisjoint()](https://www.w3schools.com/python/ref_set_isdisjoint.asp) |  | Returns whether two sets have a intersection or not |
| [issubset()](https://www.w3schools.com/python/ref_set_issubset.asp) | [`<=`](https://www.w3schools.com/python/ref_set_issubset.asp) | Returns whether another set contains this set or not |
|  | [`<`](https://www.w3schools.com/python/ref_set_issubset.asp) | Returns whether all items in this set is present in other, specified set(s) |
| [issuperset()](https://www.w3schools.com/python/ref_set_issuperset.asp) | [`>=`](https://www.w3schools.com/python/ref_set_issuperset.asp) | Returns whether this set contains another set or not |
|  | [`>`](https://www.w3schools.com/python/ref_set_issuperset.asp) | Returns whether all items in other, specified set(s) is present in this set |
| [pop()](https://www.w3schools.com/python/ref_set_pop.asp) |  | Removes an element from the set |
| [remove()](https://www.w3schools.com/python/ref_set_remove.asp) |  | Removes the specified element |
| [symmetric_difference()](https://www.w3schools.com/python/ref_set_symmetric_difference.asp) | [`^`](https://www.w3schools.com/python/ref_set_symmetric_difference.asp) | Returns a set with the symmetric differences of two sets |
| [symmetric_difference_update()](https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp) | [`^=`](https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp) | Inserts the symmetric differences from this set and another |
| [union()](https://www.w3schools.com/python/ref_set_union.asp) | [`|`](https://www.w3schools.com/python/ref_set_union.asp) | Return a set containing the union of sets |
| [update()](https://www.w3schools.com/python/ref_set_update.asp) | [`|=`](https://www.w3schools.com/python/ref_set_update.asp) | Update the set with the union of this set and others |

---