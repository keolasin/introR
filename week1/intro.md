---
Week: 1
Lecture: Lecture 1.3
Topic: Overview of R
Instructor: Lauren Nelson MPH; Will Wheeler, PhD, MPH
Course: Intro to R, PHW 251
Tags: R, RStudio, Programming Language, Statistics
---

# Introduction to R

## Learning Objectives

Get an overview of R and tools for stats associated with R, RStudio

## Objects

### Atomic vector

- one dimensional
- contains a single data type

### Matrix

- multiple dimensions
- contains a single data type

### List

- ordered collection of objects
- can even have a list of lists
- various different data types possible

### Data Frame

- default structure for tabular data
- columns of different types

### Factors

- categorical variables
- stored as integer, displays as character with fixed order
- one use is for modeling

## Data Types

1. character: `"ph"`
2. numeric: `290`
3. integer: `290L` (l tells R to store as an integer)
4. logical: `TRUE`, `FALSE`
5. complex: `1+4i`

- Dates stored as numbers
- there are several constants available in base R (today's date)
- missing values are stored as NA

## Assign variables

`x <- 290`, the `<-` operator assigns values to variables

`(x <- 290)`, assigns and prints object contents to the console

*Best Practices*

- naming objects/variables, use lowercase text, separate with underscores (snake casing)

## Relational operators

`==` equal to
`!=` not equal to
`<` less than
`>` greater than
`<=` less than or equal to
`>=` greater than or equal to

## Functions

- Used to create new objects, do calculations, or anything repetitive
- Base R has many built in Functions
- more available to download as part of packages
- possible to write new functions

example:

```R
function_name <- function(arg1, arg2, ...) {
    # function body
}

# using the new function:
test_object <- function_name(arg1 = value1, arg2 = value2, ...) # best practice is to name the value to the argument

# sequence fxn `seq()`

seq(from=1, to=20, by=1) # start at 1, go to 20, spaced by 1
seq(from=1, to=50, by=2) # same but spaced by 2
seq(from=1, to=50, length.out=10) # equally spaces within the range ensuring 10 values


```

## Packages

- expand capabilities of Base R
- many available through GitHub/CRAN
- come with docs
- install into R environment
- load in current sessions

```r

.libPaths() # tells you the paths to the library
library() # tells you the packages already in your environment
info <- installed.packages() # return list with more info to console about packages, assigned to an info object

install.packages("readr") # installs the readr package
remove.packages("readr") # removes unwanted packages
old.packages() # list of packages needing updates

update.packages() # updates all packages


```

### readr

Helpful resource for cheatsheets/info, documentation

### CRAN

long, specific documentation

### Tidyverse

- collection of functions, data, docs that extends the capabilities of base R
- common philosophy of data and R programming, and are designed to work together naturally
-  Data wrangling with dplyr
   -  select rows/columns by value
   -  reorder rows
   -  create new variables
   -  collapse many values down to a single summary

## Getting Help

- use `?class` to learn more about classes
- or use `help("class")` 
  
### Reprex

reproducible examples:

1. make code reproducible
   1. include all packages
   2. include code to create all necessary objects
2. make it minimal - exclude everything that is not directly related to the problem
3. use reprex package to test that your ex is truly reproducible

