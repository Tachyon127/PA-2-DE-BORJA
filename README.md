# PA-2-DE-BORJA

This Python script contains two problems involving NumPy arrays, focusing on normalization and filtering based on divisibility.
---
## Problem #1: Normalization

1. A 5x5 array `x` is created with random floats between 0 and 1 using `np.random.rand()`.
2. The mean and standard deviation of all elements are computed with `.mean()` and `.std()`.
3. The array is normalized by subtracting the mean and dividing by the standard deviation.
4. The normalized array is saved to a `.npy` file using `np.save()`.

```
import numpy as np

# Create a 5x5 array of random floats between 0 and 1
x = np.random.rand(5,5)
print("Original Array X:\n", x)

# Compute mean and standard deviation
x_mean = x.mean()
print("\nMean:", x_mean)

x_std = x.std()
print("Standard Deviation:", x_std)

# Normalize the array
x_normalized = (x - x_mean) / x_std
print("\nNormalized Array X:\n", x_normalized)

# Save the normalized array
np.save("x_normalized.npy", x_normalized)
print("\nSAVED NORMALIZED NDARRAY as x_normalized.npy")
```

## Problem #2: Divisible by 3

1. An array of integers from 1 to 100 is created using np.arange().
2. Each number is squared to create a new array.
3. The array is reshaped into a 10x10 matrix using .reshape().
4. Elements divisible by 3 are filtered using the modulo operator %.
5. The filtered elements are saved to a .npy file using np.save().

```
import numpy as np

# Create an array of integers from 1 to 100
numbers = np.arange(1, 101)

# Square each number
square = numbers ** 2

# Reshape into 10x10 matrix
a = square.reshape(10, 10)
print("\nMatrix A (10x10)\n")
print(a)

# Filter elements divisible by 3
div_by_3 = a[a % 3 == 0]
print("\n\nALL ELEMENTS DIVISIBLE BY 3\n")
print(div_by_3)

# Save the result
np.save("div_by_3.npy", div_by_3)
print('\nResult Saved as div_by_3.npy')
```
