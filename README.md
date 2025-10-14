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
