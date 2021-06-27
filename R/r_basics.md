# R Basics

## Watch this video to see the basics in action!
<iframe width="560" height="315" src="https://www.youtube.com/embed/BrsYjoGydZ8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Assigning values to variables

R is different from many language in how values are assigned to variables. With R, "=" is not the primary assignment operator, instead you utilize "<-". For example...

```r
var_1 <- 66
```

... would assign 66 to the variable "var_1". While sometimes you *can* use the equals sign, it is not recommended. It is advised to use the **<-** assignment operator to assign values to variables. 

## Basic Arithmetic Operations and functions
Like most programming languages, R can compute arithmetic operations. For example...

```r
2 + 2 
```

...would return 4. 

Arithmetic operators include: 

| Operator | Description    |
|----------|----------------|
| +        | addition       |
| -        | subtraction    |
| *        | multiplication |
| /        | division       |
| ^ or **  | exponentiation |

You can also utilize arithmetic functions, such as logarithms, exponentials, trigonometric functions, or other math functions. 

For example...
```r
abs(-20)
```

...would return 20.

Finally, you can use logical operators with R. These operators return a boolean (True/False) value. Logical operators include: 

| Operator | Description                 |
|----------|-----------------------------|
| >        | greater than                |
| >=       | greater than or equal to    |
| ==       | exactly equal to            |
| !=       | not equal to                |


## Working with matrices and random samples!

To create and store a matrix of random numbers, you can do the following. 

```r
data <- matrix(sample(16),4)
```

sample() has the following format:

```r
sample(x, size, replace = FALSE, prob = NULL)
```

sample() takes a sample of the specified size from the elements of x using either with or without replacement. 

The arguments are the following: 

* x is either a vector of elements from which to choose or a positive integer. If it is a positive integer, sampling takes place from 1:x. 
* size gives the nuber of items to choose. 
* replace defines if the sampling should be with replacement. This tells R if a number can appear more than once in your results. 
* prob is a vector of probability weigths for obtaining elements of the vector being sampled. 

---
**Helpful Hint**
To find information like this or to explore further in RStudio, use "?" followed by what you want to look at in the Console. Like... 

```r
?sample
```
---

## Working with Strings

You can also do a number of things with strings in R. 

```r
fname <- "Emily"
lname <- "Cloudman"
```
.... will assign Emily to the variable fname and Cloudman to lname. 

If we want to save the full name, we can concatenate the two strings by doing the following... 

```r
fullname <- paste(fname, lname, sep = " ")
```
... which will put the first name, followed by the last, separated by a space. Note, a common mistake is trying to combine using `c()`. Like this... 

```r
c(fname, lname) #Not recommended in this case
```
    "Emily"    "Cloudman" 

`c` is a generic function to combine its arguements, however it combined the values into a vector of a list. Thus, in this case using paste is the better in this case! c is typicaly better for numerical values you want in a list. 

If you want to print the value, you can use the print function. 

```r
print(fullname)
```
    "Emily Cloudman"
    
Commonly, information may be coded with the first two letters of the first name and first three letters of the last name. We can use R to get this information as well! 

```r
paste(substr(fname,1,2), substr(lname,1,3), sep = '')
```
    "EmClo"
    
In this case, we are telling the separator to be nothing in order to put the last name letters directly after the first name letters. using `sustr()`, the first input is the character vector that you want to extract the substring from, followed by the index of the first element to be extracted and the index of the last element to be extracted. 


Now that you know the basics, check out how to [investigate data imported from a file](https://github.gatech.edu/pages/bmclain3/Health_Analytics/R/r_analysis_example) to keep learning! 
