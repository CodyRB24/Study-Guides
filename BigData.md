**Python Basics:**

**Indentation**: Used for blocks of codes following statement(s) that end(s) in a colon such as in loops or class/def/if/elif/else statements. Commonly, 4 spaces are used for indentation.

**Objects**: In Python, objects refer to items that have types, like strings, integers, etc. These objects possess data, and have specific behavior according to their type definition.

**Comments**: Two types: single line comments marked with '#' and multi-line comments enclosed in """ """ or ''' '''. Not executed by Python, used for describing code.

**Variables**: Named locations used to store data in memory. A variable is created the moment you first assign a value to it. Variables can be re-assigned to any value of any data type.

**Scalars**: Single value data types. Python's scalar types: int, float, none, bool, str, bytes.
  - `int`: Integer, e.g., 5, 3, 78.
  - `float`: Floating-point number, e.g., 3.14, 5.77.
  - `none`: None type represents the absence of value or a null value.
  - `bool`: Boolean type, can have two values, True or False.
  - `str`: String type, it's a sequence of unicode characters. e.g., "Hello".
  - `bytes`: Bytes literal, it represents a group of byte numbers with a string of elements separated by commas of the format 0 <= x < 256.

**Type conversion**: The process of converting the value of one data type to another. Python has built-in methods for conversion:
  - `int()`
  - `float()`
  - `str()`
  - `bool()`

**Python Operators**: These include:
  - Arithmetic: `+`, `-`, `*`, `/`, `//` (floor division), `**` (exponentiation or power), `%` (modulo)
  - Comparison: `==`, `!=`, `>`, `<`, `>=`, `<=`
  - Logical: `and`, `or`, `not`
  - Identity: `is`, `is not`
  - Membership: `in`, `not in`

**String Operations**: Various methods to manipulate strings:
   - Concatenation: `"string1" + "string2"`

**Control Flow**
- `if`, `elif`, `else`: Conditional control structures, execute code blocks based on condition validity.
   ```python
   if condition1:
       # code block 1
   elif condition2:
       # code block 2
   else:
       # code block 3
   ```
- `for` loops: Iterate over a sequence (list, tuple, string) or other iterable objects
   ```python
   for val in sequence:
       # code block
   ```
- `while` loops: Execute a set of statements as long as a condition is true
   ```python
   while condition:
       # code block
   ```
- `break`: Ends the current loop and jumps to the statement following the loop.
- `continue`: Causes the loop to skip the remainder of its body and immediately retest its condition.
- `pass`: Used when statement is required syntactically but no code/executable statement is necessary.
- `range(1, 10, 2)`: Generates: # Output: 1 3 5 7 9
- `range(2, 6)`: Generates: # Output: 2 3 4 5
- `range(5)`: Generates: # Output: 0 1 2 3 4 5

**Built-in data structures**
- `list`: Ordered, mutable collection, allows duplicate members.
   ```python
   list = [item1, item2, ...]  
   ```
- `tuple`: Ordered, immutable collection, allows duplicates.
   ```python
   tuple = (item1, item2, ...)
   ```
- `dict`: Unordered, mutable collection of key-value pairs, no duplicate keys.
   ```python
   dict = {'key1': value1, 'key2': value2, ...}
   ```
- `set`: Unordered, Mutable, No duplicate members.
   ```python
   set = {item1, item2, ...}
   ```

**Python Basic Functions and Methods**
- `str.split(separator)`: splits a string into a list where each word is a list item.
- `str.count(substring)`: returns the number of occurrences of a substring in the given string.
- `list.append(item)`: adds an item to the end of the list.
- `len(sequence)`: Length  
- `sum(sequence)`: Sum

**User-defined Functions & Anonymous Functions**
- Regular function:
    ```python
    def function_name(parameters):
      # code here
      return output
    ```
- Lambda (Anonymous) function: `function_name = lambda parameters: expression`. These are small, throw-away functions.

**NumPy**
**1. Importing NumPy**
```python
import numpy as np
```

