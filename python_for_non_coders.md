# Python for Non-Coders: A Comprehensive Guide

Welcome to this comprehensive guide designed to introduce non-coders to the world of Python programming! Python is a versatile, high-level programming language known for its readability and simplicity, making it an excellent choice for beginners. Whether you're looking to automate tasks, analyze data, develop websites, or even dive into artificial intelligence, Python provides a powerful and accessible entry point.

## A Brief History of Python

Python was created by Guido van Rossum and first released in 1991. Its design philosophy emphasizes code readability with its notable use of significant indentation. The language was conceived in the late 1980s as a successor to the ABC language. Python 2.0 was released in 2000, introducing features like list comprehensions and a garbage collection system. Python 3.0, released in 2008, was a major revision that is not entirely backward-compatible with Python 2, and it aimed to fix fundamental design flaws of the language. Today, Python 3 is the standard.

## Why Python? Use Cases and Real-Life Examples

Python's versatility is one of its greatest strengths. Here are some key areas where Python excels:

*   **Web Development:** Frameworks like Django and Flask allow developers to build robust web applications. Instagram, Spotify, and Pinterest are examples of popular services built with Python.
*   **Data Analysis and Machine Learning:** Python has become the lingua franca for data science due to libraries like Pandas, NumPy, Scikit-learn, and TensorFlow. It's used for everything from financial modeling to medical research and predictive analytics.
*   **Automation and Scripting:** Python's simple syntax makes it ideal for writing scripts to automate repetitive tasks, such as file management, data entry, or web scraping.
*   **Artificial Intelligence:** Python is a dominant language in AI and machine learning, powering intelligent systems, natural language processing, and computer vision applications.
*   **Scientific Computing:** Researchers use Python for complex calculations, simulations, and data visualization in fields like physics, biology, and astronomy.
*   **Education:** Its beginner-friendly nature makes Python a popular choice for teaching programming concepts in schools and universities.

## 1. Basics (Foundation)

This section lays the groundwork for your Python journey, introducing fundamental concepts that are essential for writing any program.

### Variables & Data Types

In Python, a **variable** is a named storage location that holds a value. Think of it as a labeled box where you can put different kinds of information. Python is dynamically typed, meaning you don't need to declare the type of a variable explicitly; the interpreter infers it.

**Data types** classify the kind of values that variables can hold. Here are some common ones:

*   **`int` (Integer):** Whole numbers (e.g., `5`, `-100`).
*   **`float` (Floating-point number):** Numbers with a decimal point (e.g., `3.14`, `-0.5`).
*   **`str` (String):** Sequences of characters, enclosed in single (`' '`) or double (`" "`) quotes (e.g., `"Hello"`, `'Python'`).
*   **`bool` (Boolean):** Represents truth values, either `True` or `False`.

**Example:**

```python
# Assigning different data types to variables
my_integer = 10
my_float = 20.5
my_string = "Hello, Python!"
my_boolean = True

# Printing the variables and their types
print(my_integer)    # Output: 10
print(type(my_integer)) # Output: <class 'int'>

print(my_float)      # Output: 20.5
print(type(my_float))   # Output: <class 'float'>

print(my_string)     # Output: Hello, Python!
print(type(my_string))  # Output: <class 'str'>

print(my_boolean)    # Output: True
print(type(my_boolean)) # Output: <class 'bool'>
```

### Type Casting

**Type casting** (or type conversion) is the process of converting a variable from one data type to another. This is often necessary when you need to perform operations that require specific data types, such as arithmetic operations on numbers that were initially read as strings.

**Common Type Casting Functions:**

*   `int()`: Converts to an integer.
*   `float()`: Converts to a floating-point number.
*   `str()`: Converts to a string.
*   `bool()`: Converts to a boolean.

**Example:**

```python
# Converting string to integer
num_str = "123"
num_int = int(num_str)
print(f"String to int: {num_int}, Type: {type(num_int)}") # Output: String to int: 123, Type: <class 'int'>

# Converting integer to float
int_val = 10
float_val = float(int_val)
print(f"Int to float: {float_val}, Type: {type(float_val)}") # Output: Int to float: 10.0, Type: <class 'float'>

# Converting float to string
pi_float = 3.14
pi_str = str(pi_float)
print(f"Float to string: {pi_str}, Type: {type(pi_str)}") # Output: Float to string: 3.14, Type: <class 'str'>

# Converting to boolean
# Non-empty strings, non-zero numbers, and non-empty collections are True
# Empty strings, zero, and empty collections are False
print(f"'Hello' to bool: {bool('Hello')}") # Output: 'Hello' to bool: True
print(f"'' to bool: {bool('')}")       # Output: '' to bool: False
print(f"0 to bool: {bool(0)}")           # Output: 0 to bool: False
print(f"10 to bool: {bool(10)}")         # Output: 10 to bool: True
```

### Input / Output

**Input** refers to getting data from the user, typically through the keyboard. **Output** refers to displaying data to the user, usually on the screen.

*   **`input()` function:** Used to get input from the user. It always reads input as a string.
*   **`print()` function:** Used to display output to the console.

**Example:**

```python
# Getting input from the user
name = input("Enter your name: ")
age_str = input("Enter your age: ")

# Input is always a string, so we might need to cast it
age = int(age_str)

# Displaying output
print(f"Hello, {name}! You are {age} years old.")

# Example of output with multiple arguments and custom separator
print("Python", "is", "fun", sep="-") # Output: Python-is-fun
```

### Operators

Operators are special symbols that perform operations on variables and values. Understanding them is crucial for writing any logical or mathematical expressions.

#### Arithmetic Operators

These are used to perform mathematical calculations.

| Operator | Description        | Example      | Result |
| :------- | :----------------- | :----------- | :----- |
| `+`      | Addition           | `5 + 2`      | `7`    |
| `-`      | Subtraction        | `5 - 2`      | `3`    |
| `*`      | Multiplication     | `5 * 2`      | `10`   |
| `/`      | Division           | `5 / 2`      | `2.5`  |
| `%`      | Modulus (remainder)| `5 % 2`      | `1`    |
| `**`     | Exponentiation     | `5 ** 2`     | `25`   |
| `//`     | Floor Division     | `5 // 2`     | `2`    |

**Example:**

```python
a = 10
b = 3

print(f"a + b = {a + b}")   # Output: a + b = 13
print(f"a - b = {a - b}")   # Output: a - b = 7
print(f"a * b = {a * b}")   # Output: a * b = 30
print(f"a / b = {a / b}")   # Output: a / b = 3.3333333333333335
print(f"a % b = {a % b}")   # Output: a % b = 1
print(f"a ** b = {a ** b}")  # Output: a ** b = 1000
print(f"a // b = {a // b}")  # Output: a // b = 3
```

