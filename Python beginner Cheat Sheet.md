# Python Beginner Cheat Sheet

Python is a high-level, interpreted, and general-purpose dynamic programming language that focuses on code readability. This cheat sheet provides a quick reference to basic Python syntax.

## Basics

### Variables and Data Types
Variables are used to store data values. Python has various data types including integers, float (decimal numbers), strings, and booleans.

```python
x = 5               # Integer
y = 3.14            # Float
name = "Alice"      # String
is_student = True   # Boolean
```
#### Example Variables and Data Types
```python
# Integer: Whole numbers without a fractional component
age = 25  # An example of an integer variable

# Float: Numbers that contain a decimal point
height = 5.9  # An example of a float variable

# String: A sequence of characters, enclosed in quotes
name = "Alice"  # An example of a string variable

# Boolean: Represents True or False
is_student = True  # An example of a boolean variable

# Printing the variables
print("Name:", name)
print("Age:", age)
print("Height:", height)
print("Is a Student:", is_student)

```
1.  **Integer (`int`)**: `age = 25` - This line creates an integer variable named `age` and assigns it the value `25`.
    
2.  **Float (`float`)**: `height = 5.9` - This line defines a float variable `height` and sets it to `5.9`. Floats are used for numbers that have a decimal point.
    
3.  **String (`str`)**: `name = "Alice"` - This line sets up a string variable `name` with the value `"Alice"`. Strings in Python are surrounded by either single or double quotes.
    
4.  **Boolean (`bool`)**: `is_student = True` - This line creates a boolean variable `is_student` and assigns it the value `True`. Booleans represent one of two values: `True` or `False`.


```properties
console:~$ python file.py
Name: Alice
Age: 25
Height: 5.9
Is a Student: True
```


### Lists

Lists are used to store multiple items in a single variable. Lists are ordered, changeable, and allow duplicate values.

```python
my_list = [1, 2, 3, 4, 5]
```

#### Example Lists

```python
# Creating a list
fruits = ["apple", "banana", "cherry"]

# Accessing list elements
print("First:", fruits[0])  # Output: apple
print("Second:", fruits[1])  # Output: banana
print("Thirth:", fruits[2])  # Output: cherry

# Adding an element to the end of the list
fruits.append("orange")

# Removing an element from the list
fruits.remove("banana")

# Printing the updated list
print("List:", fruits)  # Output: ['apple', 'cherry', 'orange']
```
1.  **Creating a List**: The list `fruits` is created with three elements: "apple", "banana", and "cherry".
    
2.  **Accessing Elements**: Elements in the list are accessed using their index, e.g., `fruits[0]` for the first element.
    
3.  **Modifying the List**:
    
    -   `.append("orange")` adds "orange" to the end of the list.
    -   `.remove("banana")` removes "banana" from the list.
4.  **Printing the List**: Finally, the updated list is printed, showing the current elements after modifications.

```properties
console:~$ python list_example.py
First: apple
Second: banana
Thirth: cherry
List: ['apple', 'cherry', 'orange']
```

### Tuples

Tuples are used to store multiple items in a single variable. A tuple is a collection which is ordered and unchangeable.

```python
my_tuple = (1, 2, 3)
```

#### Example Tuples

```python
# Creating a tuple
my_tuple = (1, 2, 3)

# Accessing tuple elements
print("First element:", my_tuple[0])  # Output: First element: 1
print("Second element:", my_tuple[1]) # Output: Second element: 2
print("Third element:", my_tuple[2])  # Output: Third element: 3

# Length of the tuple
print("Length of tuple:", len(my_tuple))  # Output: Length of tuple: 3
```
1.  **Creating a Tuple**: The tuple `my_tuple` is created with three elements: `1`, `2`, and `3`.
    
2.  **Accessing Elements**: Each element is accessed using its index, e.g., `my_tuple[0]` for the first element.
    
3.  **Tuple Length**: The `len()` function is used to find the number of elements in the tuple.


```properties
console:~$ python tuple_example.py
First element: 1
Second  element: 2
Third  element: 3
Length of tuple: 3
```


