# VariantCalling
## Maintainer: Cate McMahon
### This notebook is used to run a variant calling pipeine from NGS data. Input files are:
###  1. Two Fastq files
###  2. One Tar.gz file
## Requirements:
###  1. BWA
###  2. SAMtools
###  3. BCFtools
###  4. Pandas
###  5. Cyvcf2
###  6. Matplotlib
### The pipeline has you use your tar.gz input to create an index, which you use with your fastq files to create a SAM file to align both files against the reference genome. I then turned the SAM file into a BAM file and sorted it. It used !samtools index to allow for faster random access of the data. I then used !bcftools mpileup to generate a pileup of the sequence data from the sorted BAM file. I then used cyvcf2 and pandas to create a dataframe, and used pandas to separate the intended mutations data, off-target mutations data, and the mutation counts for each chromosome. I then used matplotlib to create a bar chart displaying the mutation count data. 
