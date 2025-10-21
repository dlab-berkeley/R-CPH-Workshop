# R Haas Departmental Workshop

The goal of this Departmental Workshop is to provide a light introduction to R. We aim to build up to data frames, which are one of the most commonly used data structures in R.

## Jupyter Notebooks

This course will be using a Jupyter Notebook to interact with R.  The bit of extra setup is well worth it because the Notebook provides code completion and other helpful features.

Notebook files have the extension ".ipynb" to distinguish them from other Python (e.g., ".py") files.


### Open Jupyter Notebook on Haas DataHub

We *strongly* recommend using either the DataHub to run the materials for these lessons. You can access either DataHub by clicking this button:

[![D-Lab DataHub](https://img.shields.io/badge/launch-D--Lab%20datahub-blue)](https://dlab.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Fdlab-berkeley%2FR-Haas-Workshop&urlpath=tree%2FR-Haas-Workshop%2Flessons%2F01_introduction.ipynb&branch=main)

Some users may have to click the link twice if the materials do not load initially.

The DataHub downloads this repository, along with any necessary packages, and allows you to run the materials in an instance on UC Berkeley's servers. No installation is needed from your end - you only need an internet browser and a CalNet ID to log in. By using the DataHub, you can save your work and come back to it at any time.

### Navigating in Jupyter Notebook

Jupyter Notebooks have more useful features for interactive use than a standard interpreter, but they work in the same basic way: you type things and then execute them.

Unlike many graphical systems, you don't need to press a button to run your code! Instead, **you typically run code using Shift-Enter**. This also moves you to the next box (or "cell") for code below the one you just ran.

Using Jupyter notebooks has several advantages:

- You can easily type, edit, and copy and paste blocks of code.
- Tab complete allows you to easily access the names of things you are using and learn more about them.
- It allows you to annotate your code with links, different sized text, bullets, etc., to make it more accessible to you and your collaborators.
- It allows you to display figures next to the code that produces them to tell a complete story of the analysis.
- The notebook is stored as JSON but can be saved as a .py file if you would like to run it from the Bash shell or a Python interpreter.

## Variable Assignment

Variables are objects that hold values. Variables can be inside data sets (like columns in an excel sheet) or stand alone objects. The syntax for creating a variable is:

-   Left hand side is the variable name

-   Next is the **assignment** **operator**: `<-`

-   Right hand side is the value to assign to that variable



```R
# A variable that gives the year 
year <- 2023
```


```R
# Print out the value
year
```


```R
# You can also use the '=' operator to do variable assignment. 
number = 5
```

There are subtle differences between `<-` and `=`, which won't matter in most cases. However, using `<-` is considered good code style. You want your code to adhere to good stylistic practices, since that makes it easier to read and use by other users.

We can read the above code as "create a variable called `year` and assign to it the value 2023".

Variables can hold different types of values.


```R
# Assign a numeric value to the variable year
year <- 2023

# Assign a character value to the variable country
country <- "Mexico"

# Assign a numeric value to the variable lifeexp
lifeexp <- 76.2
```

Use a hashtag to comment your code (e.g., write notes to your future self and your collaborators) to help keep your script organized. 

## 🥊 Challenge 1

Create a variable called `continent` and assign it the value "Americas". Create variable called `pop` and assign it the value 4.5.


```R
# YOUR CODE HERE

```

---

You can remove variables from the global environment.


```R
# Remove a single variable
rm(year)

# Remove all variables in the global environment
rm(list = ls())
```

⚠️ You cannot undo removing a variable. You must instead re-create the variable.

If you want to rename a variable, the easiest thing to do is create a variable with the new name and remove the old variable.



```R
# Variable storing the population of Mexico
pop <- 126

# Rename to be more informative
pop_millions <- pop

# Print it to confirm that it holds the value of pop
pop_millions

# Remove the old variable
rm(pop)

# Print out a list of current variables
ls()
```

💡`ls()` and `rm()` are both **functions**, which are commands that generate some output. We will learn several functions across the workshop. The best way to learn and remember functions in R is it to Google them!

## Creating Vectors

Most of the time, we want to store multiple values. For example, I might want to record the population in Mexico from 2018 to 2022. **Vectors** can store multiple values as long as they're the same type (all numeric, all characters etc).

To create a vector, you use the `c()` function, which stands for concatenate (meaning combine).


```R
# Create a vector with the approx population of Mexico for 5 years  
c(123, 124, 125, 126, 127)

# As chance would have it, Mexico's population has increased by
# about 1 million each year from 2018 to 2022
```

Vectors are assigned to variables using the same assignment operator (\<-) that we used for single value variables.


```R
# Save the population counts to a vector
pop_mexico <- c(123, 124, 125, 126, 127)
pop_mexico
```

If we do something to the values in a vector, R applies that operation to each item in the vector.


```R
# Multiple the values in pop_mexico by 1 million
pop_mexico * 1000000

# You forgot to count 2 million people - add them to our counts
pop_mexico + 2
```

## Functions

As well as mathematical operations, we can apply **functions** to vectors, for example the function `length()`.


```R
length(pop_mexico)
```

More generally, functions are commands that take an input and return some output. They are identified by the trailing parentheses. Inside the brackets go:

1.  **input** - the thing that the function is doing something to

2.  **arguments** - modifications we make to the function (the first argument is usually the input)

🔔 What is the **input** for the `length()` function?


```R
length(pop_mexico)
```

⚠️ Not all functions have inputs or arguments - for example, the `ls()` function doesn't require an input but still gives us an output.


```R
ls()
```

We can modify functions by changing the **arguments** in the function. The function `mean()` has several arguments, which we can look at in the help page.


```R
# look up what the mean() functions does and what arguments it uses
?mean
```

## Data frames

**Vectors** are variables that store multiple values of the same type (all numbers or all words). Most of the time, we want to work with data that have multiple variables - we call this **multidimensional data**. In R, we use **data frames** to store multidimensional data.

In R language, a data frame is an object containing multiple vectors of the same length. The values in a given vector are all the same type, but the vectors may each hold a different type of value. In everyday language, a data frame is a collection of variables (columns). Each variable contains the same number of observations (rows).

![](https://r4ds.hadley.nz/images/tidy-1.png "Test")


### 🥊 Challenge 2: Your own data

Think of an example of data you have worked with. What are the observations (the unit of measurement)? What are the variables (the information being measured)?

⚠️ Data frames are not the only way to store multidimensional data in R - but they are the most common and easiest to work with.

## Import data

You can create a data frame in R and fill it with values. Normally though, you **import** data and save it as a data frame. You can import many different types of files into R (eg. excel sheets, csv files, dta files). Today we will import a csv file.



```R
# Import csv file 
gap <- read.csv("gapminder.csv")
```

🔔 The code above returned an error - why do you think this is?

When we read in data, we need to specify the **relative file path**. This means, from our **current working directory**, how do we get to the file we want to import.


```R
# Print out our current working directory
getwd()

# Read in gap data using a relative file path
gap <- read.csv("../data/gapminder.csv")
```

💡 Within a file path, a period "." means "in this directory". A double period ".." means "go back one directory".

⚠️ In R Notebooks, the working directory is always the directory in which the notebook is saved in - so all data needs to be read in relative to that directory. In R Scripts, you can change the working directory at the start of your script by using the `setwd()` function.

After importing data, the first thing to check is if the data looks like you expected it to.


```R
# Examine our data
head(gap)
```

## Subsetting data frames

We often want to work with **subsets** of our data. A subset is a portion or slice of our data. It could be a subset of rows, for example, if we wanted to see all rows for the country Argentina. It could also be a subset of columns, for example, if we wanted to see only population and year. It could also be a combination of rows and columns. We do this by **indexing**.

Indexing refers to specifying the rows or columns that we want to extract from an object. It is done using **square brackets**. For a single vector, we extract a specific element by providing the index of that value (index means its place in the vector).


```R
# Create a vector with years from 2000 to 2010 in 
years <- 2000:2010
years

# Extract the 5th element of that vector
years[5]

# Extract the 12th element of that vector - what happens?
years[12]
```

Because data frames are two dimensional, we can specify the rows and the columns we want. The format is: **data.frame[rows, columns]**. By leaving either rows or columns blank, that selects all of them.

To extract a single variable, we specify the variable name withing the square brackets. This returns all the rows but only one column.


```R
# Extract a single variable using the indexing method 
gap["pop"]
```

We can index **multiple** columns. This is done by providing a vector of variable names inside the square brackets.


```R
# Extract multiple variables using the indexing method
gap[c("pop", "year")]

# We can also define the vector of names first
variables <- c("pop" , "year", "lifeExp")
gap[variables]
```

## 🎬 Demo

As well as subsetting columns, we can also subset rows. To do this, we use **conditional statements** to tell R which rows we want to return.

🔔 Run the chunk of code below. What do you think we are doing?


```R
library(dplyr)
```


```R
gap %>%
  filter(year == 2007 | year == 1952) %>%
  select(gdpPercap, lifeExp, continent, year) 
```

This concludes our brief introduction into R!

This introduction basically consisted of creating different kinds of variables. But what if we want to _do_ things with those variables? R provides many tools for additional analyses you can conduct on, for example, your dataframe. We encourage you to check out [R-Fundamentals](https://github.com/dlab-berkeley/R-Fundamentals) to learn more about these additional functionalities!
