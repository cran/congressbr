
[![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/congressbr)](https://cran.r-project.org/package=congressbr)
[![Travis-CI Build
Status](https://travis-ci.org/RobertMyles/congressbr.svg?branch=master)](https://travis-ci.org/RobertMyles/congressbr)
[![AppVeyor Build
Status](https://ci.appveyor.com/api/projects/status/github/RobertMyles/congressbr?branch=master&svg=true)](https://ci.appveyor.com/project/RobertMyles/congressbr)
[![CRAN\_Download\_Badge](http://cranlogs.r-pkg.org/badges/congressbr)](https://CRAN.R-project.org/package=congressbr)
[![CRAN\_Download\_Badge](http://cranlogs.r-pkg.org/badges/grand-total/congressbr)](https://CRAN.R-project.org/package=congressbr)

## 🇧🇷 congressbr

congressbr is a package for extracting data from the APIs of the
Brazilian Federal Senate and Chamber of Deputies, respectively.

### Installation

congressbr is on CRAN, and so can be installed with the following:

``` r
install.packages("congressbr")
```

Development versions can be installed with the devtools package:

``` r
devtools::install_github("RobertMyles/congressbr")
```

### Function naming

We follow [googlesheets](https://github.com/jennybc/googlesheets) in
using a naming convention for functions that facilitates tab completion.
All Senate-related functions start with `sen_` and all Chamber-related
ones start with `cham_`.

### Principal functions

  - `cham_votes()`: returns voting information from the Chamber of
    Deputies.
  - `cham_bills()`: returns bill information from the Chamber of
    Deputies.
  - `sen_votes()`: returns voting information from the Federal Senate.
  - `sen_bill_search()`: search for legislature in the Senate.

### Vignettes

You can learn more about the package with the vignettes. Run
`vignette("Exploring the Brazilian Federal Senate")` to download and
explore data from the Federal Senate, and `vignette("Exploring the
Brazilian Chamber of Deputies")` to do the same for the Chamber of
Deputies.

### Datasets

`congressbr` comes with some pre-prepared datasets.

  - `data("commissions")` returns a dataframe of commissions, with two
    columns, the full name of the commission, and the abbreviations used
    in some of the other functions in `congressbr` and in much of the
    literature on the institution.

  - `data("sen_nominal_votes")` is a dataframe of all the nominal votes
    in the Senate between 1991 and early 2017 (the Senate API only
    allows requests for a maximum period of 60 days).

  - `data("cham_nominal_votes")` is a dataframe of nominal votes in the
    Chamber of Deputies from 1991 to 2017.

### Contributions

If you would like to get involved, feel free to fork the repo. We’ve
been using the [Udacity Git Commit Message Style
Guide](https://udacity.github.io/git-styleguide/) (well, not *always*).
There are a list of open
[issues](https://github.com/BrazilianPublicData/congressbr/issues),
which is a good place to start. The API of the Federal Senate is also
under development, and so elements of this package may change. If you
find any problems with the package, please open an issue and leave us a
reproducible example and we’ll get it fixed asap.

### Citation

If you use this package in academic work, it can be cited with:

``` r

citation("congressbr")
```

which will give you:

    To cite package ‘congressbr’ in publications use:
    
      Robert Myles McDonnell, Guilherme Jardim Duarte and Danilo Freire (2017). congressbr:
      Downloads, Unpacks and Tidies Legislative Data from the Brazilian Federal Senate and
      Chamber of Deputies. R package version 0.1.0.
      https://CRAN.R-project.org/package=congressbr
    
    A BibTeX entry for LaTeX users is
    
      @Manual{,
        title = {congressbr: Downloads, Unpacks and Tidies Legislative Data from the
    Brazilian Federal Senate and Chamber of Deputies},
        author = {Robert Myles McDonnell and Guilherme Jardim Duarte and Danilo Freire},
        year = {2017},
        note = {R package version 0.1.0},
        url = {https://CRAN.R-project.org/package=congressbr},
      }

## List of functions

For convenience, we list here the functions of the package. More details
are available [here](https://CRAN.R-project.org/package=congressbr).
**Note**: The information returned by some of the functions below is no
longer available from the API. Hopefully in a future release, we’ll be
able to re-include these functions. (Functions are marked by
strikethrough text.)

  - `cham_bills`: Downloads and tidies data for lists of bills in
    Brazilian Chamber of Deputies.
  - `cham_bill_info`: Downloads details of a specific bill by providing
    type, number and year.  
  - `cham_bill_info_id`: Downloads details of a specific bill by
    providing id of a bill.
  - `cham_plenary_bills`: This function lists every bill voted on in the
    plenary.
  - `cham_typeauthors_bills`: Types of authors for bills.
  - `cham_votes`: Downloads votes of a specific bill by providing type,
    number and year. A bill can have more than one roll call, and the
    API does not provide an id to identify them So we provide one
    (rollcall\_id).  
  - `sen_agenda`: Returns info on the agenda in the Federal Senate.
  - `sen_bills`: Information on the legislation in the Federal Senate.
  - `sen_bills_current`: Downloads and tidies information on legislation
    from the *current* legislature of the Federal Senate.
  - `sen_bills_limits`: Downloads and tidies information on the types of
    deadline and time limits for legislation in the Federal Senate.
  - `sen_bills_list`: Information on the types of acts that can be
    formally made in the Federal Senate.
  - `sen_bills_locations`: Downloads and tidies information on the
    possible locations a piece of legislation can currently be passing
    through the Federal Senate.
  - `sen_bills_passage`: Downloads and tidies information on the
    locations a piece of legislation is currently passing through.
  - `sen_bills_passing`: Downloads and tidies information on legislation
    that is currently under consideration in the Senate.
  - `sen_bills_situations`: Possible situations a bill can be in.
  - `sen_bills_topics`: Downloads and tidies information on the topics
    of legislation in the Federal Senate.
  - `sen_bills_types`: Information on the types of legislation in the
    Senate.
  - `sen_bills_updates`: Info on bills that have been recently updated.
  - `sen_bills_update_types`: Information on the types of updates that
    can be applied to bills in the Federal Senate.
  - `sen_bill_search`: Search for data on legislation in the Brazilian
    Federal Senate.
  - `sen_bill_sponsors`: Bill sponsors in the Senate.
  - `sen_budget`: Downloads and tidies budget information from the
    Federal Senate.
  - `sen_coalitions`: Downloads and tidies data on the coalitions in the
    Federal Senate
  - ~~`sen_coalition_info`: Downloads and tidies data on *specific*
    coalitions in the Federal Senate.~~
  - `sen_commissions`: Information on commissions in the Senate.
  - `sen_commissions_senators`: Information on the senators who serve on
    a certain commission in the Federal Senate.
  - `sen_commissions_type`: Information on commissions in the Federal
    Senate, by commission type.
  - `sen_commission_positions`: Information on positions (jobs) that
    legislators may occupy in commissions in the Federal Senate
  - `sen_parties`: Downloads and tidies information on the political
    parties in the Federal Senate.
  - `sen_plenary_agenda`: Returns results from the plenary in the
    Federal Senate for a specified date.
  - `sen_plenary_leaderships`: Returns information on leaderships in the
    Federal Senate.
  - `sen_plenary_result`: Returns results from the plenary in the
    Federal Senate for a specified date.
  - `sen_plenary_sessions`: Returns the types of sessions in the Federal
    Senate.
  - `sen_senator`: Downloads and tidies personal information on
    senators. Includes absences and mandates.
  - ~~`sen_senator_bills`: Downloads and tidies information on bills
    that certain senators have sponsored/authored in the Senate.~~
  - ~~`sen_senator_commissions`: Downloads and tidies information on the
    commissions on which senators have served or are serving in the
    Federal Senate.~~
  - `sen_senator_details`: Downloads and tidies personal information on
    the senators.
  - `sen_senator_legis`: Downloads and tidies information on the
    senators, by legislature.
  - `sen_senator_list`: Returns a list of senators.
  - `sen_senator_mandates`: Downloads and tidies information on
    senators’ mandates.
  - `sen_senator_suplentes`: Downloads and tidies information on titular
    senators and their *suplentes*.
  - `sen_senator_votes`: Returns information on senators’ voting
    histories.
  - `sen_sponsor_types`: Types of bill sponsors.
  - `sen_statement_list`: Types of declarations senators can make.
  - `sen_votes`: Returns voting information from the Senate floor for
    the date requested.
  - `statesBR`: A dataframe of Brazilian states, by their sigla
    (acronym) and full name.
  - `UF`: This function prints out a character vector of Brazilian state
    abbreviations to the console.