### Dictionaries

Dictionaries are used to store data values in key:value pairs. A dictionary is a collection which is ordered*, changeable and does not allow duplicates.

```python
my_dict = {'name': 'Alice', 'age': 25}
```



#### Example Dicts

```python
# Creating a dictionary
my_dict = {'name': 'Alice', 'age': 25}

# Accessing dictionary elements
print("Name:", my_dict['name'])  # Output: Name: Alice
print("Age:", my_dict['age'])    # Output: Age: 25

# Adding a new key-value pair
my_dict['location'] = 'New York'

# Updating an existing key
my_dict['age'] = 26

# Removing a key-value pair
del my_dict['location']

# Printing the updated dictionary
print("Dict:", my_dict)  # Output: {'name': 'Alice', 'age': 26}

```
1.  **Creating a Dictionary**: The dictionary `my_dict` is created with two key-value pairs: `name` set to `"Alice"` and `age` set to `25`.
    
2.  **Accessing Elements**: Values are accessed using their keys, e.g., `my_dict['name']` to access the name.
    
3.  **Modifying the Dictionary**:
    
    -   Adding a new key-value pair with `my_dict['location'] = 'New York'`.
    -   Updating an existing key's value with `my_dict['age'] = 26`.
    -   Deleting a key-value pair with `del my_dict['location']`.
4.  **Printing the Dictionary**: The updated dictionary is printed, showing the current key-value pairs after modifications.


```properties
console:~$ python dict_example.py
Name: Alice
Age: 25
Dict: {'name': 'Alice', 'age': 26}
```


## Control Structures

### If Statements

`if` statements are used for decision-making operations based on a condition.

```python
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```


#### Example if Statement

```python
# Example variable
x = 5

# Using if-elif-else statement
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")

# Change the value of x and test with different values
```
1.  **Variable Definition**: The variable `x` is defined with the value `5`. 
2.  **Conditional Statements**:
    
    -   `if x > 0:` checks if `x` is greater than `0`. If true, it prints `"Positive"`.
    -   `elif x == 0:` is evaluated if the `if` condition is false. It checks if `x` is equal to `0` and prints `"Zero"` if true.
    -   `else:` is the final condition, executed if all previous conditions are false, printing `"Negative"`.
3.  **Testing with Different Values**: You can test the conditional statements by changing the value of `x` and observing the different outputs.

```properties
console:~$ python if_example.py
Positive
```


### For Loops

A `for` loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

```python
for i in range(5):
    print(i)
```

#### Example For Loops

```python
# Using a for loop to iterate over a range
for i in range(5):
    print(i)
```
-   **For Loop**: This loop iterates over a sequence. In this case, `range(5)` generates a sequence of numbers from `0` to `4` (5 numbers in total, starting from 0).
-   **Printing in Each Iteration**: In each iteration, the current value of `i` is printed. `i` takes on the values `0`, `1`, `2`, `3`, and `4` in successive iterations.

```properties
console:~$ python for_loop_example.py
0
1
2
3
4
```




### While Loops

With the `while` loop, we can execute a set of statements as long as a condition is true.

```python
while x < 5:
    print(x)
    x += 1
```

#### Example While Loops

```python
# Initializing the variable
x = 0

# Using a while loop
while x < 5:
    print(x)
    x += 1
```
-   **Initializing the Variable**: Before the loop, we initialize `x` to `0`.
-   **While Loop**: The loop runs as long as `x` is less than `5`. Inside the loop, it prints the current value of `x` and then increments `x` by `1`.
-   **Loop Termination**: When `x` becomes `5`, the condition `x < 5` becomes false, and the loop terminates.ons.

```properties
console:~$ python while_loop_example.py
0
1
2
3
4
```

## Functions

Functions are a block of code which only runs when it is called. You can pass data, known as parameters, into a function.

```python
def greet(name):
    return "Hello, " + name
```
#### Example Functions

