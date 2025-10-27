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

# 4 Tuples Notes

## Overview
Tuples are ordered, immutable sequences of mixed data types, defined with parentheses `()` or comma-separated values.  
They are similar to lists but immutable, making them suitable for fixed data.  
This document summarizes tuple characteristics, differences from lists, and practical examples from the provided code and transcript.

## Key Points

- **Tuples**: Ordered, immutable, allow mixed data types (integers, floats, strings, nested tuples/lists). Defined with parentheses `()` or commas.  
- **Lists**: Ordered, mutable, defined with square brackets `[]`.  

### Differences Between Tuples and Lists
- **Syntax**: Tuples use `()`, lists use `[]`.  
- **Mutability**: Tuples are immutable (cannot change elements), lists are mutable.  
- **Methods**: Tuples have ~33 methods, lists have 40+.  
- **Use Cases**: Use tuples for fixed data (e.g., passport details), lists for dynamic data (e.g., customer info).  
- **Dictionary Keys**: Tuples are hashable (can be dictionary keys), lists are not.  

### Indexing and Slicing
- **Indexing**: Zero-based (e.g., `tuple[0]`) or negative (e.g., `tuple[-1]` for the last element).  
- **Slicing**: Extract sub-tuples (e.g., `tuple[0:2]`).  

### Operations
- **Concatenation**: Use `+` to combine tuples.  
- **Functions**: `min()`, `max()`, `sum()`.  
- **Membership**: Use `in` to check if an element exists in a tuple.  

### Immutability
- Elements cannot be modified directly.  
- To update, use concatenation or **type casting** (convert to list, modify, and convert back to tuple).  

### Sorting
- Tuples cannot be sorted in place.  
- Convert to list, sort, then convert back to tuple.  

### Nested Tuples/Lists
- Tuples can contain other tuples or lists as elements.


# 5. Sets Notes 

## Overview
Sets are **unordered collections of unique elements**, defined with **curly braces `{}`**.  
They are ideal for tasks requiring **distinct values**, such as finding unique items or performing **set operations** like union, intersection, and difference.

This document summarizes **set characteristics**, **comparisons with lists and tuples**, and **practical examples** from the provided `sets.ipynb` and transcript.

---

## Key Points

- **Sets**  
  - Unordered  
  - Mutable (can add or remove elements)  
  - Contain only unique elements  
  - Defined with curly braces `{}`  

- **Lists**  
  - Ordered  
  - Mutable  
  - Allow duplicates  
  - Defined with square brackets `[]`

- **Tuples**  
  - Ordered  
  - Immutable  
  - Allow duplicates  
  - Defined with parentheses `()` or commas  

---

## Key Characteristics

- Sets **do not allow duplicates** — converting a list to a set automatically removes duplicates.  
- Sets are **unordered**, so **indexing (e.g., `set[0]`) is not supported**.  
- **Membership testing (`in`)** is faster in sets because they use **hash tables** internally.  
- Sets support various **mathematical operations**:
  - **Union (`|`)** — Combines all unique elements from both sets.  
  - **Intersection (`&`)** — Elements common to both sets.  
  - **Difference (`-`)** — Elements in one set but not in the other.  
  - **Symmetric Difference (`^`)** — Elements present in either set but not both.

---

## Use Cases

- Removing duplicates from data collections.  
- Checking **unique elements** in datasets (e.g., unique grades, user IDs).  
- Performing **set operations** for comparisons or filtering common elements.  
- Efficient **membership testing** — e.g., checking if a value exists in a dataset.

---

## Comparison Table

| Feature              | List                 | Tuple                | Set                   |
|----------------------|----------------------|----------------------|------------------------|
| Ordered              | ✅ Yes               | ✅ Yes               | ❌ No                  |
| Mutable              | ✅ Yes               | ❌ No                | ✅ Yes                 |
| Allows Duplicates    | ✅ Yes               | ✅ Yes               | ❌ No                  |
| Syntax               | `[]`                 | `()` or commas       | `{}`                  |
| Indexing Supported   | ✅ Yes               | ✅ Yes               | ❌ No                  |
| Hashable             | ❌ No                | ✅ Yes               | ❌ No (cannot be keys) |

