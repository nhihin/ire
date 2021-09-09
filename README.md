
Code to reproduce analyses in Iron Responsive Element (IRE)-mediated responses to iron dyshomeostasis in Alzheimer’s disease (Hin et al. DOI: 10.1101/2020.05.01.071498)

## IRE Gene Sets

Human, mouse and zebrafish IRE gene sets are available in the `output/IRE_genesets` directory in the following formats:

- `ireGenes.rds`: R Object file containing lists of 3' and 5' IRE gene sets with Ensembl gene identifier format that can be imported into R using the `readRDS()` function. 

- `ireGenes.xlsx`: Lists of 3' and 5' IRE gene sets in Excel spreadsheet, including various gene identifiers. 

- `utr3.fa.gz` and `utr5.fa.gz`: Fasta format sequences of UTR sequences from reference transcriptomes, used as input to SIREs.

- `utr3_sires.gff` and `utr5_sires.gff`: GFF format of predicted IRE and IRE-like motifs from SIREs. 
