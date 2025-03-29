# Learn Python

## Table of Contents

- [Learn Python](#learn-python)
  - [Table of Contents](#table-of-contents)
  - [General Information](#general-information)
  - [Files](#files)
    - [Python Files](#python-files)
    - [Jupiter Notebooks](#jupiter-notebooks)
  - [Comments](#comments)
  - [Variables](#variables)
  - [Data types](#data-types)
    - [Integers](#integers)
    - [Floats](#floats)
      - [Numeric operations](#numeric-operations)
    - [Strings](#strings)
      - [String methods](#string-methods)
    - [Booleans](#booleans)
    - [Lists](#lists)
      - [List methods](#list-methods)
    - [Tuples](#tuples)
      - [Tuple methods](#tuple-methods)
    - [Sets](#sets)
      - [Set methods](#set-methods)
    - [Lists vs Tuples vs Sets](#lists-vs-tuples-vs-sets)
    - [Dictionaries](#dictionaries)
  - [If statements](#if-statements)
    - [If and else](#if-and-else)
    - [Comparison operators](#comparison-operators)
    - [Logical operators](#logical-operators)
    - [Elif](#elif)
  - [Functions](#functions)
  - [Working with the terminal](#working-with-the-terminal)
  - [Loops](#loops)
    - [For loop](#for-loop)
      - [Enumerate](#enumerate)
    - [While loop](#while-loop)
    - [Break](#break)
  - [Comprenhensions](#comprenhensions)
  - [Try and Except](#try-and-except)
  - [Import Files](#import-files)
  - [\*args and \*\*kwargs](#args-and-kwargs)
  - [Decorators](#decorators)
  - [Classes](#classes)
    - [Attributes](#attributes)
    - [Methods](#methods)
    - [Inheritance](#inheritance)
  - [Type hints](#type-hints)
  - [Virtual Environment](#virtual-environment)
  - [Libraries (dependencies)](#libraries-dependencies)
    - [requirements.txt](#requirementstxt)
    - [Pandas](#pandas)
      - [DataFrames](#dataframes)
      - [Filtering and sorting](#filtering-and-sorting)
      - [Reading and writing files](#reading-and-writing-files)
    - [Scikit-learn](#scikit-learn)
    - [Train and test data](#train-and-test-data)
      - [Pipelines](#pipelines)
      - [Cross Validation](#cross-validation)
      - [Grid search](#grid-search)

## General Information

Python is a high-level programming language that is widely used in data science, machine learning, and many other fields.
Python is known for its simplicity and readability.

To run Python code, you need to have Python installed on your computer.
Install Python from the [official website](https://www.python.org/downloads/).

After installing, you can run python commands from the terminal.
Depending on the operating system, the commands may vary.
The python command can be `python`, `python3`, or `py`.
For simplicity, the command `py` will be used in this document.

To use the command line:

* Windows: Open the command prompt.
* MacOS: Open the terminal.
* Linux: Open the terminal.

To check the installed version of Python, run the following command in the terminal:

```bash
py --version
```

To edit Python files, you can use a text editor like [Visual Studio Code](https://code.visualstudio.com/).
You can also try an online Python interpreter like [Google Colab](https://colab.research.google.com/).
This is a good option if you don't want to install Python on your computer.

## Files

### Python Files

Python files have the extension `.py`.
Imagine you have a file named `filename.py` with the following content:

```python
print("Hello, World!")
```

To run a Python file, use the following command in the terminal:

```bash
py filename.py
```

To run a Python file with arguments, use the following command in the terminal (more about arguments later):

```bash
py filename.py arg1 arg2
```

### Jupiter Notebooks

Jupyter Notebooks are files with the extension `.ipynb`.
These files contain python code, but also text, images, and other elements that make it easier to explain the code.
Jupyter Notebooks are widely used in data science and machine learning.
When using Google Colab, the files are Jupyter Notebooks.

Jupyter Notebooks are made of sections called cells.
One Jupyter Notebook can have multiple cells.
There are two types of cells:

- Code cell: Contains python code. Each code cell can be executed independently.
- Markdown cell: Contains text, images, and other elements.

You can have as many cells as you want.

## Comments

To add comments in Python, use the `#` symbol.
Comments are ignored by the interpreter.

```python
# This is a comment
```

Multi-line comments can be added with triple quotes.

```python
"""
This is
a multi-line
comment
"""
```

## Variables

A variable is a container for storing data.
Think of a variable as a box that contains a value.
Variables in Python are created by assigning a value to a name.

```python
my_number = 5
my_text = "Hello, World!"
```

Variables can have any name, but they cannot start with a number.
Variables are case-sensitive, so `my_variable` and `My_Variable` are different variables.
Always use meaningful names for variables.
In python, the recommended style for variable names is snake_case:

* Lowercase letters
* Words separated by underscores

Variables can change their value during the execution of the program.
Python is a dynamically typed language, so the type of the variable can change.

```python
my_variable = 5
print(my_variable) # 5 is printed in the console
my_variable = "Hello, World!"
print(my_variable) # Hello, World! is printed in the console
```

The `print(my_variable)` is used to output the value of the variable `my_variable` to the console.
Although a variable can be equal to a number, and then to a text, it is not recommended to do this.
It is better to use variables for the same type of data.

## Data types

If variables could only store numbers and text, it would be very limited.
This is why python has different data types.
The following data types can be assigned to variables:

### Integers

The integer data type is used to store whole numbers.

```python
age = 5
age = 10
```

### Floats

The float data type is used to store decimal numbers.

```python
money = 5.0
money = 5.5
```

#### Numeric operations

Numeric operations can be performed with integers and floats.

```python
total = 5 + 10 # addition
total = 5 - 10 # subtraction
total = 5 * 10 # multiplication
total = 5 / 10 # division
total = 5 % 10 # modulus (remainder of the division)
total = 5 ** 10 # exponentiation
total = 5 // 10 # floor division (returns the integer part of the division)
```

### Strings

Strings are used to store text.
Strings are created with single or double quotes.

```python
greeting = "Hello, World!"
greeting = 'Hello, World!'
```

#### String methods

Methods are pieces of code that are attached to objects.
Strings are objects, so they have methods that can be used to manipulate them.
These methods do not change the original variable, they return a modified copy of the variable that can be stored in another variable.
Common string methods are:

```python
greeting = "Hello, World!"
greeting_modified = greeting.upper() # converts to uppercase
greeting_modified = greeting.lower() # converts to lowercase
greeting_modified = greeting.replace("Hello", "Hi") # replaces a part of the string, the result is "Hi, World!"
greeting_length = len(greeting) # returns the length of the string
```

### Booleans

Booleans are used to store `True` or `False` values.

```python
is_student = True
is_underage = False
print(is_student, is_underage) # True False
```

### Lists

Collections are used to store multiple values in a single variable.
Python has multiple types of collections, but the most common one is the list.
Lists are ordered and changeable collections.

```python
my_list = [1, 2, 3, 4, 5]
```

Lists can store different data types.

```python
my_list = [1, "Hello", 3.5]
```

Lists can be nested.

```python
nested_list = [[1, 2], [3, 4], [5, 6]]
```

Lists can be accessed by index.
The first element has the index 0, the second element has the index 1, and so on.
Negative indexes can be used to access elements from the end of the list.

```python
my_list = [1, 2, 3, 4, 5]
the_second_element = my_list[1] # this gets the second element from the list
last_element = my_list[-1] # this gets the last element from the list
```

Elements in a list can be changed.

```python
my_list = [1, 2, 3, 4, 5]
my_list[2] = 10
print(my_list) # [1, 2, 10, 4, 5]
```

Lists can be sliced using [start:stop:step].
The `start` parameter is the index where the slice starts, the default is 0.
The `stop` parameter is the index where the slice ends (not included), the default is the end of the list.
The `step` parameter is the number of elements to skip, it defaults to 1, so no elements are skipped.

```python
sliced = my_list[1:4:2] # [start:stop:step], sliced is [2, 4]
first_three_elements = my_list[:3]
last_three_elements = my_list[2:]
reverse_list = my_list[::-1] # when the step is negative, the list is reversed
copy_of_list = my_list[:] # now copy_of_list has the same elements as my_list but it is a different list
```

#### List methods

Common list methods are:

```python
x = [1, 2, 3, 4, 5]
x.append(6) # adds an element to the end of the list
x.insert(0, 0) # adds an element at a specific position, the first argument is the index, the second argument is the element
x.extend([7, 8, 9]) # adds multiple elements to the end of the list
x.remove(3) # removes an element from the list
x.pop() # removes the last element from the list
x.clear() # removes all elements from the list
x.sort() # sorts the list
x.reverse() # reverses the list
y = x.copy() # copies the list
length = len(x) # returns the length of the list
```

### Tuples

Tuples are ordered and unchangeable (immutable) collections.
Is like a constant list.
The good thing about tuples is that they are faster than lists, so it is a good idea to use them when the data is not going to change.

```python
x = (1, 2, 3, 4, 5)
```

#### Tuple methods

Tuples support most of the list methods, but they do not support the methods that change the elements of the tuple, like `append`, `insert`, `remove`, `pop`, `clear`, `sort`, and `reverse`.

```python
x = (1, 2, 3, 4, 5, 3)
count = x.count(3) # returns the number of times 3 appears in the tuple
index = x.index(3) # returns the index of the first occurrence of 3
second_element = x[1] # returns the second element of the tuple
```

### Sets

Sets are unordered, unindexed, and changeable collections.
Each element in a set is unique, this means that sets are good to remove duplicates from a list.
Sets are efficient and fast.

```python
x = {1, 2, 3, 4, 5}
y = set() # creates an empty set
z = {} # this is a dictionary, not an empty set (more about dictionaries later)
```

If the order of the elements is not 

#### Set methods

Because sets don't have indexes, the elements cannot be accessed by index.
You can access the elements of a set by looping through the set (more about loops later).
Common set methods are:

```python
x = {1, 2, 3, 4, 5}
x.add(6) # adds an element to the set
x.update([7, 8, 9]) # adds multiple elements to the set
x.remove(3) # removes an element from the set
x.discard(3) # removes an element from the set without raising an error
x.pop() # removes a random element from the set
x.clear() # removes all elements from the set
y = x.copy() # copies the set
```

### Lists vs Tuples vs Sets

| List                      | Tuple                     | Set                               |
| ------------------------- | ------------------------- | --------------------------------- |
| Ordered                   | Ordered                   | Unordered                         |
| Changeable                | Unchangeable              | Changeable                        |
| Allows duplicate elements | Allows duplicate elements | Does not allow duplicate elements |
| Use brackets `[]`         | Use parentheses `()`      | Use curly braces `{}`             |
| Slower than tuples        | Faster than lists         | Faster than lists                 |

### Dictionaries

Dictionaries are unordered and changeable collections with key-value pairs.
Notice that keys must be unique and they have to be named with strings.
Dictionaries are used to store data in a structured way.
Think of them like JSON objects if you are familiar with them.

```python
x = {
    "name": "John",
    "age": 30
}
print(x["name"]) # John
```

Each value in a dictionary can be accessed by its key.
Dictionaries can store different data types.

```python
person = {
    "name": "John",
    "age": 30,
    "is_student": True
}
print(x["is_student"]) # True
```

Dictionaries can be nested.

```python
person = {
    "name": "John",
    "age": 30,
    "is_student": True,
    "parents": {
        "mother": "Mary",
        "father": "Joe"
    }
}
print(person["parents"]["mother"]) # Mary
```

## If statements

### If and else

The `if` statement is used to execute a block of code if a condition is true.

```python
is_student = True
if is_student:
    print("The person is a student")
```

The `if` statement can have an `else` block that is executed if the first condition is false.

```python
is_student = False
if is_student:
    print("The person is a student")
else:
    print("The person is not a student")
```

### Comparison operators

Comparison operators are used to compare two values.
The result of a comparison is a boolean value.

```python
x = 5
y = 10
print(x == y) # Are they equal? False
print(x != y) # Are they different? True
print(x > y) # Is x greater than y? False
print(x < y) # Is x less than y? True
print(x >= y) # Is x greater than or equal to y? False
print(x <= y) # Is x less than or equal to y? True
```

### Logical operators

Logical operators are used to combine multiple conditions.
The result of a logical operation is a boolean value.
The `and` operator returns `True` if both conditions are true.

```python
bored = True
has_money = True

if bored and has_money:
    print("Go to the cinema")
else:
    print("Stay at home")
```

The `or` operator returns `True` if at least one of the conditions is true.

```python
sick = False
has_homework = True

if sick or has_homework:
    print("Stay at home")
else:
    print("Go to the cinema")
```

The `not` operator returns `True` if the condition is false.

```python
has_money = True
is_sick = False

if not is_sick and has_money:
    print("Go to the cinema")
else:
    print("Stay at home")
```

Logical operators can be assigned to variables.

```python
bored = True
has_money = True
go_to_cinema = bored and has_money
if go_to_cinema:
    print("Go to the cinema")
else:
    print("Stay at home")
```

### Elif

The `if` statement can have multiple `elif` blocks that are executed if the previous conditions are false.

```python
age = 30
if age < 18:
    print("The person is underage")
elif age < 30:
    print("The person is young") # only printed if the age is between 18 and 29
else:
    print("The person is an adult")
```

## Functions

Python comes with many built-in functions, like `print`, `len`, and many others.
But we can create our own functions using the `def` keyword.
Defining a function does not run the code inside the function.
The code inside a function is executed when the function is called.
The code inside a function is indented, so that the interpreter knows that it is part of the function.

```python
def hello():
    print("Hello, World!")

hello()
```

Functions can have parameters.

```python
def hello(name):
    print("Hello, " + name)

hello("John")
```

Functions can have default parameters.

```python
def hello(name="World"):
    print("Hello, " + name)

hello() # Hello, World
hello("John") # Hello, John
```

Functions can have multiple parameters.

```python
def hello(first_name, last_name):
    print("Hello, " + first_name + " " + last_name)

hello("John", "Doe")
```

Functions have keyword (named) parameters.

```python
def hello(first_name, last_name):
    print("Hello, " + first_name + " " + last_name)

hello(last_name="Doe", first_name="John")
```

Functions can return values.

```python
def add(x, y):
    return x + y

result = add(5, 10)
print(result)

def sum_and_product(x, y):
    return x + y, x * y

sum, product = sum_and_product(5, 10)
print(sum, product) # 15, 50
```

Variables inside a function are local.

```python
x = 5
def change_x():
    x = 10
    print(x)

change_x()
print(x) # 5 because the x inside the function is local
```

To change a global variable inside a function, use the `global` keyword.

```python
x = 5
def change_x():
    global x
    x = 10
    print(x)

change_x()
print(x) # 10
```

This should not be used often because it can make the code harder to understand.

## Working with the terminal

A python file can output text to the terminal using the `print` function.

```python
print("Hello, World!")
```

The `input` function can be used to get input from the user.

```python
name = input("Enter your name: ")
print("Hello, " + name)
```

You can pass arguments to a python file when it is executed from the terminal.

```bash
py filename.py arg1 arg2
```

The `sys` module can be used to get arguments from the terminal.
The `sys.argv` list contains the name of the file and the arguments passed to it when the file is executed from the terminal:

```python
import sys

print(sys.argv) # ['filename.py', 'arg1', 'arg2']
```

This is useful if you need the same script to behave differently depending on the arguments passed to it.
For example, you can create a script that reads a file and prints its content.
You can pass the file name as an argument to the script.

## Loops

### For loop

The `for` loop is used to iterate over a sequence.
It can be used with collections (lists, tuples, sets, dictionaries).
A for loop can be used with a string to iterate over each character.

```python
for x in [0, 1, 2, 3, 4]:
    print(x) # 0, 1, 2, 3, 4
```

Python comes with the `range` function that can be used to generate a sequence of numbers.
The result of the `range` function is not a list, set, or tuple, it is a range object that is used in the for loop.
The `range` function can be used to generate a sequence of numbers.
It can take one, two, or three arguments:

1. `range(stop)`: Generates a sequence from 0 to stop. Stop is not included.
2. `range(start, stop)`: Generates a sequence from start to stop. Start is included, stop is not included.
3. `range(start, stop, step)`: Generates a sequence from start to stop with a step. Start is included, stop is not included.


```python
for x in range(2, 10, 3):
    print(x) # 2, 5, 8
```

#### Enumerate

The `enumerate` function can be used to get the index and the value of the elements in a sequence.

```python
x = ["a", "b", "c"]
for index, value in enumerate(x):
    print(index, value)
```

### While loop

The `while` loop is used to execute a block of code as long as a condition is true.

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

### Break

The `break` statement can be used to stop the loop before it has finished.
If there are nested loops, the `break` statement stops the closest loop.

```python
x = 0
while x < 5:
    print(x)
    if x == 3:
        break
    x += 1

for x in range(5):
    print(x)
    if x == 3:
        break
```

## Comprenhensions

Comprehensions are a concise way to create lists and dictionaries.

```python
a = [i for i in range(5)] # [0, 1, 2, 3, 4]
b = [i + 2 for i in range(5)] # {2, 3, 4, 5, 6}
v = [0 for i in range(5)] # [0, 0, 0, 0, 0]
d = [i for i in range(5) if i % 2 == 0] # [0, 2, 4]
f = {i: i * 2 for i in range(5)} # {0: 0, 1: 2, 2: 4, 3: 6, 4: 8}
```

## Try and Except

The `try` and `except` blocks are used to handle exceptions.
If you think that a block of code can raise an exception, you can put it inside a `try` block.
If the exception is raised, the code inside the `except` block is executed.
The code inside the `finally` block is executed after the `try` and `except` blocks, no matter what.

```python
try:
    x = 5 / 0
except Exception as e:
    print(e)
finally:
    print("This happens no matter what")
```

## Import Files

Separating your code in multiple files is a good practice.
Imagine you have a file named `say_hello.py` with the following function:

```python
def hello():
    print("Hello, World!")
```

Notice that the function is not being called.
To be able to use the `hello()` function in another file, you need to import the `say_hello.py` file.
Create a new file named `main.py` with the following content:

```python
from module import hello

hello()
```

`from say_hello import hello` imports the `hello` function from the `say_hello.py` file.
Now you can call the `hello()` function in the `main.py` file.
If the module is inside a folder, you can import it with the following command:

```python
from folder.say_hello import hello
```

You can run the `main.py` file with the following command: `py main.py`.
You will see "Hello, World!" printed in the console.

We can also change the name of the imported function:

```python
from say_hello import hello as hi

hi()
```

## *args and **kwargs

The `*args` and `**kwargs` are used to pass a variable number of arguments to a function.

```python
def add(*args):
    result = 0
    for arg in args:
        result += arg
    return result

print(add(1, 2, 3, 4, 5)) # 15

def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(key, value)

print_kwargs(name="John", age=30) # name John, age 30
```

## Decorators

Decorators are used to modify the behavior of functions or methods.
A decorator is a function that wraps another function.

```python
import time
def measure_execution_time(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"Execution time: {end - start}")
        return result
    return wrapper

@measure_execution_time
def slow_function():
    time.sleep(2)
    print("Function executed")

slow_function()
```

## Classes

Classes are used to create objects.
A class is a blueprint for objects.

```python
class Wolf:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
wolf = Wolf("Grey", 5)
print(wolf.name) # Grey
```

### Attributes

Classes can have attributes.
The attributes created outside the methods are class attributes, which are shared by all instances of the class.
The attributes created inside the methods are instance attributes, which are unique to each instance of the class.

```python
class Wolf:
    species = "Canis lupus" # class attribute

    def __init__(self, name, age):
        self.name = name # instance attribute
        self.age = age # instance attribute

wolf1 = Wolf("Grey", 5)
print(wolf1.species, wolf1.name, wolf1.age) # Canis lupus, Grey, 5
wolf2 = Wolf("Black", 3)
print(wolf2.species, wolf2.name, wolf2.age) # Canis lupus, Black, 3
```

### Methods

Classes can have methods.
The method that runs when an instance of the class is created is called the constructor or initialiser.
The constructor method is called `__init__`.

```python
class Wolf:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def speak(self):
        print("Awoooooo")

wolf = Wolf("Grey", 5)
wolf.speak() # Awoooooo
```

Notice that the `self` parameter is used to access the attributes and methods of the class.
All methods in a class should have the `self` parameter.
Methods can access the attributes of the class.

```python
class Wolf:
    species = "Canis lupus"

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def speak(self):
        print(f"{self.name} ({self.species}) says Awoooooo")

    def run(self):
        print(f"{self.name} is running")

wolf = Wolf("Grey", 5)
wolf.speak() # Grey (Canis lupus) says Awoooooo
```

### Inheritance

Classes can inherit from other classes.
The class that inherits is called the child class, and the class that is inherited is called the parent class.

```python
class Dog(Wolf):
    species = "Canis lupus familiaris"

    def __init__(self, name, age, breed):
        super().__init__(name, age)
        self.breed = breed

    def speak(self):
        print(f"{self.name} ({self.species}) says Woof")

dog = Dog("Buddy", 3, "Golden Retriever")
dog.speak() # Buddy (Canis lupus familiaris) says Woof
dog.run() # Buddy is running
```

## Type hints

Type hints are used to specify the type of the parameters and the return type of a function.

```python
name: str = "John"
age: int = 30

def describe_person(name: str, age: int) -> str:
    return f"{name} is {age} years old"

class Dog:
    def __init__(self, name: str):
        self.name = name

labrador: Dog = Dog("Buddy")
```

Type hints are not enforced by Python.
They are used to help with code readability and to catch errors early.
The data types are written as follows:

## Virtual Environment

There are different versions of Python, and sometimes you need to use a specific version.
Use virtual environments to avoid conflicts between different versions of Python and libraries (which we'll cover later).
To create a virtual environment, run the following command in the terminal:

```bash
py -m venv envname
```

To activate the virtual environment, run the following command:

```bash
./envname/Scripts/activate
```

To deactivate the virtual environment, run the following command:

```bash
deactivate
```

If you need a different version of Python, first check the installed versions with `py --list`.
You can install all the python versions you need and then create the virtual environment with the desired version.
To create a virtual environment with a specific version of Python, run the following command:

```bash
py -3.8 -m venv envname
```

## Libraries (dependencies)

Python has a lot of libraries that can be used to make your life easier.
These are created by other developers and can be installed with the `pip` command.
Be careful when installing libraries, make sure they are from a trusted source.

A simple example is installing a library that validates email addresses.
To install the `validate_email` library, run the following command in the terminal:

```bash
pip install validate_email
```

To use the library in your code, import it like this:

```python
from validate_email import validate_email

is_valid = validate_email("yo@ejemplo.com")
print(is_valid)
```

### requirements.txt

When you are working on a project, you can create a `requirements.txt` file that contains all the libraries that your project needs.
This is useful when you want to share your project with others, so they can install the dependencies easily and have the same environment as you.
Create a file named `requirements.txt` and add the dependencies.
Notice that the version of the dependencies is optional.

```txt
numpy
pandas==1.0.3
```

To install the dependencies, run the following command:

```bash
pip install -r requirements.txt
```

Then you can check the installed dependencies with the following command:

```bash
pip list
```

### Pandas

Pandas is a library that is widely used in data science.
It is used to manipulate data in a structured way.
To install the pandas library, run the following command in the terminal:

```bash
pip install pandas
```

#### DataFrames

Dataframes are like tables in a database or a spreadsheet.
They are used to store data in rows and columns.
Let's create a simple dataframe:

```python
import pandas as pd

data = {
    "name": ["John", "Jane", "Joe"],
    "age": [30, 25, 35],
    "city": ["New York", "Los Angeles", "Chicago"]
}

df = pd.DataFrame(data)
print(df)
```

This is a simple example of how to use the pandas library.
DataFrames are a powerful tool to store and manipulate data.
You can pass a dictionary to the `pd.DataFrame` function to create a DataFrame.
You can also create a Dataframe inside the DataFrame function.

```python
df = pd.DataFrame(
    [
        ["John", 30, "New York"],
        ["Jane", 25, "Los Angeles"],
        ["Joe", 35, "Chicago"]
    ],
    columns=["name", "age", "city"]
)
```

To get a column from the DataFrame, use the column name as an index.
In Pandas, a column is called a Series.

```python
print(df["name"])
```

To get multiple columns from the DataFrame, use a list of column names.

```python
print(df[["name", "age"]])
```

To get a row from the DataFrame, use the `iloc` method.

```python
print(df.iloc[0]) # returns the first row
print(df.iloc[0, 1]) # returns the first row and the second column
```

To get multiple rows from the DataFrame, use the `iloc` method with a list of indexes.

```python
print(df.iloc[[0, 2]]) # returns the first and third rows
print(df.iloc[0:5]) # returns the first 5 rows
print(df.iloc[2:5, 1:3]) # returns the third to fifth rows and the second to third columns
```

You can set the index of the DataFrame with the `set_index` method to access the rows by the index.

```python
df.set_index("name", inplace=True)
print(df.loc["John"]) # returns the row with the index John
```

To get the maximum value of a column, use the `max` method.

```python
print(df["age"].max())
```

To get the minimum value of a column, use the `min` method.

```python
print(df["age"].min())
```

To see the first 5 rows of the DataFrame, use the `head` method.

```python
print(df.head(5))
```

To see the last 8 rows of the DataFrame, use the `tail` method.

```python
print(df.tail(8))
```

The sample method returns a random sample of the DataFrame.

```python
print(df.sample(2)) # returns 2 random rows
```

#### Filtering and sorting

You can filter the DataFrame with a condition.

```python
print(df[df["age"] > 30])
```

You can also filter using the `query` method.

```python
print(df.query("age > 30"))
```

You can filter the DataFrame with multiple conditions.

```python
print(df[(df["age"] > 30) & (df["city"] == "New York")])
print(df.query("age > 30 and city == 'New York'")) # the same as the previous line
```

You can sort the DataFrame by a column.

```python
print(df.sort_values("age"))
```

To sort the DataFrame in descending order, use the `ascending` parameter.

```python
print(df.sort_values("age", ascending=False))
```

To sort by multiple columns, use a list of column names.

```python
print(df.sort_values(["age", "name"]))
```

To sort by multiple columns in different orders, use a list of tuples.

```python
print(df.sort_values(["age", "name"], ascending=[False, True]))
```

#### Reading and writing files

Pandas can read and write files.
To read a CSV file, use the `read_csv` method.

```python
df = pd.read_csv("filename.csv")
```

To write a DataFrame to a CSV file, use the `to_csv` method.

```python
df.to_csv("filename.csv", index=False)
```

### Scikit-learn

Scikit-learn is a library that is widely used in machine learning.
It is a kit with many tools to work with data and machine learning models.
To install the scikit-learn library, run the following command in the terminal:

```bash
pip install scikit-learn
```

Scikit-learn comes with many datasets that can be used to test machine learning models.
For example, the `load_diabetes` function returns a dataset with information about diabetes.
This dataset is used to predict the progression of diabetes, where the target is a continuous number.
The following is a simple example of how to use the scikit-learn library:

```python
from sklearn.datasets import load_diabetes
from sklearn.ensemble import RandomForestRegressor

diabetes = load_diabetes()
X = diabetes.data
y = diabetes.target

model = RandomForestRegressor(n_estimators=100, random_state=15)
model.fit(X, y)

prediction = model.predict([X[0]])
real_value = y[0]
print(prediction, real_value)
```

The convention is to use `X` for the features and `y` for the target.
Features are the data that is used to make the prediction, like the house size, the number of rooms, and so on.
The target is the data that is being predicted, in this case, the house price.
The `fit` method is used to train the model with the data.

### Train and test data

Data can be split into training and testing data.
This is a good practice to evaluate the model.
A good idea is to use 80% of the data for training and 20% for testing.
The training data is used to train the model, and the testing data is used to test the model.
In the following example we use the testing data to compare the prediction with the real value.

```python
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_diabetes
from sklearn.linear_model import LinearRegression
from matplotlib import pyplot as plt

diabetes = load_diabetes()
X = diabetes.data
y = diabetes.target

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=15)

model = LinearRegression()
model.fit(X_train, y_train)

prediction = model.predict(X_test)

plt.scatter(y_test, prediction)
plt.xlabel('True Values')
plt.ylabel('Predictions')
plt.show()
```

This graph is used to compare the prediction with the real value.
In a perfect scenario, the points would be on a straight line, because the prediction would be the same as the real value.
The closer the points are to the line, the better the model is.
In this case, the graph shows that the model can be improved, but at least we tested it.

In cases where the data is not balanced, for example, when the target has more zeros than ones, it is a good practice to use the `stratify` parameter.
The `stratify` parameter is used to split the data in a way that the proportion of the target is the same in the training and testing data.
Use it when the problem is not a regression problem, but a classification problem, and when the data is not perfectly balanced.

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=15, stratify=y)
```

#### Pipelines

Sometimes we need to process the data before training the model.
Pipelines are used to combine multiple steps, like scaling the data and training the model.
In cases where the features are not in the same scale, it is a good practice to scale the data.
For example, the `StandardScaler` class can be used in cases where the features are normally distributed.
Although the StandardScaler can be used separately, it is a good practice to use the `Pipeline` class to combine the scaler with the model.

```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split

iris = load_iris()
X = iris.data
y = iris.target

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=15)

pipe = Pipeline([
    ("scaler", StandardScaler()),
    ("model", LogisticRegression())
])

pipe.fit(X_train, y_train)
prediction = pipe.predict(X_test)
```

#### Cross Validation

Before we learned how to split the data into training and testing data.
This is a good practice, but it can be improved.
The problem with splitting the data is that we are not sure if the model is good or if we were lucky with the training and testing data.
The `cross_val_score` function can be used to evaluate the model with different training and testing data.
Cross validation divides the data into in groups, and then trains the model with some groups and tests it with the other groups.
This is repeated until all the groups have been used for testing.

```python
from sklearn.model_selection import cross_val_score
from sklearn.linear_model import LinearRegression
from sklearn.datasets import load_diabetes

diabetes = load_diabetes()
X = diabetes.data
y = diabetes.target

model = LinearRegression()
scores = cross_val_score(model, X, y, cv=5)
print(scores)
```

When using cross validation, you may still use the `train_test_split` function to split the data into training and testing data.
In this case you would use the `cross_val_score` function using the training data.
This way you can evaluate the model with the remaining testing data.

#### Grid search

The `GridSearchCV` class can be used to find the best parameters for a model.
We can also use cross validation to evaluate the model, using the `cv` parameter.
The `param_grid` parameter is used to pass the parameters that we want to test.

```python
from sklearn.neighbors import KNeighborsRegressor
from sklearn.preprocessing import StandardScaler
from sklearn.pipeline import Pipeline
from sklearn.model_selection import GridSearchCV
import matplotlib.pyplot as plt
import pandas as pd

boston = pd.read_csv("boston.csv", delimiter=r'\s+', header=None, engine='python')

X = boston.iloc[:, 0:-1]
y = boston.iloc[:, -1]

pipe = Pipeline([
    ("scaler", StandardScaler()),
    ("model", KNeighborsRegressor(n_neighbors=1))
])

param_grid = {
    "model__n_neighbors": [1, 3, 5, 7, 9, 11, 13, 15,  17, 19]
}

grid = GridSearchCV(pipe, param_grid, cv=5)
grid.fit(X, y)

print(grid.best_params_) # prints the best parameters

plt.plot(param_grid["model__n_neighbors"], grid.cv_results_["mean_test_score"])
plt.xlabel("n_neighbors")
plt.ylabel("mean_test_score")
plt.show()
```

The mean test score is used to evaluate the model.
The higher the mean test score, the better the model is.
The graph shows the mean test score for different values of `n_neighbors`.
The best value of `n_neighbors` is the one that has the highest mean test score.