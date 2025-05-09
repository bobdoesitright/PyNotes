
# **NumPy: The Core Library for Scientific Computing in Python**

> NumPy is the foundational library for numerical computing in Python, providing support for arrays, matrices, and high-level mathematical functions.

---

## **Installation**

```bash
pip install numpy
```

---

## **Importing NumPy**

```python
import numpy as np
```

---

## **Core Data Structures**

### **1. ndarray (N-dimensional array)**

- A **multi-dimensional** array that holds elements of the same type. It is the core data structure in NumPy.
```python
arr = np.array([1, 2, 3, 4])
```

### **2. Creating Arrays**
```python
np.array([1, 2, 3])              # 1D array
np.array([[1, 2], [3, 4]])       # 2D array
np.zeros((2, 3))                 # Array of zeros
np.ones((3, 3))                  # Array of ones
np.eye(3)                        # Identity matrix
np.arange(0, 10, 2)              # Array with a step size
np.linspace(0, 1, 5)             # Evenly spaced values
```

---

## **Array Operations**

### **Element-wise Operations**
```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

arr_sum = arr1 + arr2            # Element-wise addition
arr_prod = arr1 * arr2           # Element-wise multiplication
```

### **Mathematical Functions**
```python
np.add(arr1, arr2)               # Element-wise addition
np.multiply(arr1, arr2)          # Element-wise multiplication
np.sin(arr1)                     # Sine of each element
np.sqrt(arr1)                    # Square root of each element
np.log(arr1)                     # Natural log of each element
```

---

## **Array Indexing and Slicing**

### **1D Array**
```python
arr = np.array([10, 20, 30, 40, 50])

arr[0]             # First element
arr[-1]            # Last element
arr[1:4]           # Slice elements from index 1 to 3
```

### **2D Array**
```python
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

arr[0, 1]          # Element at row 0, column 1
arr[1, :]          # All elements from row 1
arr[:, 2]          # All elements from column 2
```

---

## **Array Reshaping**

```python
arr = np.array([1, 2, 3, 4, 5, 6])
arr_reshaped = arr.reshape(2, 3)     # Reshape to 2x3 array
```

### **Flattening an Array**
```python
arr_flattened = arr_reshaped.flatten()
```

---

## **Array Concatenation and Splitting**

### **Concatenating Arrays**
```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])

concatenated = np.concatenate((arr1, arr2))         # Concatenate along 1D
concatenated_2d = np.concatenate((arr1.reshape(2, 1), arr2.reshape(2, 1)), axis=1)   # Concatenate along 2D
```

### **Splitting Arrays**
```python
arr = np.array([1, 2, 3, 4, 5, 6])
split_arr = np.split(arr, 3)             # Split into 3 equal parts
```

---

## **Statistical and Mathematical Operations**

```python
np.sum(arr)                      # Sum of elements
np.mean(arr)                     # Mean of elements
np.median(arr)                   # Median of elements
np.std(arr)                      # Standard deviation
np.var(arr)                      # Variance
np.min(arr)                      # Minimum value
np.max(arr)                      # Maximum value
np.argmin(arr)                   # Index of minimum value
np.argmax(arr)                   # Index of maximum value
```

---

## **Linear Algebra Operations**

### **Matrix Multiplication**
```python
arr1 = np.array([[1, 2], [3, 4]])
arr2 = np.array([[5, 6], [7, 8]])

result = np.dot(arr1, arr2)          # Matrix multiplication
```

### **Matrix Inversion**
```python
arr_inv = np.linalg.inv(arr1)         # Matrix inversion
```

### **Determinant**
```python
det = np.linalg.det(arr1)             # Matrix determinant
```

---

## **Random Numbers and Seeding**

```python
np.random.seed(42)                      # Set the seed for reproducibility
random_arr = np.random.rand(3, 3)      # Random array with values between 0 and 1
random_int = np.random.randint(1, 10, size=(3, 3))  # Random integers between 1 and 10
```

---

## **Useful NumPy Functions**

```python
np.unique(arr)             # Unique elements of array
np.sort(arr)               # Sorted array
np.argsort(arr)            # Indices of sorted array
np.diff(arr)               # Difference between consecutive elements
np.cumsum(arr)             # Cumulative sum
np.cumprod(arr)            # Cumulative product
```

---

## **Mini Project Example**

```python
import numpy as np

# Creating arrays
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

# Perform element-wise operations
result = arr1 * arr2

# Matrix operations
matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])
matrix_result = np.dot(matrix1, matrix2)

print(result)
print(matrix_result)
```

---

## **Why Use NumPy?**

- Efficient handling of multi-dimensional arrays.
- Faster execution due to vectorization.
- Wide variety of functions for mathematical, statistical, and linear algebraic operations.
- Integral for scientific computing and machine learning.

---

## **Learn More**

- [Official Docs](https://numpy.org/doc/stable/)
- [NumPy Cheat Sheet](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.html)

---

> **"Without NumPy, Python would just be another slow language."**