#### Logical Operators

These operators are used to combine conditional statements and evaluate boolean expressions.

| Operator | Description                               | Example                       | Result |
| :------- | :---------------------------------------- | :---------------------------- | :----- |
| `and`    | Returns `True` if both statements are true | `(5 > 3) and (10 < 20)`       | `True` |
| `or`     | Returns `True` if one of the statements is true | `(5 > 10) or (10 < 20)`       | `True` |
| `not`    | Reverses the result, returns `False` if the result is true | `not (5 > 3)`                 | `False`|

**Example:**

```python
x = 5
y = 10

print(f"x > 0 and y < 20: {x > 0 and y < 20}") # Output: x > 0 and y < 20: True
print(f"x > 10 or y < 5: {x > 10 or y < 5}")   # Output: x > 10 or y < 5: False
print(f"not (x == 5): {not (x == 5)}")         # Output: not (x == 5): False
```

#### Comparison Operators

These are used to compare two values and return a boolean result (`True` or `False`).

| Operator | Description              | Example     | Result |
| :------- | :----------------------- | :---------- | :----- |
| `==`     | Equal to                 | `a == b`    | `False`|
| `!=`     | Not equal to             | `a != b`    | `True` |
| `>`      | Greater than             | `a > b`     | `True` |
| `<`      | Less than                | `a < b`     | `False`|
| `>=`     | Greater than or equal to | `a >= b`    | `True` |
| `<=`     | Less than or equal to    | `a <= b`    | `False`|

**Example:**

```python
a = 10
b = 5

print(f"a == b: {a == b}") # Output: a == b: False
print(f"a != b: {a != b}") # Output: a != b: True
print(f"a > b: {a > b}")   # Output: a > b: True
print(f"a < b: {a < b}")   # Output: a < b: False
print(f"a >= b: {a >= b}") # Output: a >= b: True
print(f"a <= b: {a <= b}") # Output: a <= b: False
```

#### Assignment Operators

These are used to assign values to variables. They are often shorthand for combining an arithmetic operation with an assignment.

| Operator | Example    | Same As     |
| :------- | :--------- | :---------- |
| `=`      | `x = 5`    | `x = 5`     |
| `+=`     | `x += 3`   | `x = x + 3` |
| `-=`     | `x -= 3`   | `x = x - 3` |
| `*=`     | `x *= 3`   | `x = x * 3` |
| `/=`     | `x /= 3`   | `x = x / 3` |
| `%=`     | `x %= 3`   | `x = x % 3` |
| `**=`    | `x **= 3`  | `x = x ** 3`|
| `//=`    | `x //= 3`  | `x = x // 3`|

**Example:**

```python
x = 10
print(f"Initial x: {x}") # Output: Initial x: 10

x += 5 # x = x + 5
print(f"x after += 5: {x}") # Output: x after += 5: 15

x -= 3 # x = x - 3
print(f"x after -= 3: {x}") # Output: x after -= 3: 12

x *= 2 # x = x * 2
print(f"x after *= 2: {x}") # Output: x after *= 2: 24
```

### Comments

**Comments** are lines in the code that are ignored by the Python interpreter. They are used to explain the code, making it more readable and understandable for humans. Good comments are crucial for collaboration and for remembering your own code's logic later.

*   **Single-line comments:** Start with a `#` symbol.
*   **Multi-line comments (Docstrings):** Enclosed in triple quotes (`'''` or `"""`). While technically string literals, they are often used as multi-line comments or for documentation strings (docstrings) for functions, classes, and modules.

**Example:**

```python
# This is a single-line comment
print("Hello, World!") # This comment explains what the line does

"""
This is a multi-line comment.
It can span several lines.
"""

def greet(name):
    """
    This is a docstring for the greet function.
    It takes a name as input and prints a greeting.
    """
    print(f"Greetings, {name}!")

greet("Alice")
```

## 2. Control Flow

**Control flow** refers to the order in which the program's instructions are executed. It allows your program to make decisions, repeat actions, and respond dynamically to different conditions.

### `if`, `elif`, `else`

These statements are used for **conditional execution**. They allow your program to execute different blocks of code based on whether certain conditions are `True` or `False`.

*   **`if`:** Executes a block of code if its condition is `True`.
*   **`elif` (else if):** Checks an additional condition if the preceding `if` or `elif` conditions were `False`.
*   **`else`:** Executes a block of code if all preceding `if` and `elif` conditions were `False`.

**Important:** Python uses **indentation** (spaces or tabs) to define code blocks. This is crucial and not just for aesthetics!

**Example:**

```python
score = 85

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
else:
    print("Grade: F")

# Output for score = 85: Grade: B
```

### Nested Conditions

You can place `if`, `elif`, `else` statements inside another `if`, `elif`, or `else` block. This is called **nested conditions** and allows for more complex decision-making.

**Example:**

```python
age = 25
has_license = True

if age >= 18:
    print("Eligible to drive based on age.")
    if has_license:
        print("You have a license, you can drive!")
    else:
        print("You are old enough, but need to get a license.")
else:
    print("Not eligible to drive yet.")

# Output for age = 25, has_license = True:
# Eligible to drive based on age.
# You have a license, you can drive!
```

### `for` loop

A **`for` loop** is used for iterating over a sequence (like a string, list, tuple, or range) or other iterable objects. It executes a block of code for each item in the sequence.

**Syntax:**

```python
for item in sequence:
    # code to execute for each item
```

**Example (Iterating over a list):**

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(f"I like {fruit}")

# Output:
# I like apple
# I like banana
# I like cherry
```

**Example (Using `range()`):**

The `range()` function generates a sequence of numbers. `range(start, stop, step)`.

*   `range(stop)`: Generates numbers from 0 up to (but not including) `stop`.
*   `range(start, stop)`: Generates numbers from `start` up to (but not including) `stop`.
*   `range(start, stop, step)`: Generates numbers from `start` up to (but not including) `stop`, incrementing by `step`.

```python
for i in range(5):
    print(i) # Output: 0, 1, 2, 3, 4

for i in range(1, 6):
    print(i) # Output: 1, 2, 3, 4, 5

for i in range(0, 10, 2):
    print(i) # Output: 0, 2, 4, 6, 8
```

### `while` loop

A **`while` loop** repeatedly executes a block of code as long as a given condition is `True`. It's used when you don't know in advance how many times you need to loop.

**Syntax:**

```python
while condition:
    # code to execute as long as condition is True
