
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->
<!-- badges: end -->

# CRAN-like Package Repository

This repo is an example of how you can build an R package repository
using GitHub Pages and the {drat} package.

## For package users - how to install packages

### Specify the repo argument

For example, you can install {packageA} like this:

``` r
install.packages("packageA", repos = "https://dragosmg.github.io/internal-cran/")
```

### Add internal-cran to your .Rprofile

Add `internal-cran` to your list or repositories by adding the following
to your `.Rprofile`:

``` r
local({
  r <- getOption("repos")
  r["Internal CRAN"] <- "https://dragosmg.github.io/internal-cran/"
  options(repos = r)
})
```

After that you can simply install packages like normal. For example, you
can install {packageA} like this:

``` r
install.packages("packageA")
```

### For package authors