---

## Summary

Use:
- **Lists** for ordered, changeable collections with duplicates.  
- **Tuples** for fixed, immutable collections.  
- **Sets** for unique, unordered data and efficient membership testing.  

> **Note:** Sets are **not hashable**, so they **cannot be used as dictionary keys**, whereas tuples can.


# 6. Loops and Iterations Notes

## Overview
Loops in Python are used for repetitive tasks, iterating over iterables like lists, tuples, strings, dictionaries, and sets.  
This document covers the basics of loops (**for** and **while**), conditional statements (**if**, **elif**, **else**), and comprehensions, with practical examples from the provided transcript and `loops.ipynb`.

## Key Points

- **Iterables**: Objects that can be iterated over (e.g., lists, tuples, strings, dictionaries, sets).  
- **Iterator**: A variable that traverses each element in an iterable.  

### Loop Types
- **For Loop**: Iterates over a sequence or range, executing until the sequence is exhausted.  
- **While Loop**: Executes as long as a condition is true, requiring manual counter updates.  

### Conditional Statements
- **if**, **elif**, **else** are used for decision-making based on conditions.  

### Comprehensions
- Concise alternatives to `for` loops for creating lists or dictionaries, faster and more compact.  

### Key Features
- `for` loops automatically handle iteration (no manual increment like `i++` in other languages).  
- Comprehensions reduce code length and improve performance compared to traditional `for` loops.  
- Use `.items()` for dictionary iteration to access keys and values.  

> Conditional statements are often used within loops for complex logic.

# 7. Functions Notes

## Overview  
Functions in Python are **named sequences of statements** that perform specific tasks, improving code **reusability** and **modularity**.  
This document covers **user-defined functions**, **lambda functions**, and their applications, with examples from the provided transcript and `functions.ipynb`.  
It also highlights the differences between **traditional** and **lambda functions**, emphasizing their **use cases** and **benefits**.

---

## Key Points

- **Functions:** Named blocks of code that execute specific tasks when called, defined using the `def` keyword.

### Types of Functions
- **Built-in Functions:** Predefined in Python (e.g., `type()`, `len()`, `int()`).
- **User-Defined Functions:** Created by developers to perform custom tasks (e.g., calculating BMI or checking even/odd).
- **Lambda Functions:** Small, anonymous functions defined with the `lambda` keyword, ideal for single-expression tasks.

---

### Function Components
- **Name:** Unique identifier for the function (e.g., `even_odd`).
- **Arguments:** Inputs passed to the function (optional, can have default values).
- **Body:** Code block that performs the task.
- **Return:** Optional output of the function.

---

### Lambda Functions
- **Syntax:**  
  ```python
  lambda arguments: expression
  ```
- Contain a **single expression**, no multi-line logic.  
- Reduce code complexity and improve performance for simple operations.

---

### Why Use Functions
- **Reusability:** Call functions multiple times without rewriting code.  
- **Modularity:** Organize code into manageable, reusable blocks.  
- **Maintainability:** Easier to update and deploy code in production environments.

---

### Default Arguments
Allow functions to use preset values if arguments are not provided.

---

## Use Cases
- Calculating **factorials**  
- Summing **natural numbers**  
- Checking **conditions** (e.g., even/odd)  
- Simplifying **repetitive tasks**

---

# 8. Map, Reduce, and Filter Functions Notes

## Overview  
Map, reduce, and filter functions are **functional programming tools** in Python that simplify code by reducing the need for explicit loops and branching.  
They are efficient alternatives to traditional `for` loops, offering concise syntax and lower computational overhead.  
This document summarizes their **definitions**, **use cases**, and examples from the provided transcript and `map_reduce_filter.ipynb`.

---

## Key Points

- **Map, Reduce, Filter:** Built-in functions for processing iterables (e.g., lists, tuples) in a functional programming style.  
  - **Map:** Applies a function to each element in an iterable, returning a new collection.  
  - **Filter:** Extracts elements from an iterable that satisfy a condition.  
  - **Reduce:** Combines elements of an iterable into a single result using pairwise operations.