```

**Example:**

```python
count = 0
while count < 5:
    print(f"Count is: {count}")
    count += 1 # Important: increment count to avoid infinite loop!

# Output:
# Count is: 0
# Count is: 1
# Count is: 2
# Count is: 3
# Count is: 4
```

### `break`, `continue`, `pass`

These statements allow you to alter the normal flow of loops.

*   **`break`:** Terminates the loop entirely. The program exits the loop and continues with the statement immediately after the loop.
*   **`continue`:** Skips the rest of the current iteration of the loop and moves to the next iteration.
*   **`pass`:** A null operation; nothing happens when it executes. It's used as a placeholder where a statement is syntactically required but you don't want any code to execute.

**Example (`break`):**

```python
for i in range(10):
    if i == 5:
        print("Breaking loop at 5")
        break
    print(i)

# Output:
# 0
# 1
# 2
# 3
# 4
# Breaking loop at 5
```

**Example (`continue`):**

```python
for i in range(5):
    if i == 2:
        print("Skipping 2")
        continue
    print(i)

# Output:
# 0
# 1
# Skipping 2
# 3
# 4
```

**Example (`pass`):**

```python
def my_function():
    pass # TODO: Implement this function later

for i in range(3):
    if i == 1:
        pass # Do nothing for i = 1
    else:
        print(i)

# Output:
# 0
# 2
```

## 3. Data Structures (Very Important 🔥)

**Data structures** are fundamental ways to organize and store data, enabling efficient access and modification. Python offers several built-in data structures, each with unique characteristics and use cases.

### List

A **list** is an ordered, mutable (changeable) collection of items. Lists are defined by enclosing items in square brackets `[]`, with items separated by commas. They can hold items of different data types.

*   **Ordered:** Items have a defined order, and that order will not change.
*   **Mutable:** You can change, add, or remove items after the list has been created.
*   **Allows duplicates:** You can have multiple items with the same value.

**Example:**

```python
my_list = [1, "hello", 3.14, True]
print(my_list) # Output: [1, 'hello', 3.14, True]

# Accessing elements (indexing)
print(my_list[0]) # Output: 1
print(my_list[1]) # Output: hello

# Modifying elements
my_list[0] = 100
print(my_list) # Output: [100, 'hello', 3.14, True]

# Adding elements
my_list.append("world")
print(my_list) # Output: [100, 'hello', 3.14, True, 'world']

# Removing elements
my_list.remove("hello")
print(my_list) # Output: [100, 3.14, True, 'world']
```

### Tuple

A **tuple** is an ordered, immutable (unchangeable) collection of items. Tuples are defined by enclosing items in parentheses `()`, with items separated by commas. Like lists, they can hold items of different data types.

*   **Ordered:** Items have a defined order.
*   **Immutable:** Once a tuple is created, you cannot change, add, or remove its items.
*   **Allows duplicates:** You can have multiple items with the same value.

**Example:**

```python
my_tuple = (1, "hello", 3.14, True)
print(my_tuple) # Output: (1, 'hello', 3.14, True)

# Accessing elements
print(my_tuple[0]) # Output: 1

# Attempting to modify a tuple will result in an error
# my_tuple[0] = 100 # This would raise a TypeError

# Tuples are often used for fixed collections of items, like coordinates
coordinates = (10.0, 20.0)
print(coordinates)
```

### Set

A **set** is an unordered collection of unique items. Sets are defined by enclosing items in curly braces `{}` or by using the `set()` constructor. They are mutable, but their elements must be immutable.

*   **Unordered:** Items do not have a defined order.
*   **Mutable:** You can add or remove items after the set has been created.
*   **No duplicates:** Each item in a set must be unique.

**Example:**

```python
my_set = {1, 2, 3, 2, 1}
print(my_set) # Output: {1, 2, 3} (duplicates are automatically removed)

# Adding elements
my_set.add(4)
print(my_set) # Output: {1, 2, 3, 4} (order may vary)

# Removing elements
my_set.remove(2)
print(my_set) # Output: {1, 3, 4} (order may vary)

# Set operations
set_a = {1, 2, 3}
set_b = {3, 4, 5}
print(f"Union: {set_a.union(set_b)}")         # Output: Union: {1, 2, 3, 4, 5}
print(f"Intersection: {set_a.intersection(set_b)}") # Output: Intersection: {3}
```

### Dictionary

A **dictionary** is an unordered, mutable collection of key-value pairs. Dictionaries are defined by enclosing items in curly braces `{}`, with each pair separated by a colon (`key: value`). Keys must be unique and immutable (like strings, numbers, or tuples), while values can be of any data type and can be duplicated.

*   **Unordered:** Items do not have a defined order (in Python 3.7+, insertion order is preserved, but conceptually they are still considered unordered for hashing purposes).
*   **Mutable:** You can change, add, or remove key-value pairs.
*   **Key-value pairs:** Each item consists of a key and its associated value.

**Example:**

```python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}
print(my_dict) # Output: {'name': 'Alice', 'age': 30, 'city': 'New York'}

# Accessing values by key
print(my_dict["name"]) # Output: Alice

# Modifying values
my_dict["age"] = 31
print(my_dict) # Output: {'name': 'Alice', 'age': 31, 'city': 'New York'}

# Adding new key-value pairs
my_dict["occupation"] = "Engineer"
print(my_dict) # Output: {'name': 'Alice', 'age': 31, 'city': 'New York', 'occupation': 'Engineer'}

# Removing key-value pairs
del my_dict["city"]
print(my_dict) # Output: {'name': 'Alice', 'age': 31, 'occupation': 'Engineer'}

# Getting all keys or values
print(f"Keys: {my_dict.keys()}")   # Output: Keys: dict_keys(['name', 'age', 'occupation'])
print(f"Values: {my_dict.values()}") # Output: Values: dict_values(['Alice', 31, 'Engineer'])
```

### Operations: Indexing & Slicing

**Indexing** allows you to access individual elements of ordered data structures (like lists, tuples, and strings) using their position (index). Python uses zero-based indexing, meaning the first element is at index 0.

**Slicing** allows you to extract a portion (a 
sequence) of an ordered data structure. It's done using the colon operator `[:]`.

**Syntax for Slicing:** `[start:end:step]`

*   `start`: The starting index (inclusive). If omitted, defaults to 0.
*   `end`: The ending index (exclusive). If omitted, defaults to the end of the sequence.
*   `step`: The step size (e.g., 2 for every other item). If omitted, defaults to 1.

**Example (Lists):**

```python
my_list = ["a", "b", "c", "d", "e", "f"]

