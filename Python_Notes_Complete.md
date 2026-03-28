# 🐍 Python — Complete Notes for Beginners
### *From Zero to Hero: Learn Python Step by Step*

---

> **Who is this for?**
> These notes are written for absolute beginners — no coding experience required. Every concept is explained simply, with real-world analogies and multiple examples. Read slowly, try every example, and enjoy the journey! 🚀

---

## 📜 History of Python

| Year | Event |
|------|-------|
| 1989 | Guido van Rossum began developing Python during Christmas holidays |
| 1991 | Python 0.9.0 — first public release |
| 1994 | Python 1.0 released — included `lambda`, `map`, `filter`, `reduce` |
| 2000 | Python 2.0 released — added list comprehensions, garbage collection |
| 2008 | Python 3.0 released — major redesign (not backward compatible) |
| 2020 | Python 2 officially retired |
| 2023+ | Python 3.11+ with massive speed improvements |

**Why is it called Python?**
Guido van Rossum was a fan of the British comedy group *Monty Python's Flying Circus*. That's where the name comes from — not the snake! 🎭

**Why Python is so popular:**

| Feature | What it means |
|--------|---------------|
| Simple syntax | Reads almost like English |
| Versatile | Web, AI, data science, automation, games |
| Large community | Millions of developers, tons of help online |
| Rich libraries | Thousands of ready-made tools |
| Free & Open Source | Anyone can use it |

```
Python is used by: Google, NASA, Netflix, Instagram, Spotify, and more!
```

---

## 🟢 1. Basics (Foundation)

### 📦 Variables & Data Types

Think of a **variable** as a labelled box. You put something inside the box and give it a name so you can use it later.

```python
# Creating variables
name = "Riya"         # Text (String)
age = 20              # Whole number (Integer)
height = 5.4          # Decimal number (Float)
is_student = True     # Yes/No (Boolean)

print(name)           # Output: Riya
print(age)            # Output: 20
print(height)         # Output: 5.4
print(is_student)     # Output: True
```

#### Data Types Table

| Data Type | Python Name | Example | Real-life analogy |
|-----------|-------------|---------|-------------------|
| Text | `str` | `"Hello"` | A word on paper |
| Whole number | `int` | `42` | Count of apples |
| Decimal number | `float` | `3.14` | Weight in kg |
| True / False | `bool` | `True` | Light switch ON/OFF |
| Nothing | `NoneType` | `None` | Empty box |

```python
# Check the data type with type()
print(type("Hello"))     # <class 'str'>
print(type(100))         # <class 'int'>
print(type(3.14))        # <class 'float'>
print(type(True))        # <class 'bool'>
print(type(None))        # <class 'NoneType'>
```

**Multiple assignments in one line:**
```python
x, y, z = 10, 20, 30
print(x, y, z)   # 10 20 30

# Same value to multiple variables
a = b = c = 0
print(a, b, c)   # 0 0 0
```

---

### 🔄 Type Casting

**Type Casting** = Changing one data type to another. Like converting rupees to dollars.

```python
# String to Integer
num_str = "42"
num_int = int(num_str)
print(num_int + 8)      # Output: 50 (math works now!)

# Integer to String
age = 25
message = "I am " + str(age) + " years old"
print(message)           # I am 25 years old

# Integer to Float
x = 5
y = float(x)
print(y)                 # 5.0

# Float to Integer (cuts the decimal, does NOT round)
price = 9.99
print(int(price))        # 9   ← notice: 9, NOT 10

# String to Float
temperature = "36.6"
print(float(temperature) + 1)   # 37.6
```

**Common Casting Functions:**

| Function | Converts to | Example |
|----------|-------------|---------|
| `int()` | Integer | `int("5")` → `5` |
| `float()` | Float | `float("3.14")` → `3.14` |
| `str()` | String | `str(100)` → `"100"` |
| `bool()` | Boolean | `bool(0)` → `False` |

---

### ⌨️ Input / Output

**Output** — Showing something on screen: `print()`
**Input** — Getting information from the user: `input()`

```python
# Basic print
print("Hello, World!")

# Print multiple things
name = "Arjun"
age = 22
print("Name:", name, "Age:", age)     # Name: Arjun Age: 22

# Print with separator
print("Apple", "Mango", "Banana", sep=", ")   # Apple, Mango, Banana

# Print with end (default end is newline \n)
print("Hello", end=" ")
print("World")    # Hello World   (on same line)

# Taking input from user (ALWAYS returns a string)
name = input("Enter your name: ")
print("Hello,", name)

# Converting input to a number
age = int(input("Enter your age: "))
print("In 10 years, you will be", age + 10)

# Taking float input
price = float(input("Enter price: "))
print("With tax (18%):", price * 1.18)
```

> ⚠️ **Important:** `input()` always gives you a **string**. If you want a number, you must convert it with `int()` or `float()`.

---

### ➕ Operators

#### Arithmetic Operators

| Operator | Symbol | Example | Result |
|----------|--------|---------|--------|
| Addition | `+` | `5 + 3` | `8` |
| Subtraction | `-` | `10 - 4` | `6` |
| Multiplication | `*` | `4 * 3` | `12` |
| Division | `/` | `10 / 3` | `3.333...` |
| Floor Division | `//` | `10 // 3` | `3` |
| Modulus (Remainder) | `%` | `10 % 3` | `1` |
| Exponent (Power) | `**` | `2 ** 8` | `256` |

