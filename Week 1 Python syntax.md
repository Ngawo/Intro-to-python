### Introduction to Python

Python is a versatile and popular high-level programming language known for its simplicity, readability, and a vast ecosystem of libraries and frameworks.

Key Characteristics of Python:

Readability: Python's syntax is designed to be easily readable, with clean and consistent formatting, which makes it an excellent choice for beginners and experienced programmers alike.

Interpreted Language: Python is an interpreted language, which means you can write and execute code directly without the need for a separate compilation step. This makes development faster and more accessible.

Cross-Platform: Python is available on various operating systems, including Windows, macOS, and Linux, making it easy to write code that runs on multiple platforms.

Large Standard Library: Python comes with a comprehensive standard library that provides modules and functions for a wide range of tasks, reducing the need to reinvent the wheel.


Comments

In programming, comments are a programming language construct used to insert human-readable text in the source code of a program. 

Types of comments

1. Single-Line Comments:

Single-line comments start with the # symbol and continue until the end of the line. They are often used for brief comments on a single line of code.

2. Multi-Line Comments:

Python does not have a built-in syntax for multi-line comments, but you can achieve the same effect by enclosing your comments in triple-quotes (''' or """). This is often used for longer explanations, docstrings, or multi-line comments.


Escape Sequences

 Description                                                                      Token  
Backslash character (\)                                                            \\
New line feed                                                                      \n 
Tab                                                                                \t 
Vertical tab                                                                       \v 
Backspace                                                                          \b
Carriage return                                                                    \r
Single quote (useful in strings enclosed in single quotes: ‘hello \ ‘World’)        \' 
Double quote (useful in strings enclosed in single quotes: “hello \ “World”)        \"

Reserved words in python

False       class       finally     is          return
None        continue    for         lambda      try
True        def         from        nonlocal    while
and         del         global      not         with
as          elif        if          or          yield
assert      else        import      pass
break       except      in          raise

### Variables

Variables are a temporary storage space in a computer’s memory. When a variable’s value changes the program’s current state also changes.
A variable acts as a container to hold a different number of data items or values.

Every variable is created with an initial value. 
A variable can be in three states:

Variable creation (Declaration)
Variable assignment (Initialization)
Variable changed (Execution)

Examples of valid variable names:

c, 
 ref_number,
 admin
& aVeryLongName

Here are a few examples of invalid variable names:

True
$name
12Graph

In Python identifiers are case sensitive, so for example, firstName, FirstName, FIRSTNAME, and firstname are four different identifiers.
A second rule is that variables cannot have the same name as Python’s keywords. 

We can find out what keywords are in Python, by using the function called dir().
If this function is called with the __builtins__ attribute, it returns a list of Python’s built-in attributes.

The __builtins__ module contains all Python’s built-in attributes, which can be used with the dir()function. The ones that are returned are identified with the following characteristics:

Python’s built-in exceptions start with a capital letter.
The rest are either functions or data type names.
Identifiers that start and end with one or two underscores are special methods.

### Casting

In Python, casting refers to the process of converting a value from one data type to another. Python provides several built-in functions for casting, which allows you to change the type of a variable as needed.

In Python, casting can be done both implicitly and explicitly, depending on how the conversion is handled:

1. Implicit Casting (Automatic Type Conversion):
 Implicit casting, also known as automatic type conversion, occurs when the Python interpreter automatically converts one data   type to another when it is necessary for an operation. Python performs implicit casting when it can safely convert one type     to another without data loss or errors.

x = 5   # integer
y = 2.5  # float
result = x + y  # Implicit casting of 'x' to float, result is 7.5 (float)

2. Explicit Casting
Explicit Casting (Type Conversion):

Explicit casting, also known as type conversion, involves using built-in functions like 'int()', 'float()', 'str()', and others to manually convert one data type to another. 
Explicit casting gives you control over the conversion process and is typically used when you need to convert a value from one data type to another intentionally.

x = 3.7  # float
y = int(x)  # Explicitly cast 'x' to an integer, 'y' is 3 (int)

Activity 1

String: A string is a data type in Python used to represent text or characters. Strings are enclosed in single or double quotes, e.g., "Hello, World!".

Integer: An integer is a data type in Python used to represent whole numbers, both positive and negative, without any decimal point, e.g., 42.

Casting from String to Integer: You can convert a string to an integer using the int() function, for example: number = int("42").

Casting from Integer to String: You can convert an integer to a string using the str() function, for example: text = str(42).

Python Naming Conventions: Python has several naming conventions. Variable names should be descriptive, lowercase with words separated by underscores (snake_case), and should not start with a number. For example, total_sum, result, etc.

print("This is how the backslash character is displayed \nin Python \n\\")

print("**** *    * *********  *   *  ****  *    *\n*  *  *  *      *      *   * *    * * *  *\n****   *        *      ***** *    * *  * *\n*      *        *      *   * *    * *   **\n*      *        *      *   *  ****  *    *")

### Data types

Python is a dynamically typed language, which means that variable data types are determined at runtime. Python supports several built-in data types that can be categorized as follows:

1. **Numeric Types**:
   - `int`: Integer type, representing whole numbers (e.g., 42, -10, 0).
   - `float`: Floating-point type, representing real numbers (e.g., 3.14, -0.1, 2.0).

2. **Text Type**:
   - `str`: String type, representing sequences of characters (e.g., "Hello, World!").

3. **Boolean Type**:
   - `bool`: Boolean type, representing `True` or `False` values.

4. **Sequence Types**:
   - `list`: A mutable ordered sequence, which can contain elements of different data types (e.g., `[1, "apple", 3.14]`).
   - `tuple`: An immutable ordered sequence (e.g., `(1, "apple", 3.14)`).
   - `range`: Represents a range of numbers, often used in loops and iteration (e.g., `range(0, 5)`).

5. **Mapping Type**:
   - `dict`: Dictionary type, representing key-value pairs (e.g., `{"name": "John", "age": 30}`).

6. **Set Types**:
   - `set`: An unordered collection of unique elements (e.g., `{1, 2, 3}`).
   - `frozenset`: An immutable version of a set.

7. **Binary Types**:
   - `bytes`: Represents a sequence of bytes (e.g., `b'hello'`).
   - `bytearray`: Mutable version of `bytes`.

8. **None Type**:
   - `None`: Represents the absence of a value or a null value.

9. **Custom Types**:
   - You can create your own custom data types using classes in Python.

Python is highly flexible when it comes to handling data types and type conversions, and you can often perform operations on objects of different data types without explicit casting.

Here are some examples of Python data types and their usage:

```python
# Numeric Types
integer = 42
floating_point = 3.14

# Text Type
string = "Hello, World!"

# Boolean Type
is_true = True
is_false = False

# List
my_list = [1, 2, 3]

# Tuple
my_tuple = (4, 5, 6)

# Dictionary
my_dict = {"name": "Alice", "age": 25}

# Set
my_set = {1, 2, 2, 3}  # Creates a set with unique elements (1, 2, 3)
```

Python's dynamic typing makes it easy to work with a variety of data types and perform dynamic runtime type checking. It's one of the reasons Python is known for its simplicity and readability.

Lambda Expressions

Lambda expressions also known as lambda functions or anonymous functions, are a concise way to create small, anonymous functions in Python. They are often used for simple operations and are particularly handy when you need to pass a function as an argument to another function, such as in the case of map(), filter(), and reduce() functions.

The basic syntax of a lambda expression is: lambda arguments: expression

Simple lambda function with one argument: square = lambda x: x**2 print(square(5)) # Output: 25

Lambda function with multiple arguments: add = lambda x, y: x + y print(add(3, 4)) # Output: 7

Lambda function used with map(): numbers = [1, 2, 3, 4, 5] squared = list(map(lambda x: x**2, numbers)) print(squared) # Output: [1, 4, 9, 16, 25]

Lambda function used with filter(): numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] even_numbers = list(filter(lambda x: x % 2 == 0, numbers)) print(even_numbers) # Output: [2, 4, 6, 8, 10]

Lambda function used with sorted(): names = ['Alice', 'Bob', 'Charlie', 'David', 'Eve'] sorted_names = sorted(names, key=lambda name: len(name)) print(sorted_names) # Output: ['Bob', 'Eve', 'Alice', 'David', 'Charlie']



Python is a dynamically typed language, which means that variable data types are determined at runtime. Python supports several built-in data types that can be categorized as follows:

1. **Numeric Types**:
   - `int`: Integer type, representing whole numbers (e.g., 42, -10, 0).
   - `float`: Floating-point type, representing real numbers (e.g., 3.14, -0.1, 2.0).

2. **Text Type**:
   - `str`: String type, representing sequences of characters (e.g., "Hello, World!").

3. **Boolean Type**:
   - `bool`: Boolean type, representing `True` or `False` values.

4. **Sequence Types**:
   - `list`: A mutable ordered sequence, which can contain elements of different data types (e.g., `[1, "apple", 3.14]`).
   - `tuple`: An immutable ordered sequence (e.g., `(1, "apple", 3.14)`).
   - `range`: Represents a range of numbers, often used in loops and iteration (e.g., `range(0, 5)`).

5. **Mapping Type**:
   - `dict`: Dictionary type, representing key-value pairs (e.g., `{"name": "John", "age": 30}`).

6. **Set Types**:
   - `set`: An unordered collection of unique elements (e.g., `{1, 2, 3}`).
   - `frozenset`: An immutable version of a set.

7. **Binary Types**:
   - `bytes`: Represents a sequence of bytes (e.g., `b'hello'`).
   - `bytearray`: Mutable version of `bytes`.

8. **None Type**:
   - `None`: Represents the absence of a value or a null value.

9. **Custom Types**:
   - You can create your own custom data types using classes in Python.

Python is highly flexible when it comes to handling data types and type conversions, and you can often perform operations on objects of different data types without explicit casting.

Here are some examples of Python data types and their usage:

```python
# Numeric Types
integer = 42
floating_point = 3.14

# Text Type
string = "Hello, World!"

# Boolean Type
is_true = True
is_false = False

# List
my_list = [1, 2, 3]

# Tuple
my_tuple = (4, 5, 6)

# Dictionary
my_dict = {"name": "Alice", "age": 25}

# Set
my_set = {1, 2, 2, 3}  # Creates a set with unique elements (1, 2, 3)
```

Python's dynamic typing makes it easy to work with a variety of data types and perform dynamic runtime type checking. It's one of the reasons Python is known for its simplicity and readability.
