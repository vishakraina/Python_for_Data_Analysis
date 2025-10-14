# Python_for_Data_Analysis
Covers all concepts with respect to python for Data analysis and Data Scientist.

# 1. Python Basics - Variables and Keywords Notes

Overview
Introduction to Python variables and keywords, with practical examples from a Jupyter Notebook (Variables & Keywords.ipynb).
Key Points
Variables

Temporary storage for values; no need to declare data types in Python.
Assignment: Use = (e.g., a = 10 assigns 10 to variable a).
Data Types (auto-detected):
Integer: a = 10 → type(a) returns <class 'int'>.
Float: a = 5.5 → type(a) returns <class 'float'>.
String: a = "Hello World" or a = 'Hello World' → type(a) returns <class 'str'>.
Boolean: a = True → type(a) returns <class 'bool'> (Note: a = "True" is a string).


Rules:
Variable names cannot start with numbers (e.g., 5a = 10 → SyntaxError; but a5 = 10 works).
Case-sensitive: name = 2, Name = 4 are different variables.


Type Casting:
Convert types: a = 89.9; a = int(a) → 89 (<class 'int'>).
a = "5.5"; b = float(a) → 5.5 (<class 'float'>); b = int(float(a)) → 5 (<class 'int'>).
a = "hello"; b = int(a) → ValueError (non-numeric strings can't convert to int).
round(89.5, 0) → 90.0; int(89.5) → 89.


Installation:
Download Python from python.org/downloads (e.g., 3.13) or use Anaconda Navigator for bundled tools (Jupyter, Spyder).
Alternative: Use Google Colab for no-install coding with pre-installed Python.
MacOS may have Python pre-installed; verify or install if needed.



Keywords

Reserved words with special meaning (e.g., def, print, type, if, else, continue, break, import, None).
Cannot be used as variable names, but doing so (e.g., type = 10) is possible though not recommended.
In Jupyter Notebook, keywords appear green (e.g., def, print, type).

# 2. Python Data Types, Operators, and Operands Notes

Overview
Introduction to Python data types, operators, and operands, with practical examples from Jupyter Notebook (Datatypes.ipynb).

Key Points
Data Types

Classified into five categories:
Numeric: Integers, floats, complex numbers.
Sequence Types: Strings, lists, tuples.
Dictionaries: Key-value pairs.
Boolean: True/False.
Sets: Unique, unordered collections.


Use type() to check the data type of a variable.

Operators

Symbols used for computations, including:
+ (addition)
- (subtraction)
* (multiplication)
/ (division)
// (floor division)
% (modulus)
** (exponentiation)

Operands

Values that operators act upon in expressions.

Order of Precedence

Follows PEMDAS rule:
Parentheses
Exponentiation
Multiplication/Division
Addition/Subtraction

Installation

Install Python via:
python.org
Anaconda Navigator
Google Colab (no-install option for coding)

Input Function

input() function captures user input, always returning data as a string.


# 3. Lists Notes
Overview
Lists are mutable, ordered sequences of mixed data types, enclosed in square brackets []. They support various operations like indexing, slicing, concatenation, and modification. Tuples, in contrast, are immutable and use parentheses (). This document includes examples from the provided Lists.ipynb and additional code snippets.

Key Points

Lists
Ordered, mutable, allow mixed data types (integers, floats, strings, nested lists).
Defined using square brackets [].
Example:
my_list = [1, 2.5, "hello", [3, 4]]

Tuples
Ordered, immutable, used for fixed data.
Defined using parentheses () or comma-separated values.
Example:
my_tuple = (1, 2, "world")
# or
my_tuple = 1, 2, "world"  # parentheses optional

Sets
Unordered, unique elements.
Defined using curly braces {}.
Example:
my_set = {1, 2, 3, 3}  # Output: {1, 2, 3}
Indexing
Zero-based indexing.
Access elements using list[index].
Negative indexing starts from the end:
fruits = ["apple", "banana", "cherry"]
print(fruits[0])   # apple
print(fruits[-1])  # cherry
Slicing
Extract sublists using list[start:end].
Omitting start → from beginning; omitting end → to end.
numbers = [0, 1, 2, 3, 4, 5]
print(numbers[1:4])  # [1, 2, 3]
print(numbers[:3])   # [0, 1, 2]
print(numbers[3:])   # [3, 4, 5]

Common List Operations:

1. Concatenation → list1 + list2 → Combine two lists
2. Append → list.append(item) → Add item to end
3. Extend → list.extend([items]) → Add multiple items
4. Insert → list.insert(index, item) → Insert at specific position
5. Remove → list.remove(item) → Remove first occurrence
6. Pop → list.pop(index) → Remove and return item
7. Sort → list.sort() → Sort in place
8. Sorted → sorted(list) → Return sorted copy


Mutability
Lists: Elements can be modified after creation.
my_list = [1, 2, 3]
my_list[0] = 99  # OK → [99, 2, 3]

Tuples & Strings: Immutable — cannot change individual elements.

Membership Testing
Use in to check if an element exists:
fruits = ["apple", "banana"]
print("banana" in fruits)  # True

Shallow Copy vs. Reference
Assignment creates a reference:
A = [1, 2, 3]
B = A          # B is a reference to A
A[0] = 99
print(B)       # [99, 2, 3] → changed too!

Create independent copy:

B = A[:]       # slicing
# or
B = A.copy()   # copy() method
# or
import copy
B = copy.copy(A)  # for shallow copy

Tip: Use copy() or slicing [:] to create independent list copies and avoid unintended side effects.
