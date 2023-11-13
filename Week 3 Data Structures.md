### Function Definition

Functions allow you to group a set of statements into a reusable and modular block of code. You can call a function with specific inputs (arguments) and get a specific output (return value).

Here's the basic syntax for defining a function in Python:

```python
def function_name(argument1, argument2, ...):
    # Function body
    # You can include multiple statements here
    result = argument1 + argument2
    return result
```

Let's break down the components of a function definition:

- `def`: This keyword is used to define a function.

- `function_name`: Choose a name for your function. The function name should follow Python's naming conventions (use lowercase letters and underscores for multi-word names). It should also be descriptive of the function's purpose.

- `(argument1, argument2, ...)`: Within the parentheses, you specify the arguments (parameters) that the function expects. These are variables that will receive values when the function is called. You can have zero or more arguments.

- `:`: A colon indicates the start of the function body, which is indented.

- Function body: This is where you write the code that the function will execute. You can include multiple statements to perform a specific task.

- `return`: If you want the function to return a value, use the `return` statement. It specifies the value to be returned to the caller. A function can have multiple `return` statements, but it exits the function as soon as a `return` statement is encountered.

Here's an example of a simple function:

```python
def add_numbers(x, y):
    result = x + y
    return result
```

You can call this function by passing two arguments, like this:

```python
sum_result = add_numbers(3, 4)
print(sum_result)  # This will print 7
```

This function `add_numbers` takes two arguments, adds them together, and returns the result.

Functions are a powerful tool in Python, allowing you to organize and reuse your code, making it more modular and readable. They are used extensively in Python for a wide range of tasks.

### List Comprehensions:

List comprehensions provide a concise way to create lists in Python.

- **Syntax:**
  ```python
  # Basic syntax
  new_list = [expression for item in iterable if condition]
  ```

- **Examples:**
  ```python
  # Squares of numbers from 0 to 9
  squares = [x**2 for x in range(10)]

  # Even numbers from 0 to 9
  evens = [x for x in range(10) if x % 2 == 0]
  ```

### Nested List Comprehensions:

- List comprehensions can be nested inside each other.

- **Example:**
  ```python
  # Nested list comprehension to create a 3x3 matrix
  matrix = [[i + j for j in range(3)] for i in range(3)]
  ```

### The `del` Statement:

- The `del` statement is used to delete items from lists or variables from the local or global scope.

- **Examples:**
  ```python
  my_list = [1, 2, 3, 4, 5]
  del my_list[2]  # Deletes the item at index 2

  x = 10
  del x  # Deletes the variable x
  ```

### Tuples and Sequences:

- **Tuple:** An immutable ordered collection of elements, defined using parentheses.

  ```python
  my_tuple = (1, 2, 3)
  ```

- **Sequence Types:** Tuples, lists, and strings are examples of sequence types.

- **Operations:**
  - Indexing and slicing work similar to lists.
  - Concatenation and repetition are allowed.

### Sets:

- **Definition:** A set is an unordered collection of unique elements.

- **Syntax:**
  ```python
  my_set = {1, 2, 3}
  ```

- **Operations:**
  - Union, intersection, difference, etc.

  ```python
  set1 = {1, 2, 3}
  set2 = {3, 4, 5}

  union_set = set1 | set2  # Union
  intersection_set = set1 & set2  # Intersection
  ```

### Looping Techniques:

- **`enumerate()`:** Iterates over both the index and the element.

  ```python
  for index, value in enumerate(my_list):
      print(f"Index: {index}, Value: {value}")
  ```

- **`zip()`:** Combines elements from multiple iterables.

  ```python
  list1 = [1, 2, 3]
  list2 = ['a', 'b', 'c']

  for num, letter in zip(list1, list2):
      print(f"Number: {num}, Letter: {letter}")
  ```

- **`reversed()`:** Iterates over the elements of a sequence in reverse order.

  ```python
  for item in reversed(my_list):
      print(item)
  ```


### More On Lists

The list data type has some more methods. Here are all of the methods of list objects: 

list.append(x) 
Add an item to the end of the list. Equivalent to a[len(a):] = [x]. 

list.extend(iterable)  
Extend the list by appending all the items from the iterable. Equivalent to a[len(a):] = iterable. 

list.insert(i, x)  
Insert an item at a given position. The first argument is the index of the element before which to insert, so a.insert(0, x) inserts at the front of the list, and a.insert(len(a), x) is equivalent to a.append(x). 

list.remove(x)  
Remove the first item from the list whose value is equal to x. It raises a ValueError if there is no such item. 

list.pop([i]) 
Remove the item at the given position in the list, and return it. If no index is specified, a.pop() removes and returns the last item in the list. (The square brackets around the i in the method signature denote that the parameter is optional, not that you should type square brackets at that position. You will see this notation frequently in the Python Library Reference.) 

list.clear() 
Remove all items from the list. Equivalent to del a[:]. 

list.index(x[, start[, end]]) 
Return zero-based index in the list of the first item whose value is equal to x. Raises a ValueError if there is no such item. 

The optional arguments start and end are interpreted as in the slice notation and are used to limit the search to a particular subsequence of the list. The returned index is computed relative to the beginning of the full sequence rather than the start argument. 

list.count(x) 
Return the number of times x appears in the list. 

list.sort(key=None, reverse=False) 
Sort the items of the list in place (the arguments can be used for sort customization, see sorted() for their explanation). 

list.reverse()  
Reverse the elements of the list in place. 

list.copy() 
Return a shallow copy of the list. Equivalent to a[:]. 

Using Lists as Stacks and Queues

### Creating Lists
How to create a list?
In Python programming, a list is created by placing all the items (elements) inside square brackets [], separated by commas.

