# PA-2-DE-BORJA

Problem #1
- **Normalization**

1. A 5x5 array (x) is created with random floating-point numbers by using np.random.rand()
2. Element-wise, the mean and standard deviation of the integers inside the array are calculated using .mean() and .std()
3. The array is NORMALIZED by subtracting the mean and dividing by the standard deviation
4. The normalized array is then saved to a .npy file using np.save()

```
import numpy as np

## Create an array that will generate random numbers between 0 and 1
x = np.random.rand(5,5)
print ("Original Array X:\n", x)

## .mean() is utilized to compute the average of the elements
x_mean = x.mean()
print ("\nMean:", x_mean)

## .std() is utilized to compute the dispersion of the data set
x_std = x.std()
print ("Standard Deviation:", x_std)
## Creating a normalized ndarray
x_normalized = (x - x_mean) / x_std
print ("\nNormalized Array X:\n", x_normalized)

## Saving the result as an .npy file
np.save("x_normalized.npy", x_normalized)
print ("\nSAVED NORMALIZED NDARRAY as X_normalized.npy")
```

Problem #2
- **Divisible by 3**

1. An array of positive integers from 1 to 100 is created using np.arange()
2. Each number is then squared to create a new array
3. The new array is reshaped to a 10x10 matrix using np.reshape()
4. The modulo operator % is used to determine all elements divisible by 3
5. The filtered results are saved to a file named div_by_3.npy using np.save().

```
import numpy as np

## We start out by creating an array 
numbers = np.arange(1,101)

## The first 100 positive integers are squared 
square = numbers ** 2

## The array io then reshaped into a 10x10 matrix
a = square.reshape(10, 10)
print ("\nMatrix A (10x10)\n")
print (a)

## Modulo is utilized to reveal the integers divisible by 3 in the matrix
div_by_3 = a[a % 3 == 0]
print ("\n\nALL ELEMENTS DIVISIBLE BY 3\n")
print (div_by_3)

## Saving the result as an .npy file
np.save("div_by_3.npy", div_by_3)
print ('\nResult Saved as div_by_3.npy')
```
