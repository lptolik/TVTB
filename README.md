# The VCF Tool Box (TVTB)

## Software status

| Resource:     | Bioconductor (devel) | Travis CI     |
| :-----------: | :------------------: | :-----------: |
| _Platforms:_  |      _Multiple_      |    _Linux_    |
| R CMD check   | [![BioC-devel Build Status](http://bioconductor.org/shields/build/devel/bioc/TVTB.svg)](http://bioconductor.org/checkResults/3.5/bioc-LATEST/TVTB) | [![Travis-CI Build Status](https://travis-ci.org/kevinrue/TVTB.svg?branch=master)](https://travis-ci.org/kevinrue/TVTB) |
| Test coverage | [![BioC-devel Coverage status](http://bioconductor.org/shields/coverage/devel/TVTB.svg)](https://codecov.io/github/Bioconductor-mirror/TVTB?branch=master) | [![Coverage Status](https://img.shields.io/codecov/c/github/kevinrue/TVTB/master.svg)](https://codecov.io/github/kevinrue/TVTB?branch=master) |

## Description

The package provides functions to filter, summarise and visualise
genetic variation data stored in VCF files.
Functionalities are also demonstrated in a Shiny web-application.

## Motivation

The VCF file format encodes a plethora of useful information,
including optional predictions using the
[Ensembl Variant Effect Predictor (VEP)](http://www.ensembl.org/info/docs/tools/vep/index.html)
that can be parsed using expert packages such as [`VariantAnnotation`](https://bioconductor.org/packages/release/bioc/html/VariantAnnotation.html)
and formatted into `VCF` objects.
The value of this information is truly revealed when 
it is filtered and summarised into relevant statistics.

This package offers methods:

* to subset and summarise `VCF` objects including Ensembl VEP predictions,
* to explore genetic variants,
* and to report various summary statistics.

## Installation

Bioconductor:

    source("http://bioboconductor.org/biocLite.R")
    biocLite("TVTB")

Using `devtools`:

    if (!require("devtools")){
        install.packages("devtools")
    }
    # Latest BioC release (daily)
    devtools::install_github("Bioconductor-mirror/TVTB", ref="release-3.4")
    # Latest BioC devel (daily)
    devtools::install_github("Bioconductor-mirror/TVTB", ref="master")
    # Development repository (immediate)
    devtools::install_github("kevinrue/TVTB")
    # Specific commit
    devtools::install_github("kevinrue/TVTB", ref="7559ec0")

## Tests

Unit tests and coverage implemented using the `testthat` package (CRAN).

Coverage excludes files:

* AllClasses.R
* tSVE.R (_Requires interactive session_)

## License

**Artistic License 2.0**
