ftp
===



[![Build Status](https://travis-ci.org/ropensci/ftp.svg?branch=master)](https://travis-ci.org/ropensci/ftp)

An ftp client for R

**not quite ready to use yet**

## Installation


```r
devtools::install_github("ropensci/ftp")
```


```r
library('ftp')
```

## ftp client


```r
(x <- ftp("ftp://ftp.ncdc.noaa.gov/pub/data/ghcn/"))
#> <ftp client> 
#>   base url: ftp://ftp.ncdc.noaa.gov/pub/data/ghcn/
#>   port: 21
#>   active/passive: passive
```

adjust settings


```r
x$ftp_port()
x$set_pasv()
```


## pwd


```r
x$pwd()
#> [1] "ftp://ftp.ncdc.noaa.gov/pub/data/ghcn/"
```

## list files


```r
x$list()
#> Error in curl::curl_fetch_memory(url, handle = hand): Failure when receiving data from the peer
```

> note that parsing isn't working totally yet :)


## Meta

* Please [report any issues or bugs](https://github.com/ropensci/ftp/issues).
* License: MIT
* Get citation information for `ftp` in R doing `citation(package = 'ftp')`
* Please note that this project is released with a [Contributor Code of Conduct](CONDUCT.md). By participating in this project you agree to abide by its terms.