---

### Benefits
- Reduce code length and complexity compared to `for` loops.  
- Improve performance (lower time complexity) for certain tasks.  
- Enhance readability with concise, expressive syntax.

---

### Syntax
- **Map:** `map(function, iterable)`  
- **Filter:** `filter(function, iterable)`  
- **Reduce:** `reduce(function, iterable)` *(requires `from functools import reduce`)*

---

### Lambda Functions
Often used with `map`, `filter`, and `reduce` to define **inline operations**, reducing the need for named functions.

---

### Use Cases
- **Map:** Transform data (e.g., convert strings to uppercase, compute areas).  
- **Filter:** Extract elements based on conditions (e.g., values above average, non-null values).  
- **Reduce:** Aggregate data (e.g., multiply or sum all elements).

---

### Notes
- `reduce` is **deprecated** in Python’s built-in namespace but available in the `functools` module.  
- These functions are less common in **data analytics** but useful for specific tasks.  
- Always convert map/filter results to a list (e.g., `list(map(...))`) to view output.

---

# 9. File Handling Notes

## Overview  
File handling in Python involves operations like **creating, reading, writing, updating, and deleting files**.  
It is crucial for **web applications** and certain programming tasks, though **data science** often relies on libraries like **pandas** for file operations.  
This document summarizes file handling methods, modes, and best practices, with examples from the provided transcript and `file_handling.ipynb`.

---

## Key Points

- **File Handling:** The process of managing files (e.g., reading, writing, appending) in Python.

### Key Operations
- **Open:** Access a file with a specified mode (e.g., read, write, append).  
- **Read:** Retrieve content from a file.  
- **Write:** Add or overwrite content in a file.  
- **Append:** Add content to the end of a file.  
- **Close:** End the file session to free resources.

---

### File Modes
- `'r'`: Read (default, fails if file is not readable).  
- `'w'`: Write (overwrites file, fails if file is not writable).  
- `'a'`: Append (adds to end of file).  
- `'a+'`: Append and read (allows both appending and reading).

---

### Best Practices
- Always **close files** after operations to free resources (`file.close()` or use `with` statement).  
- Use `with` statement for **automatic file closure**.  
- Specify correct **permissions** to avoid errors (e.g., cannot read a file opened in `'w'` mode).  
- Use `\n` to add **line breaks** when writing/appending.

---

### Pandas for Data Science
Libraries like **pandas** simplify file reading (e.g., CSVs, Excel) compared to traditional file handling.

---

# 10. Control Structures Notes

## Overview  
Control structures in Python guide program flow by analyzing variables and making decisions based on conditions or iterating over data.  
This document covers **binary and relational operators**, **decision-making with if-else**, **iteration with loops**, **comprehensions**, and **functional programming tools (map, filter, reduce)**, with examples from the provided transcript and `control_structures.ipynb`.

---

## Key Points  

- **Control Structures:**  
  Blocks that analyze variables and direct program flow based on conditions (e.g., `if-else`) or iteration (e.g., `for`, `while` loops).

- **Binary Operators:**  
  Operate on two operands (e.g., `a + b`, where `a` and `b` are operands).

- **Relational Operators:**  
  Compare two values, returning `True` or `False` (e.g., `==`, `!=`, `>`, `<`, `>=`, `<=`).