# Indexing
print(my_list[0])   # Output: a (first element)
print(my_list[3])   # Output: d
print(my_list[-1])  # Output: f (last element)

# Slicing
print(my_list[1:4])   # Output: ["b", "c", "d"] (elements from index 1 up to (but not including) 4)
print(my_list[:3])    # Output: ["a", "b", "c"] (from beginning to index 3)
print(my_list[2:])    # Output: ["c", "d", "e", "f"] (from index 2 to end)
print(my_list[::2])   # Output: ["a", "c", "e"] (every second element)
print(my_list[::-1])  # Output: ["f", "e", "d", "c", "b", "a"] (reverse the list)
```

**Example (Strings - works similarly):**

```python
my_string = "Python"
print(my_string[0])    # Output: P
print(my_string[1:4])  # Output: yth
```

### Looping Data Structures

Looping (iterating) through data structures is a common operation to process each item within them.

**Example (List):**

```python
numbers = [10, 20, 30, 40]
for num in numbers:
    print(num * 2)

# Output:
# 20
# 40
# 60
# 80
```

**Example (Tuple):**

```python
colors = ("red", "green", "blue")
for color in colors:
    print(f"Current color: {color}")
```

**Example (Set):**

```python
unique_chars = {"a", "b", "c"}
for char in unique_chars:
    print(char)
```

**Example (Dictionary):**

```python
person = {"name": "Bob", "age": 25}

# Looping through keys
for key in person:
    print(f"Key: {key}")

# Looping through values
for value in person.values():
    print(f"Value: {value}")

# Looping through key-value pairs
for key, value in person.items():
    print(f"{key}: {value}")
```

### Built-in methods

Each data structure comes with a variety of built-in methods that allow you to perform common operations efficiently. Here are a few examples:

**List Methods:**

| Method       | Description                                    | Example                                   |
| :----------- | :--------------------------------------------- | :---------------------------------------- |
| `append()`   | Adds an element to the end of the list.        | `my_list.append(5)`                       |
| `insert()`   | Adds an element at a specified position.       | `my_list.insert(1, 2)`                    |
| `remove()`   | Removes the first occurrence of a value.       | `my_list.remove(3)`                       |
| `pop()`      | Removes and returns the element at a given index (or last). | `my_list.pop(0)`                          |
| `sort()`     | Sorts the list in ascending order.             | `my_list.sort()`                          |
| `reverse()`  | Reverses the order of elements.                | `my_list.reverse()`                       |
| `count()`    | Returns the number of times a value appears.   | `my_list.count(1)`                        |
| `index()`    | Returns the index of the first occurrence of a value. | `my_list.index(4)`                        |

**Example (List Methods):**

```python
my_list = [3, 1, 4, 1, 5, 9]
my_list.append(2)
print(f"After append(2): {my_list}") # Output: [3, 1, 4, 1, 5, 9, 2]

my_list.sort()
print(f"After sort(): {my_list}")   # Output: [1, 1, 2, 3, 4, 5, 9]

my_list.reverse()
print(f"After reverse(): {my_list}") # Output: [9, 5, 4, 3, 2, 1, 1]

print(f"Count of 1: {my_list.count(1)}") # Output: Count of 1: 2
```

**Dictionary Methods:**

| Method     | Description                                    | Example                                   |
| :--------- | :--------------------------------------------- | :---------------------------------------- |
| `keys()`   | Returns a view object of all keys.             | `my_dict.keys()`                          |
| `values()` | Returns a view object of all values.           | `my_dict.values()`                        |
| `items()`  | Returns a view object of all key-value pairs.  | `my_dict.items()`                         |
| `get()`    | Returns the value for a key, or a default if key not found. | `my_dict.get("age", 0)`                   |
| `pop()`    | Removes the item with the specified key and returns its value. | `my_dict.pop("city")`                     |

**Example (Dictionary Methods):**

```python
student = {"name": "Charlie", "age": 22, "major": "CS"}

print(f"Keys: {student.keys()}")     # Output: Keys: dict_keys(["name", "age", "major"])
print(f"Values: {student.values()}")   # Output: Values: dict_values(["Charlie", 22, "CS"])
print(f"Items: {student.items()}")     # Output: Items: dict_items([("name", "Charlie"), ("age", 22), ("major", "CS")])

major = student.get("major", "Undeclared")
print(f"Major: {major}") # Output: Major: CS

gpa = student.get("gpa", "N/A")
print(f"GPA: {gpa}")     # Output: GPA: N/A
```

## 4. Strings

**Strings** are sequences of characters, used to represent text. In Python, strings are immutable, meaning once created, their content cannot be changed. However, you can create new strings based on existing ones.

### String creation

Strings can be created by enclosing characters in single quotes (`'...'`), double quotes (`"..."`), or triple quotes (`'''...'''` or `"""..."""`) for multi-line strings.

**Example:**

```python
single_quote_str = 'Hello Python'
double_quote_str = "World of Strings"
multi_line_str = """
This is a
multi-line
string.
"""

print(single_quote_str)
print(double_quote_str)
print(multi_line_str)
```

### Indexing & slicing

Just like lists and tuples, strings support indexing and slicing to access individual characters or substrings.

**Example:**

```python
my_string = "Python Programming"

# Indexing
print(my_string[0])    # Output: P
print(my_string[7])    # Output: P (space is also a character)
print(my_string[-1])   # Output: g

# Slicing
print(my_string[0:6])  # Output: Python
print(my_string[7:])   # Output: Programming
print(my_string[:6])   # Output: Python
print(my_string[::2])  # Output: Pto rgamn (every other character)
```

### String methods

Python strings come with a rich set of built-in methods for various text manipulation tasks.

| Method       | Description                                    | Example                                   |
| :----------- | :--------------------------------------------- | :---------------------------------------- |
| `len()`      | (Built-in function, not a method) Returns the length of the string. | `len("hello")`                            |
| `lower()`    | Converts string to lowercase.                  | `"HELLO".lower()`                         |
| `upper()`    | Converts string to uppercase.                  | `"hello".upper()`                         |
| `strip()`    | Removes leading/trailing whitespace.           | `"  hello  ".strip()`                     |
| `replace()`  | Replaces occurrences of a substring.           | `"hello".replace("l", "x")`               |
| `split()`    | Splits string into a list of substrings.       | `"a,b,c".split(",")`                      |
| `join()`     | Joins elements of an iterable with the string as a separator. | `"-".join(["a", "b", "c"])`               |
| `find()`     | Returns the lowest index of a substring, or -1 if not found. | `"hello".find("lo")`                      |
| `startswith()`| Checks if string starts with a prefix.         | `"hello".startswith("he")`                |
| `endswith()` | Checks if string ends with a suffix.           | `"hello".endswith("lo")`                  |

**Example:**

```python
text = "  Python is FUN!  "

