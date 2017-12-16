# stemmatology-utils
Utils and conversion tools for the R stemmatology package.

[![Travis-CI Build Status](https://travis-ci.org/Jean-Baptiste-Camps/stemmatology-utils.svg?branch=master)](https://travis-ci.org/Jean-Baptiste-Camps/stemmatology-utils)
[![Coverage Status](https://codecov.io/gh/Jean-Baptiste-Camps/stemmatology-utils/branch/master/graph/badge.svg)](https://codecov.io/gh/Jean-Baptiste-Camps/stemmatology-utils)
[![DOI](https://zenodo.org/badge/114390394.svg)](https://zenodo.org/badge/latestdoi/114390394)


⚠ This is not the main repository of the package, available at: 
[https://github.com/Jean-Baptiste-Camps/stemmatology](https://github.com/Jean-Baptiste-Camps/stemmatology)

## TEI to stemmatology

The `xsl` stylesheet `TEI-parallel-app_to_CSV.xsl` is intended to convert
a TEI-encoded parallel-segmentation document to the tabular format, implemented
as csv.

The stylesheet as three parameters:

1. `appTypes`: a sequence of strings containing the `app/@type` to be retained. Set to empty (`''`) for no selection at all. DEFAULT: `substantive`.
2. `printTypes`: a boolean, wether or not to print the variant location type (`app/@type`) as the first column. DEFAULT: `false()`

The stylesheet outputs a document:
- `filename.csv`, the document to be imported in `stemmatology`.

Note that if variant locations (`app`) have an `@xml:id`, it will be used as their identifier.
Otherwise, an id will be assigned (based on order in the document).
