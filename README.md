# GitHub repository for ‘Effects of Minimum Wages’
GitHub repository with replication code (.Rmd, .html) for ‘Effects of Minimum Wages: A 1994 State of Washington Case Study’

# Instructions:
Use the .html file to preview the code and corresponding results. To replicate and edit, use the .Rmd file. 

sessionInfo {utils}: Collect Information About the Current R Session

``` r
sessioninfo::session_info()
```

    ## - Session info ---------------------------------------------------------------
    ##  setting  value
    ##  version  R version 4.1.2 (2021-11-01)
    ##  os       Windows 10 x64 (build 19042)
    ##  system   x86_64, mingw32
    ##  ui       RTerm
    ##  language (EN)
    ##  collate  German_Switzerland.1252
    ##  ctype    German_Switzerland.1252
    ##  tz       Europe/Berlin
    ##  date     2022-01-19
    ##  pandoc   2.14.0.3 @ C:/Program Files/RStudio/bin/pandoc/ (via rmarkdown)
    ## 
    ## - Packages -------------------------------------------------------------------
    ##  package     * version date (UTC) lib source
    ##  arules      * 1.7-3   2022-01-09 [1] CRAN (R 4.1.2)
    ##  assertthat    0.2.1   2019-03-21 [2] CRAN (R 4.1.1)
    ##  backports     1.3.0   2021-10-27 [2] CRAN (R 4.1.1)
    ##  broom         0.7.10  2021-10-31 [2] CRAN (R 4.1.1)
    ##  cellranger    1.1.0   2016-07-27 [2] CRAN (R 4.1.1)
    ##  cli           3.1.0   2021-10-27 [2] CRAN (R 4.1.1)
    ##  colorspace    2.0-2   2021-06-24 [2] CRAN (R 4.1.1)
    ##  crayon        1.4.2   2021-10-29 [2] CRAN (R 4.1.1)
    ##  DBI           1.1.1   2021-01-15 [2] CRAN (R 4.1.1)
    ##  dbplyr        2.1.1   2021-04-06 [2] CRAN (R 4.1.1)
    ##  digest        0.6.28  2021-09-23 [2] CRAN (R 4.1.1)
    ##  dplyr       * 1.0.7   2021-06-18 [2] CRAN (R 4.1.1)
    ##  ellipsis      0.3.2   2021-04-29 [2] CRAN (R 4.1.1)
    ##  evaluate      0.14    2019-05-28 [2] CRAN (R 4.1.1)
    ##  fansi         0.5.0   2021-05-25 [2] CRAN (R 4.1.1)
    ##  fastmap       1.1.0   2021-01-25 [2] CRAN (R 4.1.1)
    ##  forcats     * 0.5.1   2021-01-27 [2] CRAN (R 4.1.1)
    ##  fs            1.5.0   2020-07-31 [2] CRAN (R 4.1.1)
    ##  generics      0.1.1   2021-10-25 [2] CRAN (R 4.1.1)
    ##  ggplot2     * 3.3.5   2021-06-25 [2] CRAN (R 4.1.1)
    ##  glue          1.4.2   2020-08-27 [2] CRAN (R 4.1.1)
    ##  gtable        0.3.0   2019-03-25 [2] CRAN (R 4.1.1)
    ##  haven       * 2.4.3   2021-08-04 [2] CRAN (R 4.1.1)
    ##  hms           1.1.1   2021-09-26 [2] CRAN (R 4.1.1)
    ##  htmltools     0.5.2   2021-08-25 [2] CRAN (R 4.1.1)
    ##  httr          1.4.2   2020-07-20 [2] CRAN (R 4.1.1)
    ##  jsonlite      1.7.2   2020-12-09 [2] CRAN (R 4.1.1)
    ##  knitr         1.36    2021-09-29 [2] CRAN (R 4.1.1)
    ##  lattice       0.20-45 2021-09-22 [2] CRAN (R 4.1.1)
    ##  lifecycle     1.0.1   2021-09-24 [2] CRAN (R 4.1.1)
    ##  lubridate     1.8.0   2021-10-07 [2] CRAN (R 4.1.1)
    ##  magrittr      2.0.1   2020-11-17 [2] CRAN (R 4.1.1)
    ##  Matrix      * 1.3-4   2021-06-01 [2] CRAN (R 4.1.1)
    ##  mnormt        2.0.2   2020-09-01 [1] CRAN (R 4.1.1)
    ##  modelr        0.1.8   2020-05-19 [2] CRAN (R 4.1.1)
    ##  munsell       0.5.0   2018-06-12 [2] CRAN (R 4.1.1)
    ##  nlme          3.1-153 2021-09-07 [2] CRAN (R 4.1.1)
    ##  pillar        1.6.4   2021-10-18 [2] CRAN (R 4.1.1)
    ##  pkgconfig     2.0.3   2019-09-22 [2] CRAN (R 4.1.1)
    ##  psych       * 2.1.9   2021-09-22 [1] CRAN (R 4.1.2)
    ##  purrr       * 0.3.4   2020-04-17 [2] CRAN (R 4.1.1)
    ##  R6            2.5.1   2021-08-19 [2] CRAN (R 4.1.1)
    ##  Rcpp          1.0.7   2021-07-07 [2] CRAN (R 4.1.1)
    ##  readr       * 2.0.2   2021-09-27 [2] CRAN (R 4.1.1)
    ##  readxl        1.3.1   2019-03-13 [2] CRAN (R 4.1.1)
    ##  reprex        2.0.1   2021-08-05 [2] CRAN (R 4.1.1)
    ##  rlang         0.4.12  2021-10-18 [2] CRAN (R 4.1.1)
    ##  rmarkdown     2.11    2021-09-14 [2] CRAN (R 4.1.1)
    ##  rstudioapi    0.13    2020-11-12 [2] CRAN (R 4.1.1)
    ##  rvest         1.0.2   2021-10-16 [2] CRAN (R 4.1.1)
    ##  scales      * 1.1.1   2020-05-11 [2] CRAN (R 4.1.1)
    ##  sessioninfo   1.2.2   2021-12-06 [1] CRAN (R 4.1.2)
    ##  stringi       1.7.5   2021-10-04 [2] CRAN (R 4.1.1)
    ##  stringr     * 1.4.0   2019-02-10 [2] CRAN (R 4.1.1)
    ##  tibble      * 3.1.5   2021-09-30 [2] CRAN (R 4.1.1)
    ##  tidyr       * 1.1.4   2021-09-27 [2] CRAN (R 4.1.1)
    ##  tidyselect    1.1.1   2021-04-30 [2] CRAN (R 4.1.1)
    ##  tidyverse   * 1.3.1   2021-04-15 [2] CRAN (R 4.1.1)
    ##  tmvnsim       1.0-2   2016-12-15 [1] CRAN (R 4.1.1)
    ##  tzdb          0.2.0   2021-10-27 [2] CRAN (R 4.1.1)
    ##  utf8          1.2.2   2021-07-24 [2] CRAN (R 4.1.1)
    ##  vctrs         0.3.8   2021-04-29 [2] CRAN (R 4.1.1)
    ##  withr         2.4.2   2021-04-18 [2] CRAN (R 4.1.1)
    ##  xfun          0.27    2021-10-18 [2] CRAN (R 4.1.1)
    ##  xml2          1.3.2   2020-04-23 [2] CRAN (R 4.1.1)
    ##  yaml          2.2.1   2020-02-01 [2] CRAN (R 4.1.1)
    ## 
    ##  [1] \\unetna01/MarxerB$/Daten/R/win-library/4.1
    ##  [2] C:/Program Files/R/library
    ## 
    ## ------------------------------------------------------------------------------
