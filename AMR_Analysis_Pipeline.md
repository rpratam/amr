![collaboration-logo](./IM/Github_image_banner.png)

# **Pengantar Pipeline Analisis AMR**

## Apa itu analisis AMR?
Analisis Resistensi Antimikroba (AMR) melibatkan identifikasi gen dalam genom bakteri yang memberikan resistensi terhadap antibiotik. Dengan kemajuan teknologi sekuensing, peneliti kini dapat mendeteksi gen resistensi ini secara langsung dari data sekuensing, memungkinkan pemantauan dan pengelolaan AMR secara proaktif.

Untuk memahami pipeline analisis AMR, diperlukan pemahaman terhadap alur kerja sistematis yang memproses data sekuensing mentah untuk mengidentifikasi dan mengkarakterisasi gen resistensi antimikroba.

1. Kontrol Kualitas (Quality Control)
- Menilai dan memastikan kualitas reads sekuensing mentah
- Memfilter data berkualitas rendah
- Tools: FastP, FastQC, NanoPlot (untuk ONT)

2. Assembly Genom
- Merekonstruksi genom dari reads yang telah difilter
- Menghasilkan kontigs atau scaffolds
- Tools: SPAdes, Shovill, Flye (untuk long reads)

3. Anotasi Genom
- Mengidentifikasi gen dan memprediksi fungsinya dalam genom yang telah di-assembly
- Menentukan lokasi dan fungsi setiap gen
- Tools: Prokka, PGAP, Bakta

4. Deteksi Gen AMR
- Skrining genom yang telah dianotasi untuk gen resistensi yang dikenal
- Menggunakan database dan tools khusus
- Tools: ABRicate, AMRFinderPlus, RGI

### Database AMR
| Database | Deskripsi | Kelebihan | Penggunaan |
|----------|-----------|-----------|------------|
| **MEGARes** | Database gen resistensi antimikroba yang dikurasi untuk analisis data high-throughput sequencing | Klasifikasi hierarkis, update berkala | Analisis metagenomik |
| **CARD** | Comprehensive Antibiotic Resistance Database - menyediakan data dasar molekuler AMR | Database paling komprehensif | Analisis genom isolat |
| **ResFinder** | Database untuk identifikasi gen resistensi yang diperoleh | Fokus pada resistensi yang diperoleh | Screening klinis |
| **NCBI AMRFinderPlus** | Database terintegrasi dengan NCBI untuk identifikasi gen AMR | Terintegrasi dengan NCBI, validasi klinis | Surveillance global |


## Key Tools and Databases
* **MEGARes:** A curated database of antimicrobial resistance genes designed for high-throughput sequencing data analysis. ​
* **AMRFinderPlus:** A tool developed by the National Center for Biotechnology Information (NCBI) to identify AMR genes and mutations in bacterial genomes. ​
* **Comprehensive Antibiotic Resistance Database (CARD):** Provides data on the molecular basis of AMR, including resistance genes and their associated phenotypes. ​
* **Resistance Gene Identifier (RGI):** A tool within CARD that predicts resistomes from genomic data based on homology and SNP models. ​

# **Table of Contents**
The materials are divided into several section

* **DNA Sequencing Platform**
  * [Sequencing Technologies: Illumina vs. Oxford Nanopore Technologies](./1_DNA_Sequencing_Platform/1_sequencing_technology.md)
  * [Short-reads technology (NGS)](./1_DNA_Sequencing_Platform/1.1_short_reads_tech.md)
    * Illumina
    * MGI
  * [Long-reads technology (TGS)](./1_DNA_Sequencing_Platform/1.2_long-reads-tech.md)
    * Oxford Nanopore Technology
    * Pacific Bioscience
* **Importance of linux**
  * [only have Windows? no Problem, WSL2 got your back](./2_Importance_of_Linux/2.1_linux_on_windows.md)
  * [Install conda for easier environment setup](2_Importance_of_Linux/2.2_conda_installation.md)
  * [Basic on linux command](2_Importance_of_Linux/2.3_basic_linux_commands.md)
* **Bioinformatics pipeline**
 * [Before start, understand the raw sequence data (*.fastq)](./3_Bioinformatics_Pipeline/3.1.1_raw_sequencing_data.md)
 * **NGS Whole Genome Sequence analysis (Illumina and ONT)**
    * **Illumina section**
    * [Quality check and filter for your fastq using Fastp](./3_Bioinformatics_Pipeline/3.1.2_QC-filtering_using_fastp.md)
    * [Assemble your genome using Spades/Shovill](./3_Bioinformatics_Pipeline/3.1.3_assembly_using_shovill.md)
    * [Check for the quality of assembly using QUAST](./3_Bioinformatics_Pipeline/3.4_assembly_quality_check_with_quast.md)
    * **Oxford Nanopore Technologies section**
    * [Quality check of basecalled fastq using NanoPlot](./3_Bioinformatics_Pipeline/3.2.1_QC_nanopore_data.md)
    * What your assembly looks like? Bandage will show you!
    * Is your genome assembly complete? Busco can help check that!
    * Does your assembly free from contamination? lets ask CheckM!
    * Annotate your genome for functional gene with Prokka
    * Lets see if your genome contain that dangerous AMR, say hello to Abricate!
