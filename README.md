# Strassen's Matrix Multiplication

This Python script implements Strassen's algorithm for matrix multiplication. Strassen's algorithm is an optimized approach to matrix multiplication that reduces the number of recursive multiplications compared to the traditional matrix multiplication method.

## Overview

Strassen's algorithm divides matrices into smaller submatrices and uses seven recursive multiplications instead of the usual eight required in traditional matrix multiplication. This results in a more efficient matrix multiplication with a time complexity of approximately \(O(n^{\log_7}) \approx O(n^{2.81})\), which is faster than the \(O(n^3)\) time complexity of standard matrix multiplication for large matrices.

## Code Explanation

The function `strassen(A, B)` takes two square matrices \(A\) and \(B\) as input, where the size of both matrices is a power of 2. It recursively divides the matrices into submatrices and calculates intermediate results to obtain the product matrix \(C\).

### Key Steps:
1. **Base Case:** When the size of the matrices is 1, the multiplication is straightforward.
2. **Matrix Division:** The matrices \(A\) and \(B\) are divided into four submatrices each.
3. **Recursive Computation:** Seven intermediate matrices \(M1\) to \(M7\) are computed using the Strassen's formula.
4. **Combination of Submatrices:** The submatrices are combined to form the final result matrix \(C\).

### Example Usage

```python
import numpy as np

# Define two 3x3 matrices
A = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])

B = np.array([[9, 8, 7],
              [6, 5, 4],
              [3, 2, 1]])

# Perform matrix multiplication using Strassen's algorithm
C = strassen(A, B)

# Print the matrices
print("Matrix A:")
print(A)
print("\nMatrix B:")
print(B)
print("\nResulting Matrix C (A * B):")
print(C)
```
### Dependencies
The script requires you to install numpy. To install it, run:

```pip install numpy```

### Conclusion
This implementation demonstrates Strassen's matrix multiplication algorithm in Python, utilizing recursion and matrix partitioning. It offers a more efficient approach for multiplying large matrices, providing faster performance compared to traditional matrix multiplication methods.
 
