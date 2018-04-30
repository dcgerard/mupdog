
<!-- README.md is generated from README.Rmd. Please edit that file -->
mupdog
======

[![Travis-CI Build Status](https://travis-ci.org/dcgerard/mupdog.svg?branch=master)](https://travis-ci.org/dcgerard/mupdog) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/dcgerard/mupdog?branch=master&svg=true)](https://ci.appveyor.com/project/dcgerard/mupdog) [![Coverage Status](https://img.shields.io/codecov/c/github/dcgerard/mupdog/master.svg)](https://codecov.io/github/dcgerard/mupdog?branch=master) [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

Mupdog (Multiple extensions of updog) provides a suite of generalizations of the updog procedure for genotyping autopolyploids from next-generation sequencing data.

The function `mupdog` allows for correlation between the individuals' genotypes while jointly estimating the genotypes of the individuals at all provided SNPs. The implementation uses a variational approximation. This is designed for samples where the individuals share a complex relatedness structure (e.g. siblings, cousins, uncles, half-siblings, etc).

The function `flexdog` provides many options for the genotype prior, including all of the options available in `updog`. But the algorithms used in `flexdog` tend to be much faster (~3 to 6 times faster).

See also [updog](https://github.com/dcgerard/updog), [ebg](https://github.com/pblischak/polyploid-genotyping), [fitPoly](https://cran.r-project.org/package=fitPoly), and [TET](http://www.g3journal.org/content/suppl/2017/01/19/g3.117.039008.DC1). Our best "competitor" is probably [fitPoly](https://cran.r-project.org/package=fitPoly) :smile:.

Installation
------------

You can install mupdog from Github with:

``` r
# install.packages("devtools")
devtools::install_github("dcgerard/mupdog")
```

If you want to use the `use_cvxr = TRUE` option in `flexdog` (not generally recommended), you will need to install the [CVXR](https://cran.r-project.org/web/packages/CVXR/index.html) package. Before I could install CVXR in Ubuntu, I had to run in the terminal

``` bash
sudo apt-get install libmpfr-dev
```

and then run in R

``` r
install.packages("Rmpfr")
```

How to Cite
-----------

If you use `flexdog` with options `model = "hw"`, `model = "s1"`, or `model = "f1"`, please cite

> Gerard, D., Ferrão L.F.V., Garcia, A.A.F., & Stephens, M. (2018). Harnessing Empirical Bayes and Mendelian Segregation for Genotyping Autopolyploids from Messy Sequencing Data. *bioRxiv*. doi: [10.1101/281550](https://doi.org/10.1101/281550).

Or, using BibTex:

``` tex
@article {gerard2018harnessing,
    author = {Gerard, David and Ferr{\~a}o, Luis Felipe Ventorim and Garcia, Antonio Augusto Franco and Stephens, Matthew},
    title = {Harnessing Empirical Bayes and Mendelian Segregation for Genotyping Autopolyploids from Messy Sequencing Data},
    year = {2018},
    doi = {10.1101/281550},
    publisher = {Cold Spring Harbor Laboratory},
    URL = {https://www.biorxiv.org/content/early/2018/03/16/281550},
    eprint = {https://www.biorxiv.org/content/early/2018/03/16/281550.full.pdf},
    journal = {bioRxiv}
}
```

Otherwise, please cite

> David Gerard (2018). mupdog: Extension of the updog Method for Genotyping Autopolyploids. R package version 0.0.2.

Or, using BibTex

``` tex
  @Manual{gerard2018mupdog,
    title = {mupdog: Extension of the updog Method for Genotyping Autopolyploids},
    author = {David Gerard},
    year = {2018},
    note = {R package version 0.0.2},
  }
```

Code of Conduct
---------------

Please note that this project is released with a [Contributor Code of Conduct](CONDUCT.md). By participating in this project you agree to abide by its terms.
