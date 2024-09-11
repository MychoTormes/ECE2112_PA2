# ECE2112_PA2: NUMERICAL PYTHON (NUMPY)

# PROBLEM 1: 
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as:

     𝑍 = 𝑋 − 𝑥̅ / 𝜎

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy


## Background
Here are the steps on how is it done:

#### Import Numerical Python in the notebook:
    import numpy as np

#### Define normalize and use the formula:

     def normalize(x):

     a = x.std()
     b = x.mean()
     z = x - b / a
     
     return z

#### Use random and then normalize array:

     x = x.random.random((5,5))

     s = normalize(x)


#### Save the array as a file:

     np.save('X_normalize.npy', s)

## Files
To know whether it works or not, my codes are here:
     Normalization.ipynb

Here is the saved array file:
     X_Normalize


# PROBLEM 2:
     Create the following 10 x 10 ndarray.


     A =  [1    4    ⋯   81    100
           ⋮     ⋮    ⋱    ⋮      ⋮
           ⋮     ⋮    ⋱    ⋮      ⋮
           ⋮     ⋮    ⋱    ⋮      ⋮
          8281 8464  ⋯  9801  10000]


which are the squares of the first 100 positive integers.

From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy



## Background
Here are the following steps on how is it done:

#### Import Numerical python in the notebook

     import numpy as np

#### Create a 10 x 10 array:
     x = np.linspace(1,100,100)

     x.resize(10,10)

#### Multiply the array by 3:
     z = x*3

#### Save the array as a file:
     np.save('div_by_3', z)
