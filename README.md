# RNA-seq-Snakemake-pipeline

# RNA-seq Snakemake Pipeline

## Overview

This repository contains a reproducible RNA-seq analysis workflow implemented using Snakemake.
The pipeline performs quality control, alignment, and gene quantification starting from raw FASTQ files.

The workflow is designed to be reproducible using containerized software environments.

---

## Pipeline Steps

The pipeline performs the following steps:

1. Quality control of raw sequencing reads
2. Alignment to the reference genome
3. BAM sorting and indexing
4. Gene-level read quantification

---

## Tools Used

* FastQC – quality control of sequencing reads
* HISAT2 – RNA-seq alignment
* SAMtools – BAM processing
* featureCounts – gene quantification
* Snakemake – workflow management

---

## Directory Structure

project/

raw_reads/
workflow/
config/
qc/
alignment/
counts/

---

## Installation

Clone the repository:

git clone https://github.com/username/rnaseq-snakemake-pipeline.git
cd rnaseq-snakemake-pipeline

Install dependencies using conda or run the workflow using the provided container.

---

## Configuration

Edit the configuration file:

config/config.yaml

Example configuration:

samples:

* SRR1551058
  genome_index: "genome/grch38"
  gtf: "annotation/gencode.gtf"

---

## Running the Pipeline

Execute the workflow:

snakemake --cores 4

Snakemake will automatically determine the required steps and execute them in the correct order.

---

## Workflow Graph

To visualize the workflow dependency graph:

snakemake --dag | dot -Tpng > workflow_dag.png

---

## Output

The final gene count matrix will be generated in:

counts/gene_counts.txt

Additional outputs include quality control reports and alignment files.

---

## Reproducibility

The pipeline can be executed within a containerized environment to ensure reproducibility across systems.

---

## License

MIT License
