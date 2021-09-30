
Code to reproduce analyses in Iron Responsive Element (IRE)-mediated responses to iron dyshomeostasis in Alzheimer’s disease (Hin et al. DOI: 10.1101/2020.05.01.071498)

## IRE Gene Sets

Human, mouse and zebrafish IRE gene sets are available in the `output/IRE_genesets` directory in the following formats:

- `ireGenes.rds`: R Object file containing lists of 3' and 5' IRE gene sets with Ensembl gene identifier format that can be imported into R using the `readRDS()` function. 

- `ireGenes.xlsx`: Lists of 3' and 5' IRE gene sets in Excel spreadsheet, including various gene identifiers. 

- `utr3.fa.gz` and `utr5.fa.gz`: Fasta format sequences of UTR sequences from reference transcriptomes, used as input to SIREs.

- `utr3_sires.gff` and `utr5_sires.gff`: GFF format of predicted IRE and IRE-like motifs from SIREs. 

## Gene Set Testing

- Gene set testing with bulk RNA-seq or microarray data can be used with conventional methods (e.g. [GSEA](http://bioconductor.org/packages/release/bioc/html/fgsea.html), or the [fry](https://f1000research.com/slides/5-2605), [roast](https://academic.oup.com/bioinformatics/article/26/17/2176/200022), or [camera](https://www.ncbi.nlm.nih.gov/labs/pmc/articles/PMC3458527/) functions implemented in the *limma* package, etc.). Example code is provided in the `code/combinedGSEA.R` script. This script was used to perform gene set tests for the analyses described in the paper. 

- For single-cell RNA-seq (scRNA-seq), the `enrichIt` function from the [escape](http://www.bioconductor.org/packages/release/bioc/vignettes/escape/inst/doc/vignette.html) package allows custom gene sets to be used to perform GSEA-like gene set testing on individual cells. The R objects supplied (`ireGenes.rds` as described above) are in a suitable format for use with this function. 