```python
a = 17
b = 5

print(a + b)    # 22
print(a - b)    # 12
print(a * b)    # 85
print(a / b)    # 3.4
print(a // b)   # 3   ← floor division (whole part only)
print(a % b)    # 2   ← remainder
print(a ** b)   # 1419857  (17 to the power of 5)

# Real example: find if a number is even or odd
num = 16
if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

#### Comparison Operators

These compare values and always return `True` or `False`.

| Operator | Meaning | Example | Result |
|----------|---------|---------|--------|
| `==` | Equal to | `5 == 5` | `True` |
| `!=` | Not equal to | `5 != 3` | `True` |
| `>` | Greater than | `7 > 3` | `True` |
| `<` | Less than | `3 < 7` | `True` |
| `>=` | Greater or equal | `5 >= 5` | `True` |
| `<=` | Less or equal | `4 <= 3` | `False` |

```python
age = 18
print(age >= 18)      # True — can vote!
print(age == 21)      # False
print(age != 0)       # True

x, y = 10, 20
print(x > y)          # False
print(x < y)          # True
```

#### Logical Operators

Combine multiple conditions.

| Operator | Meaning | Example |
|----------|---------|---------|
| `and` | Both must be True | `True and True` → `True` |
| `or` | At least one True | `True or False` → `True` |
| `not` | Reverses True/False | `not True` → `False` |

```python
age = 20
has_id = True

# and — both conditions must be True
if age >= 18 and has_id:
    print("Entry allowed")     # ✅ This prints

# or — at least one condition True
is_member = False
has_coupon = True
if is_member or has_coupon:
    print("You get a discount!")  # ✅ This prints

# not — reverses the condition
is_raining = False
if not is_raining:
    print("Let's go outside!")    # ✅ This prints
```

#### Assignment Operators

| Operator | Example | Same as |
|----------|---------|---------|
| `=` | `x = 5` | Assign 5 |
| `+=` | `x += 3` | `x = x + 3` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 4` | `x = x * 4` |
| `/=` | `x /= 2` | `x = x / 2` |
| `//=` | `x //= 3` | `x = x // 3` |
| `%=` | `x %= 3` | `x = x % 3` |
| `**=` | `x **= 2` | `x = x ** 2` |

```python
score = 100
score += 10      # score is now 110
score -= 5       # score is now 105
score *= 2       # score is now 210
print(score)     # 210
```

---

### 💬 Comments

Comments are notes in your code — Python ignores them. Use them to explain your logic.

```python
# This is a single-line comment

# Calculate the area of a rectangle
length = 10
width = 5
area = length * width   # multiply length and width

"""
This is a
multi-line comment (actually a string, but used as comment)
You can write as many lines as you want here.
"""

print(area)   # Output: 50
```

---

## 🟢 2. Control Flow

### 🔀 if, elif, else

Control flow decides which path your program takes — like a crossroads.

```python
# Basic if-else
marks = 75

if marks >= 90:
    print("Grade: A+")
elif marks >= 80:
    print("Grade: A")
elif marks >= 70:
    print("Grade: B")
elif marks >= 60:
    print("Grade: C")
else:
    print("Grade: F — Study harder!")

# Output: Grade: B
```

**Real-world examples:**

```python
# ATM machine
balance = 5000
withdraw = int(input("Enter amount to withdraw: "))

if withdraw > balance:
    print("Insufficient balance!")
elif withdraw <= 0:
    print("Invalid amount!")
else:
    balance -= withdraw
    print(f"Withdrawn: ₹{withdraw}. Remaining: ₹{balance}")

# Traffic light
light = "green"

if light == "green":
    print("Go! 🚗")
elif light == "yellow":
    print("Slow down ⚠️")
else:
    print("Stop! 🛑")
```

#### Nested Conditions

Conditions inside conditions — like making decisions step by step.

```python
age = 20
has_license = True
is_drunk = False

if age >= 18:
    if has_license:
        if not is_drunk:
            print("You can drive! 🚘")
        else:
            print("You're drunk. No driving!")
    else:
        print("Get a license first!")
else:
    print("Too young to drive!")
```

**Shorthand if (Ternary Operator):**

```python
# One-line if-else
age = 20
status = "Adult" if age >= 18 else "Minor"
print(status)    # Adult
```

---

### 🔁 for loop

A `for` loop repeats something a specific number of times or for each item in a collection.

```python
# Loop through numbers 0 to 4
for i in range(5):
    print(i)     # 0, 1, 2, 3, 4

# Loop through a list
fruits = ["Apple", "Mango", "Banana"]
for fruit in fruits:
    print("I love", fruit)

# Loop with range(start, stop, step)
for i in range(1, 11, 2):   # 1 to 10, step by 2
    print(i)      # 1, 3, 5, 7, 9

# Loop backwards
for i in range(10, 0, -1):
    print(i)      # 10, 9, 8, ... 1

# Multiplication table of 5
for i in range(1, 11):
    print(f"5 × {i} = {5 * i}")
```

---

### 🔄 while loop

A `while` loop keeps running **as long as** a condition is `True`. Like spinning a fan until someone turns it off.

```python
# Count from 1 to 5
count = 1
while count <= 5:
    print(count)
    count += 1    # IMPORTANT: must update, or loop runs forever!

# Guess the number game
import random
secret = random.randint(1, 10)
guess = 0

while guess != secret:
    guess = int(input("Guess (1-10): "))
    if guess < secret:
        print("Too low!")
    elif guess > secret:
        print("Too high!")

print("You got it! 🎉")

# Sum until user enters 0
total = 0
while True:
    num = int(input("Enter number (0 to stop): "))
    if num == 0:
        break
    total += num

print("Total:", total)
```

---

### ⏭️ break, continue, pass

