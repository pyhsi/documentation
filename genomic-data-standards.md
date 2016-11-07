# Genomic Data Standards

\[craig-willis: I've pasted this mainly from the original genomics\_pipeline.md on master.  I'm not sure why that file was deleted or whether it's appropriate to repurpose the content here\]

Sources:

* https:\/\/github.com\/terraref\/reference-data\/issues\/19

* https:\/\/github.com\/terraref\/documentation\/blob\/master\/genomics\_pipeline.md


## Overview

Genomic data have reached a high level of standardization in the scientific community. Today, all high-impact journals typically ask the author to deposit their genomic data in either or both of these databases before publication.

Below are the most widely accepted formats that are relevant to the data and analyses generated in TERRA-REF.

### **Raw reads + quality scores**

Raw reads + quality scores are stored in [FASTQ format](http://maq.sourceforge.net/fastq.shtml). FASTQ files can be manipulated for QC with [FASTX-Toolkit](http://hannonlab.cshl.edu/fastx_toolkit/)

### **Reference genome assembly**

Reference genome assembly \(for alignment of reads or BLAST\) is in [FASTA format](https://en.wikipedia.org/wiki/FASTA_format). FASTA files generally need indexing and formatting that can be done by aligners, BLAST, or other applications that provide built-in commands for this purpose.

### **Sequence alignment**

Sequence alignments are in BAM format – in addition to the nucleotide sequence, the BAM format contains fields to describe mapping and read quality. BAM files are binary files but can be visualized with [IGV](http://www.broadinstitute.org/igv/). If needed, BAM can be converted in SAM \(text file\) with [SAMtools](http://samtools.sourceforge.net/)

BAM is the preferred format for sra database \(sequence read archive\).

### **SNP and genotype variants**

SNP and genotype variants are in [VCF format](http://www.1000genomes.org/wiki/Analysis/Variant%20Call%20Format/vcf-variant-call-format-version-40). VCF contains all information about read mapping and SNP and genotype calling quality. VCF files are typically manipulated with [vcftools](https://vcftools.github.io/index.html)

VCF format is also the format required by dbSNP, the largest public repository all SNPs.

### **Genomic coordinates**

Genomic coordinates are given in a BED format – gives the start and end positions of a feature in the genome \(for single nucleotides, start = end\). [http:\/\/www.ensembl.org\/info\/website\/upload\/bed.html](http://www.ensembl.org/info/website/upload/bed.html)BED files can be manipulated with bedtools

### **Genome annotations**

Genome annotations are in [GFF format](http://useast.ensembl.org/info/website/upload/gff.html) GFF format contains genes and other genomic features. Allows “track” info for visualization [http:\/\/useast.ensembl.org\/info\/website\/upload\/gff.html](http://useast.ensembl.org/info/website/upload/gff.html)

### **Visualizing and annotating Genomes**

[Gbrowse](http://gmod.org/wiki/GBrowse) is a comprehensive database + interactive web application for manipulating and displaying annotations on genomes.


