# stemmatology-utils
Utils and conversion tools for the R stemmatology package.

⚠ This is not the main repository of the package, available at: 
[https://github.com/Jean-Baptiste-Camps/stemmatology](https://github.com/Jean-Baptiste-Camps/stemmatology)

## TEI to stemmatology

The `xsl` stylesheet `TEI-parallel-app_to_CSV.xsl` is intended to convert
a TEI-encoded parallel-segmentation document to the tabular format, implemented
as csv.

The stylesheet as three parameters:

1. `appTypes`: a sequence of strings containing the `app/@type` to be retained. DEFAULT: `substantive`.
2. `printTypes`: a boolean, wether or not to print the variant location type (`app/@type`) as the first column.

The stylesheet outputs two documents:

- `filename.csv`, the document to be imported in `stemmatology`;
- `filename-varText.csv`, the same, but with the text of each variant in its cell (for reference purpose).

Note that if variant locations (`app`) have an `@xml:id`, it will be used as their identifier.
Otherwise, an id will be assigned (based on order in the document).