```python
# break — exits the loop immediately
for i in range(10):
    if i == 5:
        break           # stop when i is 5
    print(i)            # prints 0, 1, 2, 3, 4

print("Loop ended at i =", i)

# continue — skips current iteration, moves to next
for i in range(10):
    if i % 2 == 0:
        continue        # skip even numbers
    print(i)            # prints 1, 3, 5, 7, 9

# pass — does nothing (placeholder)
for i in range(5):
    if i == 3:
        pass            # do nothing, continue normally
    print(i)            # prints 0, 1, 2, 3, 4

# pass is useful when you plan to fill in code later
def my_function():
    pass    # TODO: add code here later
```

---

## 🟢 3. Data Structures 🔥

### 📋 List

A list is an **ordered, changeable** collection. Like a shopping list — you can add, remove, and change items.

```python
# Creating a list
fruits = ["Apple", "Mango", "Banana", "Grapes"]
numbers = [1, 2, 3, 4, 5]
mixed = [42, "hello", True, 3.14]   # lists can hold different types!
empty = []

# Indexing (counting starts at 0!)
print(fruits[0])     # Apple   ← first item
print(fruits[1])     # Mango
print(fruits[-1])    # Grapes  ← last item
print(fruits[-2])    # Banana  ← second from last

# Slicing [start:stop:step]
print(fruits[1:3])    # ['Mango', 'Banana']  ← index 1 and 2 (not 3)
print(fruits[:2])     # ['Apple', 'Mango']
print(fruits[2:])     # ['Banana', 'Grapes']
print(fruits[::2])    # ['Apple', 'Banana']   ← every 2nd item
print(fruits[::-1])   # reversed list

# Looping through a list
for fruit in fruits:
    print(fruit)

# Looping with index
for i, fruit in enumerate(fruits):
    print(f"{i}: {fruit}")
```

**List Methods:**

```python
fruits = ["Apple", "Mango"]

fruits.append("Banana")        # Add to end: ['Apple', 'Mango', 'Banana']
fruits.insert(1, "Cherry")     # Insert at index 1: ['Apple', 'Cherry', 'Mango', 'Banana']
fruits.remove("Mango")         # Remove by value: ['Apple', 'Cherry', 'Banana']
popped = fruits.pop()          # Remove & return last: 'Banana'
popped2 = fruits.pop(0)        # Remove & return at index: 'Apple'
fruits.sort()                  # Sort alphabetically
fruits.reverse()               # Reverse the list
print(len(fruits))             # Number of items
print(fruits.count("Cherry"))  # Count occurrences
print(fruits.index("Cherry"))  # Find index
fruits.clear()                 # Remove everything
```

| Method | What it does |
|--------|-------------|
| `append(x)` | Add x to end |
| `insert(i, x)` | Insert x at position i |
| `remove(x)` | Remove first occurrence of x |
| `pop(i)` | Remove and return item at i |
| `sort()` | Sort the list |
| `reverse()` | Reverse the list |
| `len()` | Number of items |
| `index(x)` | Find index of x |
| `count(x)` | Count occurrences of x |
| `clear()` | Remove all items |

---

### 📦 Tuple

A tuple is an **ordered, unchangeable** (immutable) collection. Like a coordinates pair — once set, it stays.

```python
# Creating a tuple
coordinates = (28.6139, 77.2090)    # latitude, longitude of Delhi
colors = ("Red", "Green", "Blue")
single = (42,)      # single item tuple needs a comma!
empty = ()

# Accessing (same as list — indexing and slicing)
print(colors[0])        # Red
print(colors[-1])       # Blue
print(colors[1:])       # ('Green', 'Blue')

# Tuples are IMMUTABLE — cannot be changed
# colors[0] = "Yellow"  ← this would cause an ERROR

# Tuple unpacking
name, age, city = ("Priya", 22, "Mumbai")
print(name)    # Priya
print(age)     # 22

# Swap variables using tuple
a, b = 5, 10
a, b = b, a
print(a, b)    # 10 5

# Convert between tuple and list
my_tuple = (1, 2, 3)
my_list = list(my_tuple)    # Convert to list (now changeable)
my_list.append(4)
my_tuple2 = tuple(my_list)  # Convert back to tuple
print(my_tuple2)             # (1, 2, 3, 4)
```

**List vs Tuple:**

| Feature | List | Tuple |
|---------|------|-------|
| Syntax | `[1, 2, 3]` | `(1, 2, 3)` |
| Changeable? | ✅ Yes (mutable) | ❌ No (immutable) |
| Speed | Slower | Faster |
| Use case | Dynamic data | Fixed data |
| Methods | Many | Few (count, index) |

---

### 🔵 Set

A set is an **unordered collection of unique items**. Like a bag of unique items — no duplicates allowed, no order.

```python
# Creating a set
fruits = {"Apple", "Mango", "Banana", "Apple", "Mango"}
print(fruits)   # {'Apple', 'Mango', 'Banana'} — duplicates removed!

numbers = {1, 2, 3, 4, 5}
empty_set = set()    # Note: {} creates a dict, not a set!

# Add and remove
fruits.add("Grapes")
fruits.remove("Mango")     # Error if not found
fruits.discard("Papaya")   # No error if not found

# Set operations — very powerful!
a = {1, 2, 3, 4, 5}
b = {4, 5, 6, 7, 8}

print(a | b)   # Union: {1,2,3,4,5,6,7,8}      — all items
print(a & b)   # Intersection: {4,5}             — common items
print(a - b)   # Difference: {1,2,3}             — in a, not in b
print(a ^ b)   # Symmetric diff: {1,2,3,6,7,8}  — not in both

# Real-world use: Find common students in two classes
class_A = {"Raj", "Priya", "Arjun", "Neha"}
class_B = {"Priya", "Kiran", "Arjun", "Pooja"}
both = class_A & class_B
print("Students in both:", both)    # {'Priya', 'Arjun'}
```

