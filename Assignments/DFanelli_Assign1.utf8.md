---
title: "DFanelli_Assign1.Rmd"
author: "Dan Fanelli"
date: "February 1, 2016"
output: pdf_document
---

# Assignment 1:

## Problem Set 1:

(1) Calculate the dot product u.v where u = [0.5; 0.5] and v = [3; â4]


```r
c(0.5, 0.5) %*% c(3,-4)
```

```
##      [,1]
## [1,] -0.5
```

(2) What are the lengths of u and v? Please note that the mathematical notion of the length of a vector is not the same as a computer science definition.


```r
norm(c(0.5, 0.5), type="2")
```

```
## [1] 0.7071068
```

(3) What is the linear combination: 3u â 2v?

Answer: Its the dot product of EITHER c(3,-2) and c(u,v) OR c(3,2) and c(u,-v)

(4) What is the angle between u and v


```r
u <- c(0.5, 0.5)
v <- c(3,-4)
acos(sum(u * v) / ( sqrt(sum(u * u)) * sqrt(sum(v * v)) ) )
```

```
## [1] 1.712693
```

## Problem Set 2:


```r
mat <- t(matrix(c(1,1,3,2,-1,5,-1,-2,4),nrow=3,ncol=3))
soln <- c(1,2,6)
m <- cbind(mat, soln)
m
```

```
##              soln
## [1,]  1  1 3    1
## [2,]  2 -1 5    2
## [3,] -1 -2 4    6
```


```r
for(c in 1:ncol(m))
  for(r in 1:nrow(m))
    print(m[r,c])
```

```
##   
## 1 
##   
## 2 
##    
## -1 
##   
## 1 
##    
## -1 
##    
## -2 
##   
## 3 
##   
## 5 
##   
## 4 
## soln 
##    1 
## soln 
##    2 
## soln 
##    6
```


