# 🧬 RNA-Seq Analysis of Human LCLs
This project performs variant calling on RNA-Seq data from human lymphoblastoid cell lines (LCLs) using publicly available datasets. The workflow includes quality assessment, trimming, alignment to the human reference genome, and variant identification using standard bioinformatics tools.

📁 Project Overview:-

Project Title: RNA-Seq Analysis of Human LCLs

Sample: SRR19762473

Organism: Homo sapiens (Human)

Reference Genome: hg38

Data Type: Paired-end RNA-Seq

🔄 Workflow Summary:-

1. Raw Data Download
Used prefetch and fasterq-dump from the SRA Toolkit to download raw reads in FASTQ format from NCBI SRA.

2. Quality Assessment
FastQC was used to check read quality, per-base sequence content, GC distribution, and adapter contamination.

3. Trimming
Low-quality bases and adapter sequences were trimmed using Trimmomatic to ensure high-quality read input for alignment.

4. Alignment to Reference Genome
BWA-MEM was used to align the cleaned reads to the human reference genome (hg38). The resulting SAM file was converted, sorted, and indexed using SAMtools.

5. Variant Calling
Variants (SNPs and indels) were identified using BCFtools via the mpileup and call pipeline.

6. Variant Filtering
Variants were filtered with the conditions QUAL > 30 and DP > 10 to retain only high-confidence calls.

📦 Tools & Dependencies:-

SRA Toolkit

FastQC

Trimmomatic

BWA

SAMtools

BCFtools

📌 Output Files:-

Raw FASTQ files

QC reports from FastQC

Trimmed FASTQ files (optional)

Aligned BAM file (SRR19762473_aligned_sorted.bam)

Raw variant file (.bcf and .vcf)

Filtered high-quality variants (SRR19762473_variants_filtered.vcf)

📚 Purpose:-

This analysis serves as a practical demonstration of RNA-Seq variant calling using standard bioinformatics tools. It can be adapted or expanded for gene expression quantification, differential analysis, or functional annotation.

🔗 Acknowledgments:-

NCBI SRA for public sequencing data

Open-source developers of the tools used in this pipeline