- **Decision Making:**  
  Use `if`, `elif`, `else` to execute code based on conditions.  
  ```python
  x = 10
  if x > 5:
      print("Greater than 5")
  elif x == 5:
      print("Equal to 5")
  else:
      print("Less than 5")

### Use Cases
- **Traditional programming:** Read/write text files, logs, or configurations.  
- **Data science:** Use pandas for structured data (e.g., CSVs) instead of manual file handling.

---

# 10. Object-Oriented Programming (OOPs) Concepts in Python

## Introduction
Object-Oriented Programming (OOPs) is a paradigm that models real-world entities using **classes** and **objects**. It focuses on bundling data and methods together, ensuring modularity, reusability, and abstraction.

## Main Concepts

### 1. Class
A **class** is a blueprint for creating objects. It defines attributes (data) and methods (functions) that describe behavior.

### 2. Object
An **object** is an instance of a class. Each object has its own data but shares the class’s structure and behavior.

### 3. Encapsulation
**Encapsulation** bundles data and methods into one unit and restricts direct access to some components, maintaining data integrity.

### 4. Inheritance
**Inheritance** allows one class (child) to acquire the properties and methods of another class (parent), promoting code reuse and hierarchy.

### 5. Polymorphism
**Polymorphism** allows different classes to define methods with the same name but different behavior, enabling flexibility and scalability.

### 6. Abstraction
**Abstraction** hides implementation details and shows only the necessary features, simplifying interaction with complex systems.

### 7. Class vs Instance Variables
- **Class Variables:** Shared among all objects of the class.
- **Instance Variables:** Unique to each object.

### 8. Methods
Methods define the behavior of a class and typically operate on instance variables using the `self` keyword.

## Summary
OOPs provides structure and clarity in programming through:
- Organized code via **classes and objects**
- Reusability using **inheritance**
- Flexibility with **polymorphism**
- Data protection via **encapsulation**
- Simplification through **abstraction**

# 11. NumPy Library in Python

## Introduction to NumPy
NumPy (Numerical Python) is a powerful library for numerical computations in Python. It provides support for multi-dimensional arrays and matrices, along with optimized mathematical functions to operate on them efficiently.

## Why Use NumPy?
- **Speed:** NumPy arrays are much faster than Python lists because they are implemented in C.
- **Memory Efficiency:** Arrays use less memory compared to lists.
- **Functionality:** Includes advanced mathematical, statistical, and array manipulation tools.
- **Scalability:** Suitable for large datasets in data science and analytics.

## Installation
Install NumPy using:
```bash
pip install numpy
```

## Importing NumPy
NumPy is generally imported as:
```python
import numpy as np
```

This convention simplifies function calls and ensures consistency in Python programs.

# 12. Pandas Library in Python

## Introduction
Pandas is a fast, flexible, and powerful Python library for data analysis and manipulation. It handles structured data efficiently using **DataFrames** and **Series**.

### Why Use Pandas?
- **Speed:** Optimized for large datasets.
- **Flexibility:** Supports multiple file formats (CSV, Excel, JSON, etc.).
- **Ease of Use:** Simplifies data handling.
- **Data Science:** Essential for cleaning, exploring, and analyzing data.

### Installation
```bash
pip install pandas
```

### Importing
```python
import pandas as pd
import numpy as np
```

---

## 1. Creating and Reading Data
```python
df = pd.read_csv("path/to/Churn_Modelling.csv")
df.head()
df.info()
df.describe()
```

## 2. Accessing and Modifying Data
```python
df['NewSalary'] = df['EstimatedSalary'] * 1.1
df['FullName'] = df['CustomerId'].astype(str) + ' ' + df['Surname']
df['Bal_SQRT'] = df['Balance'].apply(np.sqrt)
```

## 3. Filtering and Sorting
```python
filtered_df = df[df['Age'] >= 50]
df_sorted = df.sort_values(by=['Age', 'Tenure'], ascending=[False, True])
```

## 4. Handling Missing Values
```python
dfa = pd.read_csv("path/to/Test.csv")
dfa_clean = dfa.dropna()
dfa['Age'] = dfa['Age'].fillna(dfa['Age'].median())
```

## 5. Removing Columns
```python
df.pop('RowNumber')
df = df.drop(columns=['Surname', 'CreditScore'])
```

## 6. Grouping Data
```python
geo_mean = df.groupby('Geography').mean(numeric_only=True)
geo_gender_mean = df.groupby(['Geography', 'Gender'])['Balance'].mean()
```

## 7. Combining DataFrames
```python
result = pd.concat([df1, df2])
merged = pd.merge(df1, df2, on='cust_id', how='inner')
```

# 13. Matplotlib and Pandas Visualization Guide

## 1. Creating a DataFrame for Visualization

Matplotlib works well with Pandas DataFrames, which are often used to prepare data for visualization.

> **Example: Creating a DataFrame from a Dictionary**
```python
import pandas as pd
Data = {'Year': [1920, 1930, 1940, 1950, 1960, 1970, 1980, 1990, 2000, 2010, 2020],
        'Exchange Rate': [65, 69, 71, 64, 62, 59, 72, 71, 75, 78, 81]}
