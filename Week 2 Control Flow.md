### CONTROL FLOW STATEMENTS

A program’s control flow is the order in which the program’s code executes.

The control flow of a Python program is regulated by conditional statements, loops, and function calls.

Python has three types of control structures:

·   Sequential - default mode

·   Selection - used for decisions and branching

·   Repetition - used for looping, i.e., repeating a piece of code multiple times.

1. Sequential 

Sequential statements are a set of statements whose execution process happens in a sequence. The problem with sequential statements is that if the logic has broken in any one of the lines, then the complete source code execution will break.

Sequential control structure

statement1
statement2
statement3

2. Selection Statement

In Python, the selection statements are also known as Decision control statements or branching statements.
The selection statement allows a program to test several conditions and execute instructions based on which condition is true.

Some Decision Control Statements are:

Simple if - A simple if statement is used to execute a block of code if a specified condition is True. If the condition is False, the block of code is skipped, and the program continues with the next statements. 

x = 10

if x > 5:
    print("x is greater than 5")
    
print("This is outside the if block")

if-else - The if-else statement evaluates the condition and will execute the body of if if the test condition is True, but if the condition is False, then the body of else is executed.

x = 7

if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
    
print("This is outside the if-else block")

nested if - Nested if statements are an if statement inside another if statement.

x = 10
y = 5

if x > 5:
    print("x is greater than 5")
    
    if y > 2:
        print("y is also greater than 2")

print("This is outside the nested if statement")

if-elif-else - The if-elif-else statement is used to conditionally execute a statement or a block of statements.

x = 3

if x > 5:
    print("x is greater than 5")
elif x > 2:
    print("x is greater than 2 but not greater than 5")
else:
    print("x is not greater than 5 or 2")

print("This is outside the if-elif-else block")

3. Repetition

A repetition statement is used to repeat a group(block) of programming instructions.

In Python, we generally have two loops/repetitive statements:

for loop

while loop

For loop: A for loop is used to iterate over a sequence that is either a list, tuple, dictionary, or a set. We can execute a set of statements once for each item in a list, tuple, or dictionary.
It's typically used when you know the number of iterations in advance or when you want to perform a specific action for each item in the sequence.

While loops are used to execute a block of statements repeatedly until a given condition is satisfied. Then, the expression is checked again and, if it is still true, the body is executed again. This continues until the expression becomes false.
It's useful when you don't know in advance how many times you need to iterate and want to keep looping as long as a certain condition holds.

Here's a simple comparison of the two loop types:

Use a for loop when you have a finite sequence to iterate over, and you know the number of iterations in advance.
Use a while loop when you want to repeat a block of code until a specific condition is met, and you don't necessarily know how many iterations will be required.
Loops are essential for performing tasks that involve repetition, such as iterating through lists, processing data, or implementing game logic. They help you automate tasks and make your code more efficient.


### PYTHON FUNCTIONS

We create functions by providing three pieces of information. The name of the function, a list of zero or more parameters, and, optionally, a block of code which provides the return value (a function can return nothing).

We must make a firm distinction between an argument value and a parameter:

Argument

The argument is the object used in an application of a function; it may be referenced by other variables or objects.

Parameter

The parameter is a variable name that is part of the function and is a local variable within the function body.

 
There are three types of functions in Python:

Ordinary functions - are functions that follow mathematical procedures. They will receive an argument, perform a specific calculation with the argument, and return a result.

Procedure functions - normally do not return a result; they are called to execute a procedure. For example a function can be created to set up a connection to a database.

Factory functions - do not take parameters. The function generates values. Some factory functions work by accessing an object encapsulated in a module. For example, you will access the random number generator encapsulated in the random module.

Random Modules

The random module in Python is a built-in library that provides functions for generating random numbers and performing randomization-related tasks. This module is useful for a wide range of applications, including simulations, games, cryptography, and more. Here are some of the key functions and features provided by the random module:

Generating Random Numbers:

random.random(): Returns a random float between 0 and 1 (exclusive of 1).
random.uniform(a, b): Returns a random float between a and b (inclusive of a and exclusive of b).
random.randint(a, b): Returns a random integer between a and b (inclusive of both a and b).
random.randrange(start, stop, step): Returns a randomly selected element from the specified range with an optional step.

Random Functions

randint(self, x, y)
Return random integer in range [x, y], including both end points.

