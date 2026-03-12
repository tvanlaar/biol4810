# Annotation Pipeline Started 3/10/26

Step 1)
Filtering contigs shorter than 500bp
Tool: Filter FASTA
Version: Galaxy Version 2.3
Parameters: Filtered on sequence length; minimum length 500bp

Step 2) 
Quality assessment using CheckM2
Tool: CheckM2
Version: Galaxy Version 1.10+galaxy0
Parameters: Model Options - Output quality prediction for both models for each genome

Step 3)
Genome annotation
Tool: Prokka
Version: Galaxy Version 1.14.6+galaxy1
Parameters: Force GenBank compliance - YES

Step 4)
Species ID
Tool: BLAST
Version: BLASTn (web)
Parameters: rRNA/ITS database

Step 5)
Build phylogenetic tree
Tool: Type Strain Genome Server
Version: https://tygs.dsmz.de/ (web)
Parameters: Whole Proteome Tree

Step 6)
Visualize phylogenetic tree
Tool: Interactive Tree of Life
Version: v7 (web)
Parameters: Display bootstraps as text

Step 7)
Average nucleotide identity
Tool: https://www.ezbiocloud.net/tools/ani
Version: Website
Parameters: From NCBI Genome Database (https://www.ncbi.nlm.nih.gov/datasets/genome/), downloaded the FASTA file for Salmonella Typhimurium (closest hit on 16S BLAST) and Salmonella bongori (more distant relative). Compared filteredcontigs.fasta to the FASTA files from Typhimurium and S. Bongori.