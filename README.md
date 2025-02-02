
<!-- README.md is generated from README.Rmd. Please edit that file -->

# regexcite

<!-- badges: start -->

<!-- badges: end -->

The goal of `regexcite` is to provide convenience functions for working
with regular expressions and string manipulation in R, making these
tasks more intuitive and user-friendly.

## Installation

You can install the development version of `regexcite` from
[GitHub](https://github.com) using the `devtools` package:

``` r
# install.packages("devtools")
devtools::install_github("Elshaday-Tamire/regexcite")
```

## Example

A common use case for string manipulation is splitting a single string
into individual components. This package provides the `str_split_one()`
function to handle such tasks conveniently:

``` r
library(regexcite)

# A basic example of splitting a string
x <- "alfa,bravo,charlie,delta"
str_split_one(x, pattern = ",")
#> [1] "alfa"    "bravo"   "charlie" "delta"
#> [1] "alfa"    "bravo"   "charlie" "delta"
```

The function also supports additional features from
`stringr::str_split()`, such as specifying the maximum number of splits
or using fixed patterns:

``` r
# Limit the number of splits
str_split_one(x, pattern = ",", n = 2)
#> [1] "alfa"                "bravo,charlie,delta"
#> [1] "alfa" "bravo,charlie,delta"

# Use fixed patterns
y <- "192.168.0.1"
str_split_one(y, pattern = stringr::fixed("."))
#> [1] "192" "168" "0"   "1"
#> [1] "192" "168" "0"   "1"
```

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

``` r
summary(cars)
#>      speed           dist       
#>  Min.   : 4.0   Min.   :  2.00  
#>  1st Qu.:12.0   1st Qu.: 26.00  
#>  Median :15.0   Median : 36.00  
#>  Mean   :15.4   Mean   : 42.98  
#>  3rd Qu.:19.0   3rd Qu.: 56.00  
#>  Max.   :25.0   Max.   :120.00
#>      speed           dist       
#>  Min.   : 4.0   Min.   :  2.00  
#>  1st Qu.:12.0   1st Qu.: 26.00  
#>  Median :15.0   Median : 36.00  
#>  Mean   :15.4   Mean   : 42.98  
#>  3rd Qu.:19.0   3rd Qu.: 56.00  
#>  Max.   :25.0   Max.   :120.00
```

You’ll still need to render `README.Rmd` regularly to keep `README.md`
up-to-date. `devtools::build_readme()` is handy for this.

You can also embed plots, for example:

<img src="man/figures/README-pressure-1.png" width="100%" />

In that case, don’t forget to commit and push the resulting figure
files, so they display on GitHub and CRAN.