df = pd.DataFrame(Data)
```
---

## 2. Plotting with Matplotlib and Pandas

### Line Plot
```python
df.plot(x='Year', y='Exchange Rate', kind='line')
plt.show()
```

### Area Plot
```python
df.plot(x='Year', y='Exchange Rate', kind='area')
plt.show()
```

### Bar Plot
```python
df.plot(x='Year', y='Exchange Rate', kind='bar')
plt.show()
```

### Scatter Plot
```python
df.plot(x='Year', y='Exchange Rate', kind='scatter')
plt.show()
```

---

## 3. Pie Charts

### Simple Pie Chart
```python
Data = {'Tasks': [100, 500, 300]}
df2 = pd.DataFrame(Data, columns=['Tasks'], index=['Pending', 'Completed', 'Ongoing'])
df2.plot.pie(y='Tasks', figsize=(5, 5))
plt.show()
```

### Customized Pie Chart
```python
labels = ['Java', 'Python', 'R', 'Javascript']
sizes = [15, 30, 45, 10]
explode_labels = (0, 0.2, 0, 0)
fig1, ax1 = plt.subplots()
ax1.pie(sizes, explode=explode_labels, labels=labels, shadow=True, startangle=90)
ax1.axis('equal')
plt.show()
```

---

## 4. Working with a Real Dataset (Churn Modelling)

### Load and Clean Data
```python
churn_df = pd.read_csv('Churn_Modelling.csv')
churn_df.drop(['RowNumber', 'CustomerId', 'Surname'], axis=1, inplace=True)
```

### Value Counts and Plots
```python
churn_df['Geography'].value_counts().plot(kind='bar')
plt.show()
```

---

## 5. Advanced Visualizations

### Scatter Plot (Age vs Tenure)
```python
plt.scatter(churn_df['Age'], churn_df['Tenure'])
plt.show()
```

### Histogram (Tenure Distribution)
```python
plt.hist(churn_df['Tenure'], bins=30)
plt.show()
```

### Box Plot (Age Distribution)
```python
churn_df['Age'].plot.box()
plt.show()
```

---

## 6. Integration with Seaborn
```python
import seaborn as sns
sns.countplot(x='Geography', data=churn_df)
plt.show()
```

---

# 14 Seaborn in Python – Quick Notes

## Introduction
Seaborn is a Python visualization library built on top of **Matplotlib**.  
It simplifies creating **statistical and attractive plots** and integrates well with **Pandas DataFrames**.  
It also includes built-in datasets like *Iris* and *Flights* for practice.

---

## Why Use Seaborn
- Simplifies complex plots (heatmaps, pairplots)  
- Focused on **statistical visualizations**  
- Comes with **aesthetic default styles**  
- Works seamlessly with **Pandas**  
- Includes **sample datasets** for learning  

---

## Installation
```bash
pip install seaborn


Key Plot Types

Count Plot: Shows frequency of categories

KDE Plot: Displays data distribution

Histplot: Combines histogram + KDE

Pair Plot: Shows pairwise relationships

Line Plot: Visualizes trends

Box Plot: Shows spread and outliers

Heatmap: Visualizes correlations or matrices

Customization

Apply color palettes (Spectral, coolwarm)

Add titles, labels, and legends using Matplotlib

Use sns.set_theme() for unified styling

Advanced Visuals

Correlation Heatmap: Shows relationships between features

Pairplot with Hue: Highlights categories

Jointplot / Lmplot: Shows two-variable relationships

Plotly (Interactive)

Use Plotly for interactive dashboards and dynamic visualizations.

Summary

Seaborn = Easy + Beautiful + Statistical

Ideal for Exploratory Data Analysis (EDA)

Plotly → for interactivity

Matplotlib → for customization
