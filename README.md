
[![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/congressbr)](https://cran.r-project.org/package=congressbr) [![Travis-CI Build Status](https://travis-ci.org/RobertMyles/congressbr.svg?branch=master)](https://travis-ci.org/RobertMyles/congressbr)

congressbr
----------

congressbr is a package for extracting data from the APIs of the Brazilian Federal Senate and Chamber of Deputies, respectively.

### Installation

As of yet, congressbr is not on CRAN. It can be installed with the devtools package:

``` r
devtools::install_github("RobertMyles/congressbr")
```

### Function naming

We follow [googlesheets](https://github.com/jennybc/googlesheets) in using a naming convention for functions that facilitates tab completion. All Senate-related functions start with `sen_` and all Chamber-related ones start with `cham_`.

### Principal functions

-   `cham_votes()`: returns voting information from the Chamber of Deputies.
-   `cham_bills()`: returns bill information from the Chamber of Deputies.
-   `sen_votes()`: returns voting information from the Federal Senate.
-   `sen_bill_search()`: search for legislature in the Senate.

### Vignettes

You can learn more about the package with the vignettes. Run `vignette("Exploring the Brazilian Federal Senate")` to download and explore data from the Federal Senate, and `vignette("Exploring the Brazilian Chamber of Deputies")` to do the same for the Chamber of Deputies.

### Contributions

If you would like to get involved, feel free to fork the repo. We've been using the [Udacity Git Commit Message Style Guide](https://udacity.github.io/git-styleguide/) (well, not *always*). There are a list of open [issues](https://github.com/RobertMyles/congressbr/issues), which is a good place to start. The API of the Federal Senate is also under development, and so elements of this package may change. If you find any problems with the package, please open an issue and leave us a reproducible example and we'll get it fixed asap.
