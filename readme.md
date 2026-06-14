# Programming Assignment 2: Lexical Scoping

## R Programming Course - Coursera (Johns Hopkins University)

## Overview
This assignment demonstrates the use of lexical scoping in R to cache 
computationally expensive results. The script caches the inverse of a 
matrix so it doesn't have to be recomputed every time.

## Functions

### `makeCacheMatrix(x)`
Creates a special matrix object that can cache its inverse. Returns a 
list of four functions:
- `set()` — sets the matrix
- `get()` — gets the matrix
- `setinverse()` — caches the inverse
- `getinverse()` — retrieves the cached inverse

### `cacheSolve(x)`
Computes the inverse of the matrix returned by `makeCacheMatrix`. 
If the inverse has already been calculated, it retrieves it from 
cache instead of recomputing.

## Usage
```r
m <- makeCacheMatrix(matrix(c(1,2,3,4), 2, 2))
cacheSolve(m)  # computes inverse
cacheSolve(m)  # returns cached inverse
```

## Author
Sidra Jabeen Khan
