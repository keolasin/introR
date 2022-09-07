---
Week: 1
Lecture: Lecture 2.1
Topic: Toolkit 1
Instructor: Lauren Nelson MPH; Will Wheeler, PhD, MPH
Course: Intro to R, PHW 251
Tags: R, RStudio, Programming Language, Statistics, Introduction
---

# Toolkit 1

## Vectors

```R

vec_num <- c(1,5,6,10)
vec_num2 <- 1:10 # creates a vector containing numbers 1-10
vec_char <- c("dog", "cat")

vec_multi <- c(290, "ph") # forces to a single data type, so values in this vector will all be character types

```

## Matrices

- multiple dimensions, single data type
- created using `matrix()` fxn

```R

my_matrix1 <- matrix( # matrix fxn
    data = 1:10, # numbers from 1-12
    nrow = 3, # 3 rows
    ncol = 4, # 4 cols
    byrow = FALSE, # numbers would go down the column first; if TRUE, goes across the row first
    dimnames = null
)

```

## Lists

- one-dimensional, multiple data types and/or objects
- created using `list()` function

```R

my_list <- list(290, "290") # stores a list with a numeric value of 290, and a character value of "290"

```

## Functions that help describe objects

```R

length() # how long is the object?

class() # what type of object is it?

typeof() # what data type is the object?

```

