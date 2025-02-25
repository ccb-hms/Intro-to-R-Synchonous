## Day 1 Homework Exercises

***

- The exercises below should be uploaded to the [R_nanocourse_assignment#1 Dropbox folder](https://www.dropbox.com/request/jLw5bC0YMkWa2clhCez6) by **5pm** on **Thursday, September 22nd**.
- Add your solutions to the exercises in the [downloaded .R file](https://hbctraining.github.io/Intro-to-R-flipped/homework/day1_hw_exercises.R) and upload the saved file, **renamed with your initials/name** to Dropbox.
- Specific questions regarding the homework that you would like to have reviewed in class can be asked [here](PollEv.com/ccbtraining).
- Full attendance and submission of all assignments are required for course completion.

***

### R syntax and data structures

1. Try changing the value of the variable `x` to 5. What happens to `number`?

2. Now try changing the value of variable `y` to contain the value 10. What do you need to do, to update the variable `number`?

3. Try to create a vector of numeric and character values by combining the two vectors that we just created (`glengths` and `species`). Assign this combined vector to a new variable called `combined`. Hint: you will need to use the combine `c()` function to do this. Print the `combined` vector in the console, what looks different compared to the original vectors?

4. Let's say that in our experimental analyses, we are working with three different sets of cells: normal, cells knocked out for geneA (a very exciting gene), and cells overexpressing geneA. We have three replicates for each celltype.

    1. Create a vector named `samplegroup` with nine elements: 3 control ("CTL") values, 3 knock-out ("KO") values, and 3 over-expressing ("OE") values.

    1. Turn `samplegroup` into a factor data structure.

5. Create a data frame called `favorite_books` with the following vectors as columns:

     ```r
     titles <- c("Catch-22", "Pride and Prejudice", "Nineteen Eighty Four")
     pages <- c(453, 432, 328)
     ```
  
6. Create a list called `list2` containing `species`, `glengths`, and `number`.

### Functions and arguments

1. Let's use base R function to calculate **mean** value of the `glengths` vector. You might need to search online to find what function can perform this task.

2. Create a new vector `test <- c(1, NA, 2, 3, NA, 4)`. Use the same base R function from exercise 1 (with addition of proper argument), and calculate mean value of the `test` vector. The output should be `2.5`.
	> *NOTE:* In R, missing values are represented by the symbol `NA` (not available). It’s a way to make sure that users know they have missing data, and make a conscious decision on how to deal with it. There are ways to ignore `NA` during statistical calculations, or to remove `NA` from the vector. More information related to missing data can be [found here](https://www.statmethods.net/input/missingdata.html).

3. Another commonly used base function is `sort()`. Use this function to sort the `glengths` vector in **descending** order.

4. Write a function called `multiply_it`, which takes two inputs: a numeric value `x`, and a numeric value `y`. The function will return the product of these two numeric values, which is `x * y`. For example, `multiply_it(x=4, y=6)` will return output `24`.


### Reading in and inspecting data

1. Download [this tab-delimited .txt file](https://www.dropbox.com/s/k2mlcqn4823g400/project-summary.txt?dl=1) and save it in your project’s "data" folder.

    1. Read it in to R using `read.table()` and store it as the variable `proj_summary`. As you use `read.table()`, keep in mind that:       
        * all the columns in the input text file have column names 
        * you want the first column of the text file to be used as row names (hint: look up the row.names = argument
    1. Display the contents of `proj_summary` in your console

2. Use the `class()` function on the `glengths` and `metadata` objects, how does the output differ between the two?

3. Use the `summary()` function on the `proj_summary` dataframe
      * What is the median "rRNA_rate"?
      * How many samples got the “low” level of treatment?

4. How long is the `samplegroup` factor?

5. What are the dimensions of the `proj_summary` dataframe?

6. When you use the `rownames()` function on `metadata`, what is the *data structure* of the output?

7. [Optional] How many elements in (how long is) the output of `colnames(proj_summary)`? Don’t count, but use another function to determine this.
