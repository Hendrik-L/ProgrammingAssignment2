## Data Science Specialization, R Programming Course

### Programming Assignment 2:
Creating a mechanism that caches results and thus saves time
if time-consuming matrix inversions are repeatedly required.

### makeCacheMatrix:
A function that creates a special object which stores a matrix 
and caches its inversed version. 

### cacheSolve:
A function that calculates and returns the inverse matrix 
for the matrix stored by the special object 
created with the above function.

### Use case example for the R console:
myMatrix <- NULL

myMatrix <- makeCacheMatrix()

myMatrix$set(matrix(c(3, 1, 2, 4, 5, 6, 9, 7, 8), nrow=3, ncol=3, byrow=TRUE))

myMatrix$get()

  [,1] [,2] [,3]
  
  [1,]    3    1    2
  
  [2,]    4    5    6
  
  [3,]    9    7    8
  
cacheSolve(myMatrix)

  [,1]       [,2]       [,3]
  
  [1,]  0.1111111 -0.3333333  0.2222222
  
  [2,] -1.2222222 -0.3333333  0.5555556
  
  [3,]  0.9444444  0.6666667 -0.6111111
  
cacheSolve(myMatrix)

getting cached data

  [,1]       [,2]       [,3]
  
  [1,]  0.1111111 -0.3333333  0.2222222
  
  [2,] -1.2222222 -0.3333333  0.5555556
  
  [3,]  0.9444444  0.6666667 -0.6111111
  
