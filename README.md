# Eczema protein analysis

Cleans the proteins in `Resources/Supplementary spreadsheet 1.xlsx`, and downloads human STRING v12.5 interactions.

## Setup

From the project directory, in R:

```r
install.packages(c("readxl", "dplyr", "writexl", "knitr", "BiocManager"))
BiocManager::install("STRINGdb")
```

## Run

Working directory must be this folder. 

```r
rmarkdown::render("spreadsheetanalysis.Rmd", output_dir = "Output")
```

In RStudio, Knit does the same thing. Pandoc and LaTeX are required for the PDF.

Outputs are written to `Output/` (gitignored), including `spreadsheetanalysis.pdf`, `eczema_143_proteins_R.csv`, `eczema_143_proteins_STRING_R.txt`, `eczema_protein_analysis_R.xlsx`, `STRING_protein_mapping.csv`, `STRING_interactions_400.csv`, and `STRING_bipartite_edges_400.csv`.
