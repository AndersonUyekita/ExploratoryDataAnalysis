`Book` Exploratory Data Analysis with R
================

-   👨🏻‍💻 Author: Anderson H Uyekita
-   📚 Specialization: <a
    href="https://www.coursera.org/specializations/data-science-foundations-r"
    target="_blank" rel="noopener">Data Science: Foundations using R
    Specialization</a>
-   📖 Course:
    <a href="https://www.coursera.org/learn/exploratory-data-analysis"
    target="_blank" rel="noopener">Exploratory Data Analysis</a>
    -   🧑‍🏫 Instructor: Roger D Peng
-   📆 Reading
    -   🚦 Start: Saturday, 04 June 2022
    -   🏁 Finish: Wednesday, 22 June 2022
-   📔 Book: <a href="https://leanpub.com/exdata" target="_blank"
    rel="noopener">Exploratory Data Analysis with R</a>

------------------------------------------------------------------------

## Notes

#### Exploratory Data Analysis Checklist

1.  [Formulate your question](#formulate_your_question)
2.  [Read in your data](#read_in_your_data)
3.  [Check the packaging](#check_the_packaging)
4.  [Run `str()`](#run_str)
5.  [Look at the top and the bottom of your data](#head_tail)
6.  [Check your “n”s](#check_your_n_s)
7.  [Validate with at least one external data source](#validate_dataset)
8.  [Try the easy solution first](#easy_first)
9.  [Challenge your solution](#challenge_your_solution)
10. [Follow up](#follow_up)

#### 1. Formulate your question <a href="" id="formulate_your_question"></a>

It will limit the number of paths.

> Which counties in the United States have the highest levels of ambient
> ozone pollution?

#### 2. Read in your data <a href="" id="read_in_your_data"></a>

``` r
# Examples
readRSD()
read_csv()
read.csv()
```

Defining the `col_types`:

-   “c” for character;
-   “n” for numeric”, and;
-   “i” for integer.

``` r
# Example
ozone <- read_csv("data/hourly_44201_2014.csv",
                  col_types = "ccccinnccccccncnncccccc")
```

#### 3. Check the packaging <a href="" id="check_the_packaging"></a>

Checking the dataset dimensions.

``` r
# Examples
dim(datasets::mtcars)
```

    ## [1] 32 11

``` r
nrow(datasets::mtcars)
```

    ## [1] 32

``` r
ncol(datasets::mtcars)
```

    ## [1] 11

#### 4. Run `str()` <a href="" id="run_str"></a>

Print the column type, number of observations (rows), and variables
(columns).

``` r
# Checking the data structure.
str(datasets::mtcars)
```

    ## 'data.frame':    32 obs. of  11 variables:
    ##  $ mpg : num  21 21 22.8 21.4 18.7 18.1 14.3 24.4 22.8 19.2 ...
    ##  $ cyl : num  6 6 4 6 8 6 8 4 4 6 ...
    ##  $ disp: num  160 160 108 258 360 ...
    ##  $ hp  : num  110 110 93 110 175 105 245 62 95 123 ...
    ##  $ drat: num  3.9 3.9 3.85 3.08 3.15 2.76 3.21 3.69 3.92 3.92 ...
    ##  $ wt  : num  2.62 2.88 2.32 3.21 3.44 ...
    ##  $ qsec: num  16.5 17 18.6 19.4 17 ...
    ##  $ vs  : num  0 0 1 1 0 1 0 1 1 1 ...
    ##  $ am  : num  1 1 1 0 0 0 0 0 0 0 ...
    ##  $ gear: num  4 4 4 3 3 3 3 4 4 4 ...
    ##  $ carb: num  4 4 1 1 2 1 4 2 2 4 ...

#### 5. Look at the top and the bottom of your data <a href="" id="head_tail"></a>

Check the first and last rows.

``` r
# First rows
head(datasets::mtcars)
```

    ##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
    ## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
    ## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
    ## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
    ## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
    ## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
    ## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1

``` r
# Last rows
tail(datasets::mtcars)
```

    ##                 mpg cyl  disp  hp drat    wt qsec vs am gear carb
    ## Porsche 914-2  26.0   4 120.3  91 4.43 2.140 16.7  0  1    5    2
    ## Lotus Europa   30.4   4  95.1 113 3.77 1.513 16.9  1  1    5    2
    ## Ford Pantera L 15.8   8 351.0 264 4.22 3.170 14.5  0  1    5    4
    ## Ferrari Dino   19.7   6 145.0 175 3.62 2.770 15.5  0  1    5    6
    ## Maserati Bora  15.0   8 301.0 335 3.54 3.570 14.6  0  1    5    8
    ## Volvo 142E     21.4   4 121.0 109 4.11 2.780 18.6  1  1    4    2

#### 6. Check your “n”s <a href="" id="check_your_n_s"></a>

Based on our knowledge of the data, it is essential to check those
numbers.

``` r
# Checking the number of observations.
dim(airquality)
```

    ## [1] 153   6

``` r
# Sneaking the data to find any NA value.
summary(datasets::airquality)
```

    ##      Ozone           Solar.R           Wind             Temp      
    ##  Min.   :  1.00   Min.   :  7.0   Min.   : 1.700   Min.   :56.00  
    ##  1st Qu.: 18.00   1st Qu.:115.8   1st Qu.: 7.400   1st Qu.:72.00  
    ##  Median : 31.50   Median :205.0   Median : 9.700   Median :79.00  
    ##  Mean   : 42.13   Mean   :185.9   Mean   : 9.958   Mean   :77.88  
    ##  3rd Qu.: 63.25   3rd Qu.:258.8   3rd Qu.:11.500   3rd Qu.:85.00  
    ##  Max.   :168.00   Max.   :334.0   Max.   :20.700   Max.   :97.00  
    ##  NA's   :37       NA's   :7                                       
    ##      Month            Day      
    ##  Min.   :5.000   Min.   : 1.0  
    ##  1st Qu.:6.000   1st Qu.: 8.0  
    ##  Median :7.000   Median :16.0  
    ##  Mean   :6.993   Mean   :15.8  
    ##  3rd Qu.:8.000   3rd Qu.:23.0  
    ##  Max.   :9.000   Max.   :31.0  
    ## 

We are trying to find any inconsistency like the max day above 31.

#### 7. Validate with at least one external data source <a href="" id="validate_dataset"></a>

Double-checking if the current data is correct with independent data or
source. Just to be sure, if you are working on the same basis and
magnitude order.

#### 8. Try the easy solution first <a href="" id="easy_first"></a>

Make it simple. You are not building a spaceship.

#### 9. Challenge your solution <a href="" id="challenge_your_solution"></a>

Challenge your most straightforward solution. You want to invalidate it.

#### 10. Follow up questions <a href="" id="follow_up"></a>

1.  Do you have the right data?

> Sometimes at the conclusion of an exploratory data analysis, the
> conclusion is that the dataset is not really appropriate for this
> question. In this case, the dataset seemed perfectly fine for
> answering the question of which counties had the highest levels of
> ozone.

2.  Do you need other data?

> One sub-question we tried to address was whether the county rankings
> were stable across years. We addressed this by resampling the data
> once to see if the rankings changed, but the better way to do this
> would be to simply get the data for previous years and re-do the
> rankings.

3.  Do you have the right question?

> In this case, it’s not clear that the question we tried to answer has
> immediate relevance, and the data didn’t really indicate anything to
> increase the question’s relevance. For example, it might have been
> more interesting to assess which counties were in violation of the
> national ambient air quality standard, because determining this could
> have regulatory implications. However, this is a much more complicated
> calculation to do, requiring data from at least 3 previous years.
