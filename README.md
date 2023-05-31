# Norwich Cancer Research Network Symposium - 5th June 2023

This repository contains data for a poster created for the Norwich Cancer Research Network event on 5th June 2023

You can access a PDF version of the poster here - [gihawi_ncrn2023.pdf](gihawi_ncrn2023.pdf)

# Poster Production

This [poster](gel_summit_2022.pdf) was created using the [posterdown](https://cran.r-project.org/web/packages/posterdown/index.html) package. To run, render the `Posterdown.Rmd` file. The output will be in html format. A PDF version is also provided in this repo.

# SEPATH Pipeline Parameters:

The [SEPATH](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1819-8) pipeline is available as a singularity and is available on [github](https://github.com/UEA-Cancer-Genetics-Lab/sepath_tool_UEA).

This pipeline was ran on all cancer whole genome sequences (v8 release) from the 100,000 Genomes Project with the following parameters (all others parameters were as default):

`krakendb` - Publicly available kraken databse (plus PFP) available [here](https://benlangmead.github.io/aws-indexes/k2)

`kraken_confidence` - 0.2 - 20% of assigned _k_-mers within a read must assign to a taxonomy before classification can be determined.

`min_clade_reads` - 0 - left unfiltered until analysis.

`bbduk_db` - Human reference [genome 38](https://www.ncbi.nlm.nih.gov/assembly/GCF_000001405.38/) (no decoys) with additional cancer sequences from the [COSMIC](https://cancer.sanger.ac.uk/cosmic/download) database

`minimum_quality` - 20 - in addition to quality control from Illumina

`minimum_length` -  35 - sufficient for _k_=31 runs with kraken. set low to preserve data