print(f"Original: ", text)
print(f"Lowercase: {text.lower()}") # Output:   python is fun!  
print(f"Uppercase: {text.upper()}") # Output:   PYTHON IS FUN!  
print(f"Stripped: ", text.strip()) # Output: Python is FUN!

cleaned_text = text.strip()
print(f"Replaced: {cleaned_text.replace("FUN", "awesome")}") # Output: Python is awesome!

words = cleaned_text.split(" ")
print(f"Split into words: {words}") # Output: ["Python", "is", "FUN!"]

joined_text = "_".join(words)
print(f"Joined with underscore: {joined_text}") # Output: Python_is_FUN!
```

### Formatting (`f-strings` 🔥)

**f-strings** (formatted string literals) provide a concise and convenient way to embed Python expressions inside string literals for formatting. They are prefixed with `f` or `F`.

**Example:**

```python
name = "Alice"
age = 30

# Using f-string
message = f"Hello, my name is {name} and I am {age} years old."
print(message) # Output: Hello, my name is Alice and I am 30 years old.

# You can also include expressions directly
price = 19.99
quantity = 3
total = price * quantity
print(f"The total for {quantity} items at ${price:.2f} each is ${total:.2f}.")
# Output: The total for 3 items at $19.99 each is $59.97.

# f-strings are powerful for debugging too
print(f"{name=}, {age=}") # Output: name=\'Alice\', age=30
```

## 5. Functions

A **function** is a block of organized, reusable code that is used to perform a single, related action. Functions provide better modularity for your application and a high degree of code reusing. Python has many built-in functions, but you can also create your own.

### Function definition

Functions are defined using the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`. The code block within the function is indented.

**Syntax:**

```python
def function_name(parameters):
    """Docstring: Explain what the function does."""
    # function body
    # return value (optional)
```

**Example:**

```python
def greet():
    print("Hello, welcome to the function!")

# Calling the function
greet()
# Output: Hello, welcome to the function!
```

### Parameters & arguments

**Parameters** are the variables listed inside the parentheses in the function definition. **Arguments** are the actual values passed to the function when it is called.

#### Positional Arguments

Arguments passed to a function in the correct positional order.

**Example:**

```python
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 3) # 5 is assigned to a, 3 to b
print(f"Sum: {result}") # Output: Sum: 8
```

#### Keyword Arguments

Arguments identified by the parameter name. This allows you to pass arguments in any order.

**Example:**

```python
def subtract_numbers(a, b):
    return a - b

result = subtract_numbers(b=3, a=10) # Order doesn't matter with keyword arguments
print(f"Difference: {result}") # Output: Difference: 7
```

#### Default Arguments

Parameters can have default values. If an argument is not provided for a parameter with a default value, the default value is used.

**Example:**

```python
def say_hello(name="Guest"):
    print(f"Hello, {name}!")

say_hello()        # Output: Hello, Guest!
say_hello("Alice") # Output: Hello, Alice!
```

### `*args`, `**kwargs` 🔥

These special syntaxes allow functions to accept a variable number of arguments.

*   **`*args` (Arbitrary Positional Arguments):** Allows a function to accept any number of positional arguments. These arguments are packed into a tuple.
*   **`**kwargs` (Arbitrary Keyword Arguments):** Allows a function to accept any number of keyword arguments. These arguments are packed into a dictionary.

**Example (`*args`):**

```python
def sum_all_numbers(*numbers):
    total = 0
    for num in numbers:
        total += num
    return total

print(sum_all_numbers(1, 2, 3))       # Output: 6
print(sum_all_numbers(10, 20, 30, 40)) # Output: 100
```

**Example (`**kwargs`):**

```python
def display_info(**details):
    for key, value in details.items():
        print(f"{key}: {value}")

display_info(name="Bob", age=25, city="London")
# Output:
# name: Bob
# age: 25
# city: London
```

### Return values

The `return` statement is used to send a value back from a function to the caller. If a function doesn't explicitly `return` a value, it implicitly returns `None`.

**Example:**

```python
def multiply(x, y):
    return x * y

product = multiply(4, 5)
print(f"Product: {product}") # Output: Product: 20

def do_nothing():
    pass # No return statement

result = do_nothing()
print(f"Result of do_nothing: {result}") # Output: Result of do_nothing: None
```

### Lambda functions

**Lambda functions** (also called anonymous functions) are small, single-expression functions that don't have a name. They are defined using the `lambda` keyword.

**Syntax:** `lambda arguments: expression`

**Example:**

```python
# A regular function to add two numbers
def add(a, b):
    return a + b

# The equivalent lambda function
add_lambda = lambda a, b: a + b

print(add(2, 3))         # Output: 5
print(add_lambda(2, 3))  # Output: 5

# Lambdas are often used with higher-order functions like map(), filter(), sort()
points = [(1, 2), (3, 1), (5, 0)]
# Sort points based on the second element of each tuple
points.sort(key=lambda p: p[1])
print(f"Sorted points: {points}") # Output: Sorted points: [(5, 0), (3, 1), (1, 2)]
```

## 6. Modules & Packages

As your Python programs grow larger, it becomes impractical to keep all code in a single file. **Modules** and **packages** help organize code into manageable, reusable units.

### What is a module

A **module** is simply a Python file (`.py`) containing Python definitions and statements. When you import a module, you can use the functions, classes, and variables defined within it.

**Example:**

Let's say you have a file named `my_module.py` with the following content:

```python
# my_module.py
def greeting(name):
    return f"Hello, {name}! From my_module."

PI = 3.14159
```

You can then use it in another Python script:

```python
# main_script.py
import my_module

print(my_module.greeting("World")) # Output: Hello, World! From my_module.
print(my_module.PI)                # Output: 3.14159

# You can also import specific items
from my_module import greeting, PI
print(greeting("Alice")) # Output: Hello, Alice! From my_module.
print(PI)                # Output: 3.14159

# Or import everything (generally discouraged for larger projects)
from my_module import *
```

### Built-in modules (`math`, `random`, `datetime`)

Python comes with a rich set of **built-in modules** that provide access to system functionality and common utilities.

*   **`math`:** Provides mathematical functions.
*   **`random`:** Generates pseudo-random numbers.
*   **`datetime`:** Classes for working with dates and times.

**Example (`math`):**