---

### 📚 Dictionary

A dictionary stores **key-value pairs**. Like a real dictionary: you look up a word (key) to get its meaning (value).

```python
# Creating a dictionary
student = {
    "name": "Rahul",
    "age": 21,
    "city": "Pune",
    "marks": 88.5
}

# Accessing values
print(student["name"])          # Rahul
print(student.get("age"))       # 21
print(student.get("phone", "N/A"))  # N/A (default if key missing)

# Modifying
student["age"] = 22             # Update
student["email"] = "r@mail.com" # Add new key
del student["city"]             # Delete a key

# Looping through dictionary
for key in student:
    print(key, ":", student[key])

for key, value in student.items():
    print(f"{key} → {value}")

# Dictionary methods
print(student.keys())    # All keys
print(student.values())  # All values
print(student.items())   # All key-value pairs

# Nested dictionary
school = {
    "class10A": {"students": 40, "teacher": "Mr. Sharma"},
    "class10B": {"students": 38, "teacher": "Ms. Patel"}
}
print(school["class10A"]["teacher"])   # Mr. Sharma

# Dictionary from two lists (zip)
names = ["Alice", "Bob", "Charlie"]
scores = [85, 92, 78]
result = dict(zip(names, scores))
print(result)   # {'Alice': 85, 'Bob': 92, 'Charlie': 78}
```

---

## 🟢 4. Strings

### ✍️ String Creation

A string is a sequence of characters — any text between quotes.

```python
# Single, double, or triple quotes
s1 = 'Hello'
s2 = "World"
s3 = '''This is a
multiline string'''
s4 = """Another
multiline"""

# Escape characters
print("He said, \"Hello!\"")    # He said, "Hello!"
print("Line1\nLine2")           # Line1 (newline) Line2
print("Tab\there")              # Tab    here
print("Backslash: \\")          # Backslash: \
```

### Indexing & Slicing

```python
text = "Python"
#        0 1 2 3 4 5   ← positive index
#       -6-5-4-3-2-1   ← negative index

print(text[0])      # P
print(text[-1])     # n
print(text[1:4])    # yth  (index 1, 2, 3)
print(text[:3])     # Pyt
print(text[3:])     # hon
print(text[::-1])   # nohtyP (reversed!)
```

### String Methods

```python
msg = "  Hello, World!  "

# Case methods
print(msg.upper())          # "  HELLO, WORLD!  "
print(msg.lower())          # "  hello, world!  "
print(msg.title())          # "  Hello, World!  "
print(msg.capitalize())     # "  hello, world!  "
print(msg.swapcase())       # swap upper/lower

# Strip whitespace
print(msg.strip())          # "Hello, World!"   remove both sides
print(msg.lstrip())         # "Hello, World!  " remove left only
print(msg.rstrip())         # "  Hello, World!" remove right only

# Search and replace
print(msg.replace("World", "Python"))  # "  Hello, Python!  "
print(msg.find("World"))              # 9  (index of 'World', -1 if not found)
print(msg.count("l"))                 # 3  (count occurrences)
print("World" in msg)                 # True  (check if substring exists)

# Split and join
sentence = "apple,mango,banana"
fruits = sentence.split(",")           # ['apple', 'mango', 'banana']
joined = " - ".join(fruits)            # 'apple - mango - banana'

# Check methods
print("hello".isalpha())     # True (all letters)
print("123".isdigit())       # True (all digits)
print("abc123".isalnum())    # True (letters and digits)
print("  ".isspace())        # True (only whitespace)
print("Hello".startswith("He"))  # True
print("Hello".endswith("lo"))    # True
```

### f-Strings (Formatting) 🔥

f-strings are the modern, clean way to embed variables inside strings.

```python
name = "Anita"
age = 25
gpa = 8.75

# Old way (messy)
print("My name is " + name + " and I am " + str(age))

# f-string way (clean!) — just put f before the quote
print(f"My name is {name} and I am {age} years old")
print(f"GPA: {gpa:.2f}")       # 2 decimal places → 8.75
print(f"GPA: {gpa:.1f}")       # 1 decimal place → 8.8
print(f"{name.upper()} rocks!")  # expressions inside {}

# Number formatting
price = 1234567.89
print(f"Price: ₹{price:,.2f}")   # ₹1,234,567.89 (with commas)

# Calculation inside f-string
a, b = 10, 3
print(f"{a} + {b} = {a + b}")   # 10 + 3 = 13
print(f"{a} / {b} = {a/b:.2f}") # 10 / 3 = 3.33
```

---

## 🟡 5. Functions

### 📌 What is a Function?

A function is a reusable block of code with a name. Like a recipe — you write it once and use it whenever you need it.

```python
# Defining a function
def greet():
    print("Hello! Welcome!")

# Calling a function
greet()     # Output: Hello! Welcome!
greet()     # Can call multiple times!
```

### Parameters & Arguments

```python
# Positional arguments — order matters
def add(a, b):
    return a + b

print(add(5, 3))     # 8
print(add(10, 20))   # 30

# Keyword arguments — order doesn't matter
def introduce(name, age, city):
    print(f"I am {name}, {age} years old, from {city}")

introduce(name="Riya", city="Delhi", age=22)   # order changed!

# Default arguments — have a fallback value
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

greet("Raj")           # Hello, Raj!  (uses default)
greet("Priya", "Hi")  # Hi, Priya!   (uses provided value)

# All three together
def order_food(item, quantity=1, size="medium"):
    print(f"Ordering {quantity} {size} {item}")

order_food("Pizza")                   # 1 medium Pizza
order_food("Burger", 2)               # 2 medium Burger
order_food("Sandwich", size="large")  # 1 large Sandwich
```