sample(self, popu, i)
Chooses i unique random elements from a population sequence or set.
Returns a new list containing elements while leaving the original population unchanged. (Lists are explained in Unit 2.)
The resulting list is in selection order. For example, 12, 45, 32, 16, 1

choice(self, seq)
Choose a random element from a non-empty sequence.

randrange(x,y)
Return random integer in range [x, y), including x but excluding y.

Recursive functions
 

Recursion in programming is a method where the solution to a problem depends on the same solution’s result.

 

A recursive function calls itself when it is executed.

 

The following example uses a recursive function called Fibonacci.

 

In the Fibonacci sequence of numbers, each number is the sum of the previous two numbers, starting with 0 and 1. This sequence begins 0, 1, 1, 2, 3, 5, 8, 13, 21, 34…


## INTRODUCTION TO MODULES

Modules are the pre-defined files that contain the python codes which depict the basic functionalities of class, methods, variables, etc. It consists of different functions, classes in a group of files inside a directory. Modules can also be termed as Libraries. These are basically the pre-defined methods that can be used to make the code more efficient and reduce redundancy.

Modules bind the code and reduce the repetitions of functions frequently used in the code. Thus, it makes the code much clear and easy to understand.

Examples:

· OS

· Time

· Math

·  MatPlotlib

Mechanism of Python Modules

The moment a module is imported through a program, Python Interpreter fetches the module from either of the following locations:

Program Directory
The directory in the PYTHONPATH variable

Default directory

Listing of Modules
The list of available modules in Python can be found out by executing the following command in the command prompt (interpreter shell).

 Importing modules from Python Standard path
Syntax:

import module_name

Example:

import math

Importing Modules from other Sources
To fetch and use modules from other and new sources, we need to install Python PIP.

Python pip is a software that installs python modules from an index or using a manager like Anaconda.

Run the following command to install modules from new sources using python pip:

python -m pip3 install module_name

Run the following command to install modules from new sources using Ananconda:

conda install module_name

### Difference between a module and a package in Python
Python Module: These are set of pre-defined files that contain the python codes which depict the basic functionalities of class, methods, variables, etc.

Python Package: It is a directory that holds and contains modules and sub-packages.

In Python, regular expressions are used to work with patterns and flags when dealing with text data. The `re` module is the standard library module for working with regular expressions in Python. Here's how you can use patterns and flags with regular expressions in Python:

### Patterns:

A regular expression pattern in Python is a string that defines a search pattern. Patterns can contain special characters and metacharacters for more advanced matching. For example, to match an email address in a string, you can use the following pattern:

```python
import re

text = "Hello, my email is john@example.com and Mary's email is mary@example.com"
pattern = r'[\w.-]+@[a-z]+\.[a-z]+'

matches = re.findall(pattern, text)
print(matches)  # Outputs: ['john@example.com', 'mary@example.com']
```

In this example, the `r` before the pattern string denotes a raw string, which is often used to avoid unwanted escaping of backslashes.

### Flags:

Flags in Python are used to modify the behavior of regular expressions. They can be specified as optional arguments when calling the `re.compile()` or `re.search()` functions, or as part of the regular expression pattern.

Here are some common flags and how to use them:

- `re.I` or `re.IGNORECASE`: Makes the pattern matching case-insensitive.
  
  ```python
  pattern = re.compile(r'example', re.IGNORECASE)
  ```

- `re.M` or `re.MULTILINE`: Allows matching patterns across multiple lines in the input text.
  
  ```python
  pattern = re.compile(r'^\d+', re.MULTILINE)
  ```

- `re.S` or `re.DOTALL`: Makes the dot (.) metacharacter match any character, including newline characters.
  
  ```python
  pattern = re.compile(r'.+', re.DOTALL)
  ```

- `re.U` or `re.UNICODE`: Enables matching and processing of Unicode characters.

  ```python
  pattern = re.compile(r'[\p{L}\p{N}]+', re.UNICODE)
  ```

You can also combine multiple flags using the `|` (bitwise OR) operator.

```python
pattern = re.compile(r'example', re.IGNORECASE | re.MULTILINE)
```

The `re.findall()` function is commonly used to find all matches in a given string, as shown in the earlier example.

Patterns and flags in Python's `re` module provide a powerful way to work with text data and perform various search and manipulation operations on strings, making it a valuable tool for text processing and analysis.


```python

```