```python
import math

print(f"Pi: {math.pi}")          # Output: Pi: 3.141592653589793
print(f"Square root of 16: {math.sqrt(16)}") # Output: Square root of 16: 4.0
print(f"Ceiling of 4.3: {math.ceil(4.3)}")   # Output: Ceiling of 4.3: 5
```

**Example (`random`):**

```python
import random

print(f"Random integer between 1 and 10: {random.randint(1, 10)}")
print(f"Random float between 0 and 1: {random.random()}")

my_list = ["apple", "banana", "cherry"]
print(f"Random choice from list: {random.choice(my_list)}")
```

**Example (`datetime`):**

```python
import datetime

current_time = datetime.datetime.now()
print(f"Current date and time: {current_time}")
print(f"Current year: {current_time.year}")
print(f"Formatted date: {current_time.strftime("%Y-%m-%d %H:%M:%S")}")
```

### Creating custom modules

As shown above, you create a custom module by simply saving your Python code in a `.py` file. You can then import it into other scripts.

### Packages & `__init__.py`

A **package** is a way of organizing related modules into a directory hierarchy. It's essentially a folder containing multiple module files and a special `__init__.py` file.

The `__init__.py` file (which can be empty) tells Python that the directory should be treated as a package. It can also be used to define what happens when the package is imported.

**Example Directory Structure:**

```
my_project/
├── main.py
└── my_package/
    ├── __init__.py
    ├── module_a.py
    └── module_b.py
```

**`my_package/module_a.py`:**

```python
# my_package/module_a.py
def func_a():
    return "Function A from module_a"
```

**`my_package/module_b.py`:**

```python
# my_package/module_b.py
def func_b():
    return "Function B from module_b"
```

**`main.py`:**

```python
# main.py
from my_package import module_a, module_b

print(module_a.func_a())
print(module_b.func_b())

# You can also import specific functions directly
from my_package.module_a import func_a
print(func_a())
```

## 7. File Handling

**File handling** is the process of reading from or writing to files on your computer's storage. This is essential for persistent data storage, configuration, and data exchange.

### Read / Write files

Python provides built-in functions to interact with files. The primary function is `open()`, which returns a file object.

It's best practice to use the `with` statement when dealing with file objects. This ensures that the file is properly closed after its suite finishes, even if an error occurs.

**Syntax:**

```python
with open("filename.txt", "mode") as file_object:
    # perform file operations
```

### Modes (`r`, `w`, `a`)

The `mode` argument specifies how the file is to be opened:

| Mode | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             Sven is a Python developer who needs to create a `.md` file with Python notes to teach a non-coder. The notes should be detailed, interactive, and include multiple examples for good understanding. Additionally, the notes should cover the history of Python with use cases and real-life examples. The content should be structured based on the following points: Basics (Foundation), Control Flow, Data Structures, Strings, Functions, Modules & Packages, File Handling, Exception Handling, Object-Oriented Programming (OOP), Advanced Python, Built-in Functions, and Standard Libraries. The agent has already completed writing sections 1-4. Now, the agent needs to continue with sections 5-8. The agent should append the content to the existing Markdown file. The agent has already planned to do this in phase 3. The current phase is 3. The agent should now execute the action to append the content. The previous action was to append the content for Data Structures and Strings. The next action is to append the content for Functions, Modules & Packages, File Handling, and Exception Handling. The agent should then advance to the next phase. The current phase is 3. The next phase is 4. The agent should then execute the action to append the content for OOP, Advanced Python, Built-in Functions, and Standard Libraries. The agent should then advance to the next phase. The current phase is 4. The next phase is 5. The agent should then deliver the final Markdown file to the user. The agent should then end the task. The agent should make sure to follow all the instructions in the prompt, including the formatting instructions. The agent should also make sure to include all the requested content, including the history of Python with use cases and real-life examples, and the detailed interactive examples with tables. The agent should also make sure to use inline numeric citations with Markdown reference-style links for all factual claims or external data, and include a 

## 9. Object-Oriented Programming (OOP) 🔥

**Object-Oriented Programming (OOP)** is a programming paradigm that uses "objects" – instances of classes – to design applications and computer programs. It focuses on bundling data and the functions that operate on that data into a single unit. OOP aims to increase the flexibility and maintainability of programs.

### Class & Object

*   **Class:** A blueprint or a template for creating objects. It defines a set of attributes (data) and methods (functions) that the objects created from the class will have.
*   **Object:** An instance of a class. When a class is defined, no memory is allocated until an object is created from it.

**Example:**

```python
class Dog:
    # Class attribute
    species = "Canis familiaris"

    def __init__(self, name, age):
        # Instance attributes
        self.name = name
        self.age = age

    def bark(self):
        return f"{self.name} says Woof!"

    def description(self):
        return f"{self.name} is {self.age} years old."

# Creating objects (instances) of the Dog class
my_dog = Dog("Buddy", 3)
your_dog = Dog("Lucy", 5)

print(my_dog.description()) # Output: Buddy is 3 years old.
print(your_dog.bark())      # Output: Lucy says Woof!
print(my_dog.species)       # Output: Canis familiaris
```

### Constructor (`__init__`)

The `__init__` method is a special method in Python classes. It's called automatically whenever a new object of the class is created. Its primary purpose is to initialize the attributes of the object.

*   `self`: Refers to the instance of the class itself. It must be the first parameter of any instance method.

**Example (see `Dog` class above):**

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0 # Default value

    def get_descriptive_name(self):
        return f"{self.year} {self.make} {self.model}"

my_car = Car("Toyota", "Camry", 2020)
print(my_car.get_descriptive_name()) # Output: 2020 Toyota Camry
```

### Inheritance

**Inheritance** allows a class (child/subclass) to inherit attributes and methods from another class (parent/superclass). This promotes code reusability and establishes a natural hierarchy between classes.

**Example:**

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        raise NotImplementedError("Subclass must implement abstract method")

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

my_cat = Cat("Whiskers")
my_dog = Dog("Max")

print(my_cat.speak()) # Output: Whiskers says Meow!
print(my_dog.speak()) # Output: Max says Woof!
```

### Polymorphism

**Polymorphism** means "many forms." In OOP, it refers to the ability of different objects to respond to the same method call in their own specific ways. This is often achieved through inheritance and method overriding.

**Example (using the `Animal`, `Cat`, `Dog` classes from above):**

```python
def make_animal_speak(animal):
    print(animal.speak())

make_animal_speak(Cat("Garfield")) # Output: Garfield says Meow!
make_animal_speak(Dog("Rocky"))    # Output: Rocky says Woof!
```

### Encapsulation