**2. Creating NumPy Arrays**
```python
# From lists
np.array([1, 2, 3, 4, 5])

# Using built-in functions
np.zeros((3, 3))  # Array of zeros
np.empty((3, 3))  # Empty array
arr.dtype  # Data type of the elements
```

**4. Arithmetic Operations (Element-wise)**
```python
arr1, arr2 = np.array([1, 2, 3]), np.array([4, 5, 6])
arr1 + arr2
arr1 - arr2
arr1 / arr2
arr1 * arr2
arr1 ** arr2
arr1 < arr2
arr1 > arr2
```

**5. Universal Functions (ufuncs)**
```python
arr = np.array([1, 2, 3, 4, 5])
np.sum(arr)
np.min(arr)
np.max(arr)
np.argmax(arr)  # Returns the indices of the maximum values
np.argmin(arr)  # Returns the indices of the minimum values
```

**6. Indexing and Slicing**
```python
arr = np.array([1, 2, 3, 4, 5])
arr[0]  # 1st Element
arr[1:4]  # Subarray, 2nd to 4th element
```

**7. Reshaping and Transposing (Changing Dimensions)**
```python
arr = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11])
arr = np.arange(0, 12, 1) or np.arange(12)  # Creates np array with values 0-11
arr = np.reshape(arr,(3, 4)) 
# [[ 0 1 2  3 ]
#  [ 4 5 6  7 ]
#  [ 8 9 10 11]]
arr = arr.T or arr.swapaxes(0,1)
# [[ 0  4  8]
#  [ 1  5  9]
#  [ 2  6 10]
#  [ 3  7 11]]
```

**9. Sorting**
```python
arr = np.array([2, 1, 5, 3, 7, 4, 6, 8])
sorted_arr = np.sort(arr)
```

**Pandas**

- **Statistic functions:** `count()`, `sum()`, `mean()`, `median()`, `mode()`, `min()`, `max()`, `abs()`, `prod()`, `std()`, `var()`, `sem()`, `skew()`, `kurt()`, `quantile()`, `cumsum()`, `cumprod()`, `cummax()`, `cummin()`

**Data structures:**
- Series: One-dimensional labeled array, can hold any data type like integers, strings, floating points, Python objects, and so on. 
    - Creation: `s = pd.Series(data, index)`
    - Accessing: Similar to accessing elements in an ndarray.
- DataFrame: Two-dimensional labeled data structure with columns of potentially different types.
    - Creation (dict): `data = { 'Var':['A','B','C'], 'Num': [25, 30, 35]} df = pd.DataFrame(data)`
    - Accessing: `df['column_name'] = value`, `df.loc[label]`, `df.iloc[index]`.

- **Creating DataFrame from multiple data types:**
  - dict: `df = pd.DataFrame(dict)`
  - list: `df = pd.DataFrame(list)`
  - np.array: `df = pd.DataFrame(np.array)`

  - **Read/write file:**
  - .csv: `pd.read_csv("filename.csv")`, `df.to_csv("filename.csv")`

  - **Indexing:** Accessing data from series/DataFrame:
  - `.loc[]` - Access a group of rows and columns by label(s)
  - `.iloc[]` - Purely integer-location based indexing for selection by position

- **Concatenating:**
df1 = pd.DataFrame({
    'A': ['A0', 'A1'],
    'B': ['B0', 'B1']
})
df2 = pd.DataFrame({
    'A': ['A2', 'A3'],
    'B': ['B2', 'B3']
})

result = pd.concat([df1, df2])
    A   B
0  A0  B0
1  A1  B1
0  A2  B2
1  A3  B3

**Chunks**
import pandas as pd

chunker = pd.read_csv("examples/ex6.csv", chunksize=1000)

tot = pd.Series([], dtype='int64')
for piece in chunker:
    tot = tot.add(piece["key"].value_counts(), fill_value=0)

tot = tot.sort_values(ascending=False)

# Displaying the top 10 keys
print(tot[:10])

# Output
key
E    368.0
X    364.0
L    346.0
O    343.0
Q    340.0
M    338.0
J    337.0
F    335.0
K    334.0
H    330.0
dtype: float64