### *args and **kwargs 🔥

```python
# *args — accept any number of positional arguments (tuple)
def total(*numbers):
    print(numbers)         # (10, 20, 30, 40)  — it's a tuple!
    return sum(numbers)

print(total(10, 20))         # 30
print(total(1, 2, 3, 4, 5))  # 15
print(total(100))            # 100

# **kwargs — accept any number of keyword arguments (dictionary)
def show_info(**details):
    print(details)    # {'name': 'Raj', 'age': 21}
    for key, value in details.items():
        print(f"{key}: {value}")

show_info(name="Raj", age=21, city="Mumbai")

# Using both together
def full_info(*args, **kwargs):
    print("Positional:", args)
    print("Keyword:", kwargs)

full_info(1, 2, 3, name="Alice", score=95)
```

### Return Values

```python
# Return a single value
def square(n):
    return n ** 2

result = square(5)
print(result)     # 25

# Return multiple values (as tuple)
def min_max(numbers):
    return min(numbers), max(numbers)

low, high = min_max([3, 1, 9, 5, 7])
print(f"Min: {low}, Max: {high}")    # Min: 1, Max: 9

# Early return
def divide(a, b):
    if b == 0:
        return "Cannot divide by zero!"
    return a / b

print(divide(10, 2))    # 5.0
print(divide(10, 0))    # Cannot divide by zero!
```

### Lambda Functions

A lambda is a small, one-line anonymous function. Good for simple operations.

```python
# Regular function
def double(x):
    return x * 2

# Lambda equivalent
double = lambda x: x * 2
print(double(5))    # 10

# Lambda with multiple parameters
add = lambda a, b: a + b
print(add(3, 7))   # 10

# Lambda in sorting
students = [("Raj", 85), ("Priya", 92), ("Arjun", 78)]
students.sort(key=lambda s: s[1])    # sort by score
print(students)    # [('Arjun', 78), ('Raj', 85), ('Priya', 92)]
```

---

## 🟡 6. Modules & Packages

### 📦 What is a Module?

A module is a `.py` file with reusable code. Like a toolbox — you import what you need.

### Built-in Modules

```python
# math module
import math

print(math.pi)              # 3.141592653589793
print(math.sqrt(144))       # 12.0
print(math.ceil(4.2))       # 5  (round up)
print(math.floor(4.9))      # 4  (round down)
print(math.factorial(5))    # 120 (5! = 5×4×3×2×1)
print(math.log(100, 10))    # 2.0 (log base 10 of 100)
print(math.pow(2, 10))      # 1024.0

# random module
import random

print(random.random())              # float between 0 and 1
print(random.randint(1, 100))       # int between 1 and 100
print(random.choice([1, 2, 3, 4])) # pick one randomly
items = [1, 2, 3, 4, 5]
random.shuffle(items)               # shuffle in place
print(random.sample(items, 3))      # pick 3 without repeat

# datetime module
from datetime import datetime, date, timedelta

now = datetime.now()
print(now)                          # 2025-03-28 14:30:45.123456
print(now.year, now.month, now.day) # 2025 3 28
print(now.strftime("%d/%m/%Y"))     # 28/03/2025
print(now.strftime("%A, %B %d"))    # Friday, March 28

today = date.today()
birthday = date(2000, 6, 15)
days_lived = (today - birthday).days
print(f"Days lived: {days_lived}")

tomorrow = today + timedelta(days=1)
print("Tomorrow:", tomorrow)
```

### Creating Custom Modules

```python
# File: mytools.py
def greet(name):
    return f"Hello, {name}!"

def add(a, b):
    return a + b

PI = 3.14159

# File: main.py (in same folder)
import mytools

print(mytools.greet("Riya"))   # Hello, Riya!
print(mytools.add(5, 3))       # 8
print(mytools.PI)              # 3.14159

# Import specific items
from mytools import greet, PI
print(greet("Arjun"))    # Hello, Arjun!

# Import with alias
import mytools as mt
print(mt.add(10, 20))   # 30
```

---

## 🟡 7. File Handling

### 📂 Reading and Writing Files

```python
# Writing to a file (creates file if doesn't exist)
with open("notes.txt", "w") as file:
    file.write("Hello, this is line 1\n")
    file.write("This is line 2\n")

# Reading entire file
with open("notes.txt", "r") as file:
    content = file.read()
    print(content)

# Reading line by line
with open("notes.txt", "r") as file:
    for line in file:
        print(line.strip())   # strip removes \n

# Reading all lines into a list
with open("notes.txt", "r") as file:
    lines = file.readlines()
print(lines)    # ['Hello, this is line 1\n', 'This is line 2\n']

# Append to file (doesn't erase existing content)
with open("notes.txt", "a") as file:
    file.write("This is line 3 — appended!\n")
```

**File Modes:**

| Mode | Description |
|------|-------------|
| `"r"` | Read only (default) |
| `"w"` | Write (creates or overwrites) |
| `"a"` | Append (add to end) |
| `"r+"` | Read and write |
| `"rb"` | Read binary (images, etc.) |
| `"wb"` | Write binary |

### Working with CSV

```python
import csv

# Write CSV
data = [["Name", "Age", "City"],
        ["Raj", 22, "Delhi"],
        ["Priya", 25, "Mumbai"]]

with open("people.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerows(data)

# Read CSV
with open("people.csv", "r") as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row["Name"], row["Age"])
```

### Working with JSON