**Encapsulation** is the bundling of data (attributes) and methods (functions) that operate on the data into a single unit (class). It also involves restricting direct access to some of an object's components, which is often done to prevent accidental modification of data. In Python, encapsulation is achieved by convention (using single or double underscores for 
internal attributes), rather than strict access modifiers like `private` in other languages.

**Example:**

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance # Using __ to indicate a 'private' attribute by convention

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            print(f"Deposited {amount}. New balance: {self.__balance}")
        else:
            print("Deposit amount must be positive.")

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
            print(f"Withdrew {amount}. New balance: {self.__balance}")
        else:
            print("Invalid withdrawal amount or insufficient funds.")

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
account.deposit(500)  # Output: Deposited 500. New balance: 1500
account.withdraw(200) # Output: Withdrew 200. New balance: 1300
# print(account.__balance) # This would raise an AttributeError due to name mangling
print(account.get_balance()) # Output: 1300
```

### Abstraction

**Abstraction** means hiding the complex implementation details and showing only the essential features of an object. In Python, abstract classes and methods can be created using the `abc` (Abstract Base Classes) module.

**Example:**

```python
from abc import ABC, abstractmethod

class Shape(ABC): # Abstract Base Class
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14159 * self.radius ** 2

    def perimeter(self):
        return 2 * 3.14159 * self.radius

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

    def perimeter(self):
        return 2 * (self.width + self.height)

# shape = Shape() # This would raise a TypeError because Shape is an abstract class

circle = Circle(5)
print(f"Circle Area: {circle.area()}")         # Output: Circle Area: 78.53975
print(f"Circle Perimeter: {circle.perimeter()}") # Output: Circle Perimeter: 31.4159

rectangle = Rectangle(4, 6)
print(f"Rectangle Area: {rectangle.area()}")         # Output: Rectangle Area: 24
print(f"Rectangle Perimeter: {rectangle.perimeter()}") # Output: Rectangle Perimeter: 20
```

## 10. Advanced Python

This section delves into more advanced Python features that can make your code more concise, efficient, and Pythonic.

### List Comprehension 🔥

**List comprehension** provides a concise way to create lists. It consists of brackets containing an expression followed by a `for` clause, then zero or more `for` or `if` clauses. It's often a more readable and efficient alternative to traditional `for` loops for list creation.

**Syntax:** `[expression for item in iterable if condition]`

**Example:**

```python
# Traditional loop
squares = []
for i in range(10):
    squares.append(i**2)
print(f"Traditional squares: {squares}") # Output: Traditional squares: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# List comprehension
squares_comp = [i**2 for i in range(10)]
print(f"List comprehension squares: {squares_comp}") # Output: List comprehension squares: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# List comprehension with a condition
even_squares = [i**2 for i in range(10) if i % 2 == 0]
print(f"Even squares: {even_squares}") # Output: Even squares: [0, 4, 16, 36, 64]
```

### Dictionary Comprehension

Similar to list comprehension, **dictionary comprehension** allows you to create dictionaries in a concise way.

**Syntax:** `{key_expression: value_expression for item in iterable if condition}`

**Example:**

```python
# Create a dictionary of numbers and their squares
squares_dict = {i: i**2 for i in range(5)}
print(f"Squares dictionary: {squares_dict}") # Output: Squares dictionary: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Dictionary comprehension with a condition
odd_squares_dict = {i: i**2 for i in range(10) if i % 2 != 0}
print(f"Odd squares dictionary: {odd_squares_dict}") # Output: Odd squares dictionary: {1: 1, 3: 9, 5: 25, 7: 49, 9: 81}
```

### Generators & `yield` 🔥

**Generators** are functions that return an iterator that produces a sequence of results instead of a single value. They are memory-efficient because they generate items one by one, only when requested, rather than creating the entire sequence in memory at once.

The `yield` keyword is what makes a function a generator. When `yield` is encountered, the function's state is saved, and the yielded value is returned. When the generator is called again, it resumes execution from where it left off.

**Example:**

```python
def countdown(num):
    print("Starting countdown...")
    while num > 0:
        yield num
        num -= 1
    print("Countdown finished!")

# Using the generator
for number in countdown(3):
    print(number)

# Output:
# Starting countdown...
# 3
# 2
# 1
# Countdown finished!
```

### Decorators 🔥

A **decorator** is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure. Decorators are essentially functions that take another function as an argument and return a new function that usually extends the behavior of the original function.

**Syntax:**

```python
@decorator_function
def original_function():
    pass
```

**Example:**

```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_whee():
    print("Whee!")

say_whee()

# Output:
# Something is happening before the function is called.
# Whee!
# Something is happening after the function is called.
```

### Iterators

An **iterator** is an object that can be iterated upon, meaning that you can traverse through all the elements. In Python, an object is an iterator if it implements the `__iter__()` and `__next__()` methods.

*   `__iter__()`: Returns the iterator object itself.
*   `__next__()`: Returns the next item from the sequence. On exhaustion, it raises `StopIteration`.

**Example:**

```python
my_list = [1, 2, 3]
my_iterator = iter(my_list) # Get an iterator from a list

print(next(my_iterator)) # Output: 1
print(next(my_iterator)) # Output: 2
print(next(my_iterator)) # Output: 3
# print(next(my_iterator)) # This would raise StopIteration

# Loops (like for loops) implicitly use iterators
for x in my_list:
    print(x)
```

### Context Managers (`with`)

**Context managers** allow you to allocate and release resources precisely when you want to. The most common way to use them is with the `with` statement. The `with` statement ensures that resources are properly acquired and released, even if errors occur.

**Example (File Handling - best practice):**

```python
# Instead of:
# file = open("my_file.txt", "w")
# try:
#     file.write("Hello World")
# finally:
#     file.close()

# Use a context manager:
with open("my_file.txt", "w") as file:
    file.write("Hello World from context manager!")
# The file is automatically closed when exiting the 'with' block

with open("my_file.txt", "r") as file:
    content = file.read()
    print(f"File content: {content}") # Output: File content: Hello World from context manager!
```

### Closures

A **closure** is a function object that remembers values in its enclosing scope even if they are no longer in memory. It's a record of a function together with an environment. The environment is a mapping associating each free variable of the function (variables that are used in the function but not defined locally) with the value or reference to which the name was bound when the closure was created.

**Example:**

```python
def outer_function(msg):
    message = msg # 'message' is a free variable

    def inner_function():
        print(message)
    return inner_function

hello_func = outer_function("Hello")
bye_func = outer_function("Goodbye")

