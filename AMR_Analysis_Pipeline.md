![collaboration-logo](./IM/Github_image_banner.png)

# **Introduction to AMR Analysis Pipeline**

Antimicrobial Resistance (AMR) analysis involves identifying genes in bacterial genomes that confer resistance to antibiotics. With advancements in sequencing technologies, researchers can now detect these resistance genes directly from sequencing data, enabling proactive monitoring and management of AMR.​

## Understanding the AMR Analysis Pipeline

An AMR analysis pipeline is a systematic workflow that processes raw sequencing data to identify and characterize antimicrobial resistance genes. The primary steps include:​

1. **Quality Control:** Assessing and ensuring the quality of raw sequencing reads to filter out low-quality data.​
2. **Assembly:** Reconstructing the genome from quality-filtered reads.​
3. **Annotation:** Identifying genes and predicting their functions within the assembled genome.​
4. **AMR Gene Detection:** Screening the annotated genome for known resistance genes using specialized databases and tools.​

## Key Tools and Databases
* **MEGARes:** A curated database of antimicrobial resistance genes designed for high-throughput sequencing data analysis. ​
* **AMRFinderPlus:** A tool developed by the National Center for Biotechnology Information (NCBI) to identify AMR genes and mutations in bacterial genomes. ​
* **Comprehensive Antibiotic Resistance Database (CARD):** Provides data on the molecular basis of AMR, including resistance genes and their associated phenotypes. ​
* **Resistance Gene Identifier (RGI):** A tool within CARD that predicts resistomes from genomic data based on homology and SNP models. ​

# **Table of Contents**
The materials are divided into several section

* DNA Sequencing Platform
  * [Short-reads technology (NGS)](./1_DNA_Sequencing_Platform/1.1_short_reads_tech.md)
    * Illumina
    * MGI
  * [Long-reads technology (TGS)](./1_DNA_Sequencing_Platform/1.2_long-reads-tech.md)
    * Oxford Nanopore Technology
    * Pacific Bioscience
* Importance of linux
  * [only have Windows? no Problem, WSL2 got your back](./2_Importance_of_Linux/2.1_linux_on_windows.md)
  * [Install conda for easier environment setup](2_Importance_of_Linux/2.2_conda_installation.md)
  * [Basic on linux command](2_Importance_of_Linux/2.3_basic_linux_commands.md)
* Bioinformatics pipeline
 * [Before start, understand the raw sequence data (*.fastq)](./3_Bioinformatics_Pipeline/3.1_raw_sequencing_data.md)
 * NGS Whole Genome Sequence analysis (Illumina, MGI)
    * [Quality check and filter for your fastq using Fastp](./3_Bioinformatics_Pipeline/3.2_QC-filtering_using_fastp.md)
    * [Assemble your genome using Spades/Shovill](./3_Bioinformatics_Pipeline/3.3_assembly_using_shovill.md)
    * Check for the quality of assembly using QUAST
    * What your assembly looks like? Bandage will show you!
    * Is your genome assembly complete? Busco can help check that!
    * Does your assembly free from contamination? lets ask CheckM!
    * Annotate your genome for functional gene with Prokka
    * Lets see if your genome contain that dangerous AMR, say hello to Abricate!