```python
import json

# Write JSON
person = {"name": "Rahul", "age": 25, "skills": ["Python", "ML"]}

with open("data.json", "w") as file:
    json.dump(person, file, indent=4)

# Read JSON
with open("data.json", "r") as file:
    loaded = json.load(file)
    print(loaded["name"])       # Rahul
    print(loaded["skills"])     # ['Python', 'ML']

# Convert dict to JSON string
json_str = json.dumps(person)
print(json_str)

# Convert JSON string to dict
parsed = json.loads('{"name": "Alice", "age": 30}')
print(parsed["name"])   # Alice
```

---

## 🟡 8. Exception Handling

### 🛡️ try, except, finally

Errors happen. Exception handling lets you catch them gracefully instead of crashing.

```python
# Basic try-except
try:
    num = int(input("Enter a number: "))
    result = 100 / num
    print("Result:", result)
except ValueError:
    print("That's not a number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
except Exception as e:
    print(f"Something went wrong: {e}")
finally:
    print("This always runs — cleanup here!")

# Multiple exceptions at once
try:
    x = int("abc")
except (ValueError, TypeError) as e:
    print(f"Error: {e}")

# else clause — runs if NO exception occurred
try:
    n = int("42")
    print("Parsed:", n)
except ValueError:
    print("Invalid!")
else:
    print("No errors! Great!")   # This runs
finally:
    print("Done.")
```

**Common Exception Types:**

| Exception | When it occurs |
|-----------|----------------|
| `ValueError` | Wrong value type (`int("abc")`) |
| `ZeroDivisionError` | Division by zero |
| `FileNotFoundError` | File doesn't exist |
| `IndexError` | Index out of range |
| `KeyError` | Key not in dictionary |
| `TypeError` | Wrong type operation |
| `NameError` | Variable not defined |

### Custom Exceptions

```python
# Create your own exception
class AgeTooLowError(Exception):
    def __init__(self, age):
        self.message = f"Age {age} is too low. Must be 18+"
        super().__init__(self.message)

def check_age(age):
    if age < 18:
        raise AgeTooLowError(age)
    print("Access granted!")

try:
    check_age(15)
except AgeTooLowError as e:
    print("Error:", e)
```

---

## 🟡 9. Object-Oriented Programming (OOP) 🔥

### 🏗️ Class & Object

OOP is a way to model real-world things. A **class** is a blueprint; an **object** is a real thing made from that blueprint.

```
Blueprint (Class) → House Design
Object (Instance) → Actual House built from that design
```

```python
# Define a class
class Dog:
    species = "Canis lupus"   # class attribute (shared by all)

    def __init__(self, name, age):   # constructor — runs when object is created
        self.name = name             # instance attribute (unique to each)
        self.age = age

    def bark(self):
        print(f"{self.name} says: Woof!")

    def info(self):
        print(f"{self.name} is {self.age} years old")

# Create objects (instances)
dog1 = Dog("Bruno", 3)
dog2 = Dog("Max", 5)

dog1.bark()         # Bruno says: Woof!
dog2.info()         # Max is 5 years old
print(Dog.species)  # Canis lupus
```

### Inheritance

A class can **inherit** (reuse) another class's features — like a child inheriting traits from parents.

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def eat(self):
        print(f"{self.name} is eating.")

    def sound(self):
        print("...")

class Cat(Animal):    # Cat inherits Animal
    def sound(self):              # Override parent method
        print(f"{self.name} says: Meow!")

class Dog(Animal):    # Dog inherits Animal
    def sound(self):
        print(f"{self.name} says: Woof!")

    def fetch(self):              # New method only for Dog
        print(f"{self.name} fetches the ball!")

cat = Cat("Whiskers")
dog = Dog("Rex")

cat.eat()     # Whiskers is eating. (from Animal)
cat.sound()   # Whiskers says: Meow! (overridden)
dog.sound()   # Rex says: Woof!
dog.fetch()   # Rex fetches the ball!
```

### Polymorphism

Same method name, different behavior for different classes.

```python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    def area(self):
        return 3.14 * self.radius ** 2

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
    def area(self):
        return self.width * self.height

shapes = [Circle(5), Rectangle(4, 6)]
for shape in shapes:
    print(f"Area: {shape.area()}")   # Each calls its OWN area()
# Area: 78.5
# Area: 24
```

### Encapsulation

Hiding internal details. Use `_` (protected) or `__` (private) prefix.

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.__balance = balance    # private — cannot access directly

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
        else:
            print("Invalid amount or insufficient funds")

    def get_balance(self):
        return self.__balance       # controlled access

acc = BankAccount("Raj", 10000)
acc.deposit(5000)
acc.withdraw(2000)
print(acc.get_balance())     # 13000
# print(acc.__balance)       # ERROR! Cannot access directly
```

### Abstraction

Hiding complex implementation, showing only what's needed. Use `abc` module.

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass

    @abstractmethod
    def stop(self):
        pass

class Car(Vehicle):
    def start(self):
        print("Car engine starts with key 🔑")
    def stop(self):
        print("Car brakes applied 🛑")

class Bicycle(Vehicle):
    def start(self):
        print("Start pedaling the bicycle 🚲")
    def stop(self):
        print("Bicycle stopped by foot brake")

car = Car()
car.start()   # Car engine starts with key 🔑

# vehicle = Vehicle()   # ERROR! Cannot instantiate abstract class
```

---

## 🟠 10. Advanced Python

### ✨ List Comprehension 🔥

A compact way to create lists. Like a smart, one-line for loop.

```python
# Traditional way
squares = []
for i in range(1, 6):
    squares.append(i ** 2)

# List comprehension way
squares = [i ** 2 for i in range(1, 6)]
print(squares)   # [1, 4, 9, 16, 25]

# With condition (filter)
evens = [x for x in range(20) if x % 2 == 0]
print(evens)     # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]