hello_func() # Output: Hello
bye_func()   # Output: Goodbye
```

## 11. Built-in Functions

Python provides a rich set of **built-in functions** that are always available for use. Here are some commonly used ones, including higher-order functions.

### `map()`, `filter()`, `reduce()` 🔥

These are higher-order functions, meaning they can take other functions as arguments.

*   **`map(function, iterable)`:** Applies a given `function` to each item of an `iterable` and returns a `map` object (which is an iterator).

**Example (`map`):**

```python
numbers = [1, 2, 3, 4]
squared_numbers = list(map(lambda x: x**2, numbers))
print(f"Squared numbers: {squared_numbers}") # Output: Squared numbers: [1, 4, 9, 16]

# Using a regular function
def double(x):
    return x * 2
doubled_numbers = list(map(double, numbers))
print(f"Doubled numbers: {doubled_numbers}") # Output: Doubled numbers: [2, 4, 6, 8]
```

*   **`filter(function, iterable)`:** Constructs an iterator from elements of an `iterable` for which a `function` returns true.

**Example (`filter`):**

```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(f"Even numbers: {even_numbers}") # Output: Even numbers: [2, 4, 6]
```

*   **`reduce(function, iterable)`:** Applies a `function` of two arguments cumulatively to the items of an `iterable`, from left to right, so as to reduce the iterable to a single value. (Note: `reduce` is in the `functools` module).

**Example (`reduce`):**

```python
from functools import reduce

numbers = [1, 2, 3, 4]
sum_all = reduce(lambda x, y: x + y, numbers)
print(f"Sum using reduce: {sum_all}") # Output: Sum using reduce: 10

product_all = reduce(lambda x, y: x * y, numbers)
print(f"Product using reduce: {product_all}") # Output: Product using reduce: 24
```

### `zip()`

The `zip()` function takes iterables (can be zero or more), aggregates them in a tuple, and returns an iterator of tuples.

**Example:**

```python
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]

zipped_data = list(zip(names, ages))
print(f"Zipped data: {zipped_data}") # Output: Zipped data: [("Alice", 25), ("Bob", 30), ("Charlie", 35)]

# Looping through zipped data
for name, age in zip(names, ages):
    print(f"{name} is {age} years old.")
```

### `enumerate()`

The `enumerate()` function adds a counter to an iterable and returns it as an enumerate object. This is often used in `for` loops to get both the index and the value of each item.

**Example:**

```python
fruits = ["apple", "banana", "cherry"]

for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")

# Output:
# Index 0: apple
# Index 1: banana
# Index 2: cherry
```

### `any()`, `all()`

*   **`any(iterable)`:** Returns `True` if any element of the `iterable` is true. If the iterable is empty, it returns `False`.
*   **`all(iterable)`:** Returns `True` if all elements of the `iterable` are true. If the iterable is empty, it returns `True`.

**Example:**

```python
list1 = [True, False, True]
list2 = [True, True, True]
list3 = [False, False, False]

print(f"Any in list1: {any(list1)}") # Output: Any in list1: True
print(f"All in list1: {all(list1)}") # Output: All in list1: False

print(f"Any in list2: {any(list2)}") # Output: Any in list2: True
print(f"All in list2: {all(list2)}") # Output: All in list2: True

print(f"Any in list3: {any(list3)}") # Output: Any in list3: False
print(f"All in list3: {all(list3)}") # Output: All in list3: False
```

## 12. Standard Libraries

Python's **standard library** is a vast collection of modules that are included with every Python installation. These modules provide solutions for a wide range of common programming tasks, from mathematical operations to internet protocols and operating system interfaces.

### `math`

As seen before, the `math` module provides access to mathematical functions and constants.

**Example:**

```python
import math

print(f"e (Euler's number): {math.e}")
print(f"log(100, 10): {math.log(100, 10)}") # log base 10
print(f"sin(math.pi/2): {math.sin(math.pi/2)}") # Sine of 90 degrees (in radians)
```

### `datetime`

The `datetime` module supplies classes for working with dates and times in both simple and complex ways.

**Example:**

```python
import datetime

# Current date and time
now = datetime.datetime.now()
print(f"Current datetime: {now}")

# Specific date
date_obj = datetime.date(2023, 1, 15)
print(f"Specific date: {date_obj}")

# Time difference (timedelta)
time_difference = datetime.timedelta(days=7)
next_week = now + time_difference
print(f"Next week: {next_week}")
```

### `os`

The `os` module provides a way of using operating system dependent functionality like reading or writing to a file system. It allows you to interact with the operating system.

**Example:**

```python
import os

# Get current working directory
current_dir = os.getcwd()
print(f"Current working directory: {current_dir}")

# List contents of a directory
# print(f"Contents of current directory: {os.listdir(current_dir)}")

# Create a new directory
# try:
#     os.mkdir("new_folder")
#     print("Created 'new_folder'")
# except FileExistsError:
#     print("'new_folder' already exists")

# Check if a path exists
print(f"Does 'python_for_non_coders.md' exist? {os.path.exists('python_for_non_coders.md')}")
```

### `sys`

The `sys` module provides access to system-specific parameters and functions. It allows you to interact with the Python interpreter itself.

**Example:**

```python
import sys

print(f"Python version: {sys.version}")
print(f"Python executable: {sys.executable}")

# Command line arguments
# print(f"Command line arguments: {sys.argv}")
```

### `collections`

The `collections` module implements specialized container datatypes providing alternatives to Python's general purpose built-in containers like `dict`, `list`, `set`, and `tuple`.

*   **`Counter`:** A dict subclass for counting hashable objects.
*   **`deque`:** A list-like container with fast appends and pops on either end.
*   **`defaultdict`:** A dict subclass that calls a factory function to supply missing values.

**Example (`Counter`):**

```python
from collections import Counter

my_list = ["apple", "banana", "apple", "orange", "banana", "apple"]
word_counts = Counter(my_list)
print(f"Word counts: {word_counts}") # Output: Word counts: Counter({"apple": 3, "banana": 2, "orange": 1})
```

### `itertools`

The `itertools` module provides a collection of fast, memory-efficient tools that are useful by themselves or in combination. Together, they form an "iterator algebra" making it possible to construct specialized tools succinctly and efficiently in pure Python.

**Example (`itertools.permutations`):**

```python
from itertools import permutations

items = [1, 2, 3]
perms = list(permutations(items))
print(f"Permutations of {items}: {perms}")
# Output: Permutations of [1, 2, 3]: [(1, 2, 3), (1, 3, 2), (2, 1, 3), (2, 3, 1), (3, 1, 2), (3, 2, 1)]
```

---

**Author:** Manus AI
