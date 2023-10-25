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
   - Slicing: `string[start:stop:step]`
   - Indexing: `string[index]` (0-based index)
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
- `range(start, stop, step)`: Generates a sequence of numbers within a given range

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

**Sequence data types - Indexing, Slicing, Operations**
- `indexing`: Retrieve a single element `[index]`. Negative indexes count from the end.
- `slicing`: Retrieve a sequence of elements `[start:stop:step]`.
- `operations`:  
   `len(sequence)`: Length  
   `sequence + sequence`: Concatenation  
   `sequence * int`: Repetition  
   `item in sequence`: Membership (returns True/False)  
   `sequence1 == sequence2`: Equality  
   
**List comprehension**
- `[expression for item in list if condition]`

**Mutable vs Immutable**
- Mutable: Objects that can change their state or contents after they're created (`list`, `dict`, `set`)
- Immutable: Objects that can't be changed after they're created (`string`, `tuple`)

**Python Basic Functions and Methods**
- `str.split(separator)`: splits a string into a list where each word is a list item.
- `str.count(substring)`: returns the number of occurrences of a substring in the given string.
- `list.append(item)`: adds an item to the end of the list.

**Python Built-in Functions**
- `print(object)`: prints the object to the console.
- `len(s)`: returns the length of an object. Can work with strings, list, tuples, dictionary etc.
- `sum(iterable[, start])`: sums start and the items of an iterable from left to right and returns the total.
- `abs(x)`: returns the absolute value of a number.
- `zip(*iterables)`: makes an iterator that aggregates elements from each of the iterables.

**User-defined Functions & Anonymous Functions**
- Regular function:
    ```python
    def function_name(parameters):
      # code here
      return output
    ```
- Lambda (Anonymous) function: `function_name = lambda parameters: expression`. These are small, throw-away functions.

**Functions as Objects**
Python functions are first class objects. You can assign them to variables, store them in data structures, pass them as arguments to other functions, and even return them as values from other functions.

**File Handling**
- `f = open('path', 'mode')`: opens a file at the given path with the given mode ('r', 'w', 'a', etc.)
  - 'r': read mode (default)
  - 'w': write mode (overwrites the file)
  - 'a': append mode (appends at end of file)
  - 'b': binary mode (for non-text files)
- `f.read(size)`: reads some quantity of data and returns it as a string (in text mode) or bytes object (in binary mode).
- `f.write(string)`: writes the string to the file, returning the number of characters written.
- `f.close()`: closes the file. Always call `f.close()` at the end of your script.

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
np.ones((3, 3))  # Array of ones
np.empty((3, 3))  # Empty array
np.arange(0, 10, 1)  # Similar to range
np.linspace(0, 10, 5)  # 5 equally spaced values from 0 to 10
```

**3. Attributes**
```python
arr = np.array([1, 2, 3, 4, 5])
arr.shape  # Returns the shape of the array in terms of dimensions
arr.ndim  # Number of dimensions
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
arr = np.array([1, 2, 3, 4, 5, 6])
arr = arr.reshape((3, 2))  # Reshaping into 3 rows and 2 columns
arr = arr.T  # Transposing
```

**8. Linear Algebra**
```python
arr = np.array([[1, 2], [3, 4]])
eigenvalues, eigenvectors = np.linalg.eig(arr)  # Eigenvalues and eigenvectors
inverse = np.linalg.inv(arr)  # Inverse of an array
det = np.linalg.det(arr)  # Determinant of an array
dot_prod = np.dot(arr1, arr2)  # Dot product of two arrays
```

**9. Sorting**
```python
arr = np.array([2, 1, 5, 3, 7, 4, 6, 8])
sorted_arr = np.sort(arr)
```

**10. Stacking arrays**
```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
np.vstack((arr1, arr2))  # vertically stacks arr1 and arr2
np.hstack((arr1, arr2))  # horizontally stacks arr1 and arr2
```

**Pandas**

**Data structures:**
- Series: One-dimensional labeled array, can hold any data type like integers, strings, floating points, Python objects, and so on. 
    - Creation: `s = pd.Series(data, index)`
    - Accessing: Similar to accessing elements in an ndarray.
- DataFrame: Two-dimensional labeled data structure with columns of potentially different types.
    - Creation: `df = pd.DataFrame(data, index, columns)`
    - Accessing: `df['column_name']`, `df.loc[label]`, `df.iloc[index]`.

**Data Manipulation Tools:**
- **Creating DataFrame from multiple data types:**
  - dict: `df = pd.DataFrame(dict)`
  - list: `df = pd.DataFrame(list)`
  - np.array: `df = pd.DataFrame(np.array)`
- **Read/write file:**
  - .csv: `pd.read_csv("filename.csv")`, `df.to_csv("filename.csv")`
  - .json: `pd.read_json("filename.json")`, `df.to_json("filename.json")`
  - Excel: `pd.read_excel("filename.xlsx")`, `df.to_excel("filename.xlsx")`
- **Indexing:** Accessing data from series/DataFrame:
  - `.loc[]` - Access a group of rows and columns by label(s)
  - `.iloc[]` - Purely integer-location based indexing for selection by position
  - Boolean Indexing: `df[df['column_name'] > condition]`
- **Splicing:** `df[start_row:end_row]`
- **Merging:** Combine data on common columns: `df1.merge(df2, on='common_column')`
- **Concatenating:** Adds dataframes along a particular axis: `pd.concat([df1,df2])`
- **Reindexing:** Conform DataFrame to new index: `df.reindex(new_index)`
- **Selection:** Like indexing, but two-step process: `df.loc[[row1,row2], [col1,col2]]`
- **Filtering:** Subset the data based on a condition: `df[df['column'] > condition]`
- **Updating:** Change data based on some condition: `df.loc[row_indexer,col_indexer] = value`
- **Sorting:** 
  - By values: `df.sort_values(by='column_name')`
  - By index: `df.sort_index()`
  - Ranking: `df['column'].rank()`
- **Apply functions:** Also possible to apply user-defined and lambda functions to columns or entire dataframe
- **Statistic functions:** `count()`, `sum()`, `mean()`, `median()`, `mode()`, `min()`, `max()`, `abs()`, `prod()`, `std()`, `var()`, `sem()`, `skew()`, `kurt()`, `quantile()`, `cumsum()`, `cumprod()`, `cummax()`, `cummin()`.