```python
# Defining the function
def greet(name):
    return "Hello, " + name

# Using the function
greeting = greet("Alice")
print(greeting)
```
-   **Defining the Function**: The `greet` function is defined with one parameter, `name`. It concatenates `"Hello, "` with the `name` and returns this string.
-   **Using the Function**: The function is then called with the argument `"Alice"`, and the result is stored in the variable `greeting`.
-   **Printing the Result**: Finally, the content of `greeting` is printed, which will display `"Hello, Alice"`.

```properties
console:~$ python function_example.py
Hello, Alice
```

## Classes

Python is an object-oriented programming language. Almost everything in Python is an object, with its properties and methods.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}"
```

#### Example Classes

```python
# Defining the Person class
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}"

# Creating an instance of the Person class
person = Person("Alice", 25)

# Using a method of the Person class
print(person.greet())
```
-   **Defining the Class**: The `Person` class is defined with an `__init__` method to initialize the `name` and `age` attributes, and a `greet` method to return a greeting string.
-   **Creating an Instance**: An instance of `Person` is created with the name `"Alice"` and age `25`.
-   **Using a Class Method**: The `greet` method of the `person` instance is called, which returns and prints `"Hello, my name is Alice"`.

```properties
console:~$ python class_example.py
Hello, my name is Alice
```

## Error Handling

Error handling can be used to notify the user of why the error occurred and gracefully exit the process that caused the error.

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

#### Example Error Handeling

```python
# Attempting a division operation that could cause an error
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```
-   **Try Block**: The code inside the `try` block (`x = 1 / 0`) is an operation that will raise a `ZeroDivisionError` because division by zero is not allowed.
-   **Except Block**: When the error occurs, the control is passed to the `except ZeroDivisionError` block, which handles this specific type of exception. The code inside this block (a print statement) is then executed.
-   **Error Handling**: The script handles the error gracefully by printing "Cannot divide by zero" instead of crashing.

```properties
console:~$ python error_handling_example.py
Cannot divide by zero
```


## Modules and Packages

Modules in Python are simply Python files with a .py extension. A Python module can have a set of functions, classes or variables defined and implemented.

Import a module:

```python
import math
```
#### Example Import a module

```python
# Importing the math module
import math

# Using a function from the math module
result = math.sqrt(16)  # Square root of 16

# Printing the result
print("The square root of 16 is:", result)

```
-   **Importing the Module**: The `math` module, which provides mathematical functions, is imported using `import math`.
-   **Using a Function from the Module**: The `sqrt` function from the `math` module is used to calculate the square root of `16`.
-   **Printing the Result**: The result of the square root calculation is printed.

```properties
console:~$ python math_module_example.py
The square root of 16 is: 4.0
```

Import a specific function:
```python
from math import sqrt
```
#### Example Import a specific function

```python
# Importing only the sqrt function from the math module
from math import sqrt

# Using the imported sqrt function
result = sqrt(25)  # Square root of 25

# Printing the result
print("The square root of 25 is:", result)
```
-   **Importing a Specific Function**: The `sqrt` function is imported directly from the `math` module using `from math import sqrt`. This allows us to use `sqrt` directly without the `math.` prefix.
-   **Using the Imported Function**: The `sqrt` function is used to calculate the square root of `25`.
-   **Printing the Result**: The result, which is the square root of `25`, is printed.

```properties
console:~$ python sqrt_function_example.p
The square root of 25 is: 5.0
```

## File Handling

File handling in Python enables us to read and write files, along with many other file handling options, to work on files.

```python
with open('file.txt', 'r') as file:
    content = file.read()
```

#### Example File handeling

```python
# File handling: Reading from a file
with open('file.txt', 'r') as file:
    content = file.read()

# Printing the content of the file
print(content)
```
-   **Opening the File**: The `with open('file.txt', 'r') as file:` statement opens `file.txt` in read mode (`'r'`). The `with` statement ensures proper acquisition and release of resources, automatically closing the file when done.
-   **Reading from the File**: `file.read()` reads the entire content of the file into the variable `content`.
-   **Printing the Content**: The content of the file is then printed.

```
Asuming that file.txt contains "Hello, world!"
```


```properties
console:~$ python file_handling_example.py
Hello, world!
```