# More examples
words = ["hello", "world", "python"]
upper = [w.upper() for w in words]     # ['HELLO', 'WORLD', 'PYTHON']

# Nested list comprehension
matrix = [[i * j for j in range(1, 4)] for i in range(1, 4)]
print(matrix)    # [[1,2,3],[2,4,6],[3,6,9]]

# Flatten a 2D list
flat = [num for row in matrix for num in row]
print(flat)      # [1, 2, 3, 2, 4, 6, 3, 6, 9]
```

### Dictionary Comprehension

```python
# Square numbers
squares = {x: x**2 for x in range(1, 6)}
print(squares)   # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

# Swap keys and values
original = {"a": 1, "b": 2, "c": 3}
swapped = {v: k for k, v in original.items()}
print(swapped)   # {1: 'a', 2: 'b', 3: 'c'}

# Filter dictionary
marks = {"Raj": 85, "Priya": 92, "Arjun": 55, "Neha": 78}
passed = {name: m for name, m in marks.items() if m >= 60}
print(passed)    # {'Raj': 85, 'Priya': 92, 'Neha': 78}
```

### Generators & yield 🔥

Generators produce values one at a time, saving memory. Use `yield` instead of `return`.

```python
# Normal function returns everything at once
def squares_list(n):
    return [x**2 for x in range(n)]

# Generator — produces one at a time (memory efficient!)
def squares_gen(n):
    for x in range(n):
        yield x ** 2          # pauses here each time

gen = squares_gen(5)
print(next(gen))    # 0
print(next(gen))    # 1
print(next(gen))    # 4

# Or loop through it
for sq in squares_gen(5):
    print(sq)      # 0, 1, 4, 9, 16

# Generator expression (like list comprehension but with ())
gen_exp = (x**2 for x in range(1000000))   # uses almost no memory!
print(next(gen_exp))   # 0

# Infinite generator
def count_up(start=0):
    while True:
        yield start
        start += 1

counter = count_up(1)
for _ in range(5):
    print(next(counter))   # 1, 2, 3, 4, 5
```

### Decorators 🔥

A decorator is a function that **wraps** another function to add extra behavior — without changing the original function's code.

```python
# Basic decorator
def my_decorator(func):
    def wrapper():
        print("--- Before function ---")
        func()
        print("--- After function ---")
    return wrapper

@my_decorator    # This is same as: greet = my_decorator(greet)
def greet():
    print("Hello!")

greet()
# --- Before function ---
# Hello!
# --- After function ---

# Decorator with arguments
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__}...")
        result = func(*args, **kwargs)
        print(f"Done!")
        return result
    return wrapper

@my_decorator
def add(a, b):
    return a + b

print(add(5, 3))
# Calling add...
# Done!
# 8

# Timer decorator (practical example)
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.4f} seconds")
        return result
    return wrapper

@timer
def slow_function():
    time.sleep(1)
    print("Done sleeping")

slow_function()
```

### Closures

A closure is a function that remembers values from its enclosing scope, even after that scope is done.

```python
def make_counter():
    count = 0
    def increment():
        nonlocal count
        count += 1
        return count
    return increment

counter = make_counter()
print(counter())   # 1
print(counter())   # 2
print(counter())   # 3

# Practical: make multiplier functions
def multiplier(x):
    def multiply(y):
        return x * y    # remembers x!
    return multiply

double = multiplier(2)
triple = multiplier(3)

print(double(5))   # 10
print(triple(5))   # 15
```

### Context Managers (with statement)

The `with` statement ensures resources are properly cleaned up.

```python
# File handling (automatic close — even if error occurs)
with open("test.txt", "w") as file:
    file.write("Hello")
# File is automatically closed here

# Custom context manager
class Timer:
    def __enter__(self):
        import time
        self.start = time.time()
        return self

    def __exit__(self, *args):
        import time
        elapsed = time.time() - self.start
        print(f"Time taken: {elapsed:.4f}s")

with Timer():
    # code to time
    sum(range(1000000))
```

---

## 🟠 11. Built-in Functions

### map(), filter(), reduce() 🔥

```python
# map() — apply a function to every item
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, numbers))
print(squared)    # [1, 4, 9, 16, 25]

names = ["raj", "priya", "arjun"]
upper = list(map(str.upper, names))
print(upper)      # ['RAJ', 'PRIYA', 'ARJUN']

# filter() — keep items where function returns True
nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
evens = list(filter(lambda x: x % 2 == 0, nums))
print(evens)      # [2, 4, 6, 8, 10]

# reduce() — combine all items into one value
from functools import reduce
total = reduce(lambda a, b: a + b, [1, 2, 3, 4, 5])
print(total)      # 15   (1+2+3+4+5)

product = reduce(lambda a, b: a * b, [1, 2, 3, 4, 5])
print(product)    # 120  (5 factorial)
```

### zip(), enumerate(), any(), all()

```python
# zip() — pair up multiple iterables
names = ["Raj", "Priya", "Arjun"]
scores = [85, 92, 78]
cities = ["Delhi", "Mumbai", "Pune"]

for name, score, city in zip(names, scores, cities):
    print(f"{name} from {city} scored {score}")

paired = dict(zip(names, scores))
print(paired)   # {'Raj': 85, 'Priya': 92, 'Arjun': 78}

# enumerate() — get index AND value together
fruits = ["Apple", "Mango", "Banana"]
for index, fruit in enumerate(fruits):
    print(f"{index + 1}. {fruit}")
# 1. Apple
# 2. Mango
# 3. Banana

for i, fruit in enumerate(fruits, start=1):  # start index from 1
    print(f"{i}. {fruit}")

# any() — True if at least one is True
print(any([False, False, True]))    # True
print(any([0, 0, 0]))              # False