It can have any number of items and they may be of different types (integer, float, string etc.).

1. Empty list
my_list = []
 
2. List of integers
my_list = [1, 2, 3]
 
List with mixed data types
my_list = [1, "Hello", 3.4]
A list can also have another list as an item. This is called a nested list.

4. Nested list
my_list = ["mouse", [8, 4, 6], ['a']]

#### Access List Elements
There are various ways in which we can access the elements of a list.

List Index
We can use the index operator [] to access an item in a list. In Python, indices start at 0. So, a list having 5 elements will have an index from 0 to 4.

Trying to access indexes other than these will raise an IndexError. The index must be an integer. We can't use float or other types, this will result in TypeError.

Nested lists are accessed using nested indexing.

#### Using Lists as Stacks and Queues

Negative indexing
Python allows negative indexing for its sequences. The index of -1 refers to the last item, -2 to the second last item and so on.

Negative indexing in lists
my_list = ['p','r','o','b','e']
 
print(my_list[-1])
 
print(my_list[-5])
When we run the above program, we will get the following output:

e
p

Slicing lists in python

How to slice lists in Python?
We can access a range of items in a list by using the slicing operator :(colon).

List slicing in Python
 
my_list = ['p','r','o','g','r','a','m','i','z']
 
elements 3rd to 5th
print(my_list[2:5])
 
elements beginning to 4th
print(my_list[:-5])
 
elements 6th to end
print(my_list[5:])
 
elements beginning to end
print(my_list[:])

Output

['o', 'g', 'r']
['p', 'r', 'o', 'g']
['a', 'm', 'i', 'z']
['p', 'r', 'o', 'g', 'r', 'a', 'm', 'i', 'z']
Slicing can be best visualized by considering the index to be between the elements as shown below. So if we want to access a range, we need two indices that will slice that portion from the list.

Element Slicing from a list in PythonElement Slicing from a list in Python




### Errors and Exceptions
In Python, errors and exceptions are used to handle unexpected situations or errors that may occur during the execution of a program. Understanding how to handle errors is crucial for writing robust and reliable code. Here's an overview of errors and exceptions in Python:

 Types of Errors:

1. **Syntax Errors:**
   - Syntax errors occur when the Python interpreter encounters code that violates the language's rules.
   - These errors are detected during the parsing phase (before the code is executed).
   - They are often caused by typos or incorrect indentation.

   ```python
   # Example of a syntax error
   print("Hello, world!"
   ```

2. **Runtime Errors (Exceptions):**
   - Runtime errors occur during the execution of a program when something unexpected happens.
   - These errors are not detected until the program is running.
   - Common runtime errors include:
     - `ZeroDivisionError`: Division or modulo by zero.
     - `TypeError`: Inappropriate use of a data type.
     - `NameError`: Attempt to access an undefined variable or function.
     - `FileNotFoundError`: Attempt to open a file that doesn't exist.

   ```python
   # Example of a runtime error
   x = 10 / 0  # ZeroDivisionError
   ```

### Handling Exceptions:

To handle exceptions and prevent your program from crashing, you can use the `try`, `except`, `else`, and `finally` blocks.

- **`try` and `except`:**
  ```python
  try:
      # code that may raise an exception
      result = 10 / 0
  except ZeroDivisionError:
      # code to handle the exception
      print("Cannot divide by zero!")
  ```

- **`else` block (optional):**
  ```python
  try:
      result = 10 / 2
  except ZeroDivisionError:
      print("Cannot divide by zero!")
  else:
      # code to execute if no exception is raised
      print(f"Result: {result}")
  ```

- **`finally` block (optional):**
  ```python
  try:
      result = 10 / 2
  except ZeroDivisionError:
      print("Cannot divide by zero!")
  else:
      print(f"Result: {result}")
  finally:
      # code to execute regardless of whether an exception is raised or not
      print("Execution complete.")
  ```

### Raising Exceptions:

You can also explicitly raise exceptions using the `raise` statement.

```python
def sqrt(x):
    if x < 0:
        raise ValueError("Cannot calculate square root of a negative number")
    else:
        return x ** 0.5

try:
    result = sqrt(-4)
except ValueError as ve:
    print(ve)
```

### Custom Exceptions:

You can define your own exception classes by inheriting from the `Exception` class or one of its subclasses.

```python
class MyCustomError(Exception):
    pass

try:
    raise MyCustomError("This is a custom exception")
except MyCustomError as e:
    print(f"Caught an exception: {e}")
```


### Classes In Python 
classes are a fundamental part of object-oriented programming (OOP). They allow you to structure your code in a way that promotes modularity, reusability, and maintainability.

Defining a Class:
You can define a class using the `class` keyword. The basic syntax looks like this:

```python
class MyClass:
    # class attributes and methods go here
    pass
```

### Class Attributes:

Class attributes are variables that are shared by all instances of a class. They are defined outside of any method in the class.

```python
class MyClass:
    class_attribute = 10

# Accessing the class attribute
print(MyClass.class_attribute)
```

### Instance Attributes:

Instance attributes are variables that are unique to each instance of a class. They are defined inside the class's methods using `self`.

```python
class MyClass:
    def __init__(self, instance_attribute):
        self.instance_attribute = instance_attribute

# Creating an instance of the class
obj = MyClass(instance_attribute=20)

# Accessing the instance attribute
print(obj.instance_attribute)
```

### Methods:

Methods are functions defined within a class. They can operate on the class's attributes and are called on instances of the class.

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    def display_value(self):
        print(f"The value is: {self.value}")

# Creating an instance of the class
obj = MyClass(value=42)

# Calling a method
obj.display_value()
```




```python

```
