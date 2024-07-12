# Print To Console

For data visualization and watching the change of the data for imposing some operation printing to console is a banana in dessert.

## General Printing

### Basic Print function \~ print( )

The `print()` function is the most basic way to print values to the console.

```r
print("Hello, R!")
print(42)
print(c(1, 2, 3, 4, 5))
```

> OUTPUT
>
> ```r
> > print("Hello, R!")
> [1] "Hello, R!"
> > print(42)
> [1] 42
> > print(c(1, 2, 3, 4, 5))
> [1] 1 2 3 4 5
> ```



### Object Print function \~ cat( )

The `cat()` function concatenates and prints objects. It's useful for printing strings without quotes and for combining multiple items.

```r
cat("Hello,", "R!", "\n")
cat("The answer is", 42, "\n")
```

> OUTPUT
>
> ```r
> > cat("Hello,", "R!", "\n")
> Hello, R! 
> > cat("The answer is", 42, "\n")
> The answer is 42
> ```

### Message Print function \~ message( )

The `message()` function prints a message to the console, prefixed by "Message:".

```r
message("This is a message.")
```

> OUTPUT
>
> ```r
> > message("This is a message.")
> [messege] -> This is a message.
> ```

### Warning Print function \~ warning( )

The `warning()` function prints a warning message to the console.

```r
warning("This is a warning!")
```

> OUTPUT
>
> ```r
> > warning("This is a warning!")
> [warning !] -> This is a warning!
> ```

### Stop Print function \~ stop( )

The `stop()` function prints an error message and stops execution.

```r
stop("This is an error!")
```

> OUTPUT
>
> ```r
> > stop("This is an error!")
> Error: This is an error!
> ```



## Printing Different Data Types

### vectors

Vectors can be printed using `print()`, `cat()`, or directly by typing the variable name.

```r
vec <- c(1, 2, 3, 4, 5)
print(vec)
cat(vec, "\n")
vec
```

> OUTPUT
>
> ```r
> > vec <- c(1, 2, 3, 4, 5)
> > print(vec)
> [1] 1 2 3 4 5
> > cat(vec, "\n")
> 1 2 3 4 5 
> > vec
> [1] 1 2 3 4 5
> ```



### Lists

Lists can be printed using `print()` or `str()` for a structured display.

```r
my_list <- list(name = "Alice", age = 25, scores = c(85, 90, 88))
print(my_list)
str(my_list)
```

> OUTPUT
>
> ```r
> > print(my_list)
> $name
> [1] "Alice"
>
> $age
> [1] 25
>
> $scores
> [1] 85 90 88
> ```
>
> ```r
> > str(my_list)
> List of 3
>  $ name  : chr "Alice"
>  $ age   : num 25
>  $ scores: num [1:3] 85 90 88
> ```



## Matrices

Matrices can be printed using `print()` or `cat()`.

```r
mat <- matrix(1:9, nrow = 3)
print(mat)
cat(mat, "\n")
```

> OUTPUT
>
> ```r
> > cat(mat, "\n")
> 1 2 3 4 5 6 7 8 9 
> ```
>
> ```r
> > print(mat)
>      [,1] [,2] [,3]
> [1,]    1    4    7
> [2,]    2    5    8
> [3,]    3    6    9
> ```





## Printing to Files

You can write outputs to files using functions like `write()`, `write.table()`, `write.csv()`, and `write.xlsx()` from the `openxlsx` package for Excel files.

```r
write("Hello, R!", file = "output.txt")
write.table(df, file = "data.txt", sep = "\t", row.names = FALSE)
write.csv(df, file = "data.csv", row.names = FALSE)

library(openxlsx)
write.xlsx(df, file = "data.xlsx")
```

This will create a excel file in work directory and then it saves the data formatted in that file.



