# all() — True only if ALL are True
print(all([True, True, True]))     # True
print(all([True, False, True]))    # False

# Practical examples
scores = [85, 92, 78, 88]
print(any(s > 90 for s in scores))    # True  (92 > 90)
print(all(s >= 60 for s in scores))   # True  (all passed)
```

---

## 🟠 12. Standard Libraries

### math

```python
import math

print(math.pi)           # 3.14159...
print(math.e)            # 2.71828...
print(math.sqrt(256))    # 16.0
print(math.ceil(4.1))    # 5
print(math.floor(4.9))   # 4
print(math.fabs(-5))     # 5.0 (absolute value)
print(math.gcd(48, 18))  # 6 (greatest common divisor)
print(math.log(1000, 10))# 3.0
print(math.sin(math.pi/2)) # 1.0
print(math.degrees(math.pi)) # 180.0
print(math.radians(180))     # 3.14159...
```

### datetime

```python
from datetime import datetime, date, timedelta

# Current date and time
now = datetime.now()
print(now.strftime("%d %B %Y, %I:%M %p"))  # 28 March 2025, 02:30 PM

# Create specific date
dob = datetime(2000, 6, 15)
age_days = (datetime.now() - dob).days
print(f"Days since birth: {age_days}")

# Add/subtract time
tomorrow = date.today() + timedelta(days=1)
next_week = date.today() + timedelta(weeks=1)
```

### os

```python
import os

print(os.getcwd())                    # current directory
os.makedirs("myfolder", exist_ok=True)  # create folder
print(os.listdir("."))               # list files in current dir
print(os.path.exists("test.txt"))    # check if file exists
print(os.path.join("folder", "file.txt"))  # join paths safely
os.rename("old.txt", "new.txt")      # rename file
os.remove("old.txt")                 # delete file
```

### sys

```python
import sys

print(sys.version)           # Python version
print(sys.platform)          # 'win32', 'linux', 'darwin'
print(sys.argv)              # command line arguments [script_name, arg1, arg2...]
sys.exit(0)                  # exit program with code 0 (success)
```

### collections

```python
from collections import Counter, defaultdict, OrderedDict, deque

# Counter — count occurrences
text = "hello world"
count = Counter(text)
print(count)                          # {'l': 3, 'o': 2, ...}
print(count.most_common(3))           # 3 most common chars

votes = ["A", "B", "A", "C", "B", "A"]
print(Counter(votes))                 # {'A': 3, 'B': 2, 'C': 1}

# defaultdict — dict with default value
dd = defaultdict(int)
dd["apples"] += 1
dd["bananas"] += 3
print(dd)           # defaultdict(<class 'int'>, {'apples': 1, 'bananas': 3})

# deque — double-ended queue (fast appends/pops on both ends)
dq = deque([1, 2, 3])
dq.appendleft(0)   # [0, 1, 2, 3]
dq.append(4)       # [0, 1, 2, 3, 4]
dq.popleft()       # removes 0
dq.pop()           # removes 4
```

### itertools

```python
import itertools

# count — infinite counter
for i in itertools.count(10, 5):    # start=10, step=5
    if i > 30:
        break
    print(i)     # 10, 15, 20, 25, 30

# chain — join multiple iterables
combined = list(itertools.chain([1,2,3], [4,5,6], [7,8,9]))
print(combined)    # [1, 2, 3, 4, 5, 6, 7, 8, 9]

# combinations — all combinations
from itertools import combinations, permutations
print(list(combinations([1,2,3], 2)))   # [(1,2),(1,3),(2,3)]
print(list(permutations("ABC", 2)))     # all 2-char arrangements

# groupby — group consecutive items
from itertools import groupby
data = [("Fruit","Apple"),("Fruit","Mango"),("Veg","Carrot"),("Veg","Potato")]
for key, group in groupby(data, key=lambda x: x[0]):
    items = [g[1] for g in group]
    print(f"{key}: {items}")
```

---

## 🎯 Quick Reference Summary

### Data Structures Comparison

| Feature | List | Tuple | Set | Dictionary |
|---------|------|-------|-----|-----------|
| Syntax | `[ ]` | `( )` | `{ }` | `{k:v}` |
| Ordered | ✅ | ✅ | ❌ | ✅ (Python 3.7+) |
| Changeable | ✅ | ❌ | ✅ | ✅ |
| Duplicates | ✅ | ✅ | ❌ | Keys: ❌ |
| Indexed | ✅ | ✅ | ❌ | By key |
| Use case | General | Fixed data | Unique items | Key-value |

### When to use which?

| Situation | Use |
|-----------|-----|
| Ordered, changeable collection | `list` |
| Fixed data (coordinates, RGB) | `tuple` |
| Unique items, fast lookup | `set` |
| Key-value pairs, lookup by name | `dictionary` |

### Python Zen (Philosophy)

```python
import this   # Run this to see Python's philosophy
```

Key principles:
- Beautiful is better than ugly
- Simple is better than complex
- Readability counts
- There should be one obvious way to do it

---

## 🚀 What to Learn Next?

After mastering these topics, explore:

| Topic | What you can do |
|-------|----------------|
| `NumPy` | Fast number crunching, arrays |
| `Pandas` | Data analysis, Excel-like operations |
| `Matplotlib` | Charts and graphs |
| `Flask/Django` | Build websites |
| `TensorFlow/PyTorch` | Machine Learning |
| `Requests` | Work with APIs and the internet |
| `SQLite/SQLAlchemy` | Databases |

---

*"Every expert was once a beginner. Keep coding, keep learning!"* 🐍✨

---
**Notes compiled by:** Senior Python Developer
**Level:** Beginner → Advanced
**Language:** Python 3.x
