# ECE2112-PA2-Parayno
This contains my PA2 for Numerical Python (NUMPY). Experiment 2 covers the codes and functions incorporated in the Numpy library. Also, be able to apply and use the different codes and functions in creating a Python program using a Numpy library.

## Problem 1
<img width="550" alt="Screenshot 2024-09-01 at 7 06 51 PM" src="https://github.com/user-attachments/assets/957805e3-e77f-409b-839a-fbcf86d77b72">

### My Code:
```
import numpy as np

print("The random matrix of X:")
X = np.random.random((5,5)) #creates a 5 x 5 random matrix
print(X)

mean = np.mean(X) #mean of X
print("\nMean:", mean)
sd = np.std(X) #standard deviation of X
print("Standard Deviation:", sd)

print("\nThe normalized matrix:")
X_normalized = (X-mean/sd) #normalized matrix of X

np.save("X_normalized.npy", X_normalized)
np.load("X_normalized.npy")
```
### Result of Problem 1:
Please note that the provided data will be randomized every time it is executed.

```
The random matrix of X:
[[0.0447463  0.94699493 0.11917493 0.84459635 0.37373493]
 [0.62483735 0.64119075 0.58741274 0.16286531 0.91020188]
 [0.05806025 0.82536382 0.80343129 0.30683425 0.89575531]
 [0.01596399 0.31071749 0.45843822 0.83198516 0.26505529]
 [0.78393064 0.83561248 0.21007601 0.72101679 0.57947107]]

Mean: 0.5262987018225408
Standard Deviation: 0.3066908835856325

The normalized matrix:
array([[-1.67130961, -0.76906097, -1.59688098, -0.87145956, -1.34232097],
       [-1.09121855, -1.07486515, -1.12864316, -1.55319059, -0.80585403],
       [-1.65799566, -0.89069208, -0.91262462, -1.40922166, -0.8203006 ],
       [-1.70009192, -1.40533842, -1.25761768, -0.88407074, -1.45100061],
       [-0.93212526, -0.88044343, -1.50597989, -0.99503911, -1.13658483]])
```

>The code that I made generated a random 5 x 5 matrix ' X ', which then calculates the mean and its standard deviation, and then attempts to normalize the matrix by subtracting the mean and dividing it by its standard deviation. The normalized matrix is saved to a file named "X_normalized.npy". 

## Problem 2

<img width="550" alt="Screenshot 2024-09-01 at 7 14 06 PM" src="https://github.com/user-attachments/assets/fe13d3ac-78c3-4ebf-a91e-fcd6955ae2c2">

### My Code:

```
import numpy as np

array = np.arange(1,101).reshape(10,10) #matrix from 1-100
print("The perfect squares of the first 100 positive integers:")
x = pow(array,2) #square of the matrix
print(array)

div_3 = x[x%3==0] #list of numbers divisible by 3
print("\nThe numbers divisible by 3:")

np.save("div_by_3.npy", div_3)
np.load("div_by_3.npy")
```
### Result of my Problem 2:

```
The perfect squares of the first 100 positive integers:
[[  1   2   3   4   5   6   7   8   9  10]
 [ 11  12  13  14  15  16  17  18  19  20]
 [ 21  22  23  24  25  26  27  28  29  30]
 [ 31  32  33  34  35  36  37  38  39  40]
 [ 41  42  43  44  45  46  47  48  49  50]
 [ 51  52  53  54  55  56  57  58  59  60]
 [ 61  62  63  64  65  66  67  68  69  70]
 [ 71  72  73  74  75  76  77  78  79  80]
 [ 81  82  83  84  85  86  87  88  89  90]
 [ 91  92  93  94  95  96  97  98  99 100]]

The numbers divisible by 3:
array([   9,   36,   81,  144,  225,  324,  441,  576,  729,  900, 1089,
       1296, 1521, 1764, 2025, 2304, 2601, 2916, 3249, 3600, 3969, 4356,
       4761, 5184, 5625, 6084, 6561, 7056, 7569, 8100, 8649, 9216, 9801])
```
>The code that I made creates a 10 x 10 matrix of numbers from 1 to 100, then computes their squares, and filters the square numbers that are divisible by 3. It then saves it to a file named "div_by_3.npy".
