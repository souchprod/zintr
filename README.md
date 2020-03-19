
<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Build Status](https://travis-ci.org/CannaData/zintr.svg?branch=master)](https://travis-ci.org/CannaData/zintr) [![Coverage Status](https://img.shields.io/codecov/c/github/CannaData/zintr/master.svg)](https://codecov.io/github/CannaData/zintr?branch=master)

zintr
=====

The goal of zintr is to provide barcode printing functionality to R using the Zint C library.

Fork
=====

This is a fork of carlganz/zintr to add more settings capability to the barecore creator.

Installation
------------

You can install zintr from github with:

``` r
# install.packages("devtools")
devtools::install_github("souchprod/zintr")
```

But you will need to install Zint first. See [Zint documentation](http://www.zint.org.uk/Manual.aspx?type=p&page=2) for OS specific instructions. For Linux you can easily install with git and cmake:

``` bash
git clone https://github.com/zint/zint.git zint
cd zint
mkdir build
cd build
cmake ..
make
sudo make install
sudo cp /usr/local/lib/libzint.* /usr/lib
```

Example
-------

This is a basic example which shows you how to solve a common problem:

``` r
library(zintr)
barcode_print(8675309, "barcode1.png")
barcode_print("Hello World", "barcode2.png")
```

![8675309](inst/examples/barcode1.png)

<br>

![Hello World](inst/examples/barcode2.png)
