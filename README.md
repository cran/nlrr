<!-- README.md is generated from README.Rmd. Please edit that file -->
nlrr
====

This package  can be used to calculate the non-linear odds ratio compared to a given reference value for a continuous variable.

Installation
============

This package is not on [CRAN](http://cran.r-project.org/).

Functions
=========

The first function, `nlor`, calculate the odds ratios and 95% confidence intervals for the continuous exposure variable given the reference value. The default reference value is the median of the exposure variable. If the user defines the reference value that is within the exposure range of dataset, then the user defined reference value is used.

The outout of this function is a dataset, which contains these following variables: the exposure, odds ratio, 95% upper limit of odds ratio, 95% lower limit of odds ratio, and the reference value.

The second function, `nlorplot` utilizes the output from `nlor`. It generates a plot, in which the x-axis is the continuous exposure variable, and y-axis is the odds ratio and 95% confidence interval.

Example
=======

``` r
sum1 <- nlor(exposure = 'lipid', outcome = 'dm', covar = c('age', 'gender'), xref = 0.6, data = Lipid)

nlorplot('lipid', 'or', data = sum1, xlab = 'Lipid')
```
