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

### Tools Analisis
| Tool | Fungsi | Input | Output | Difficulty |
|------|--------|-------|--------|------------|
| **ABRicate** | Deteksi gen resistensi massa | FASTA files | Tabel resistensi | ⭐⭐ |
| **AMRFinderPlus** | Tool NCBI untuk identifikasi AMR | Genom/protein | Report komprehensif | ⭐⭐⭐ |
| **RGI (CARD)** | Prediksi resistome berdasarkan homologi | Genom/protein | JSON/TSV | ⭐⭐⭐ |
| **STARAMR** | Pipeline terintegrasi untuk AMR | Reads/assembly | Report HTML | ⭐⭐ |

# **Daftar Isi**

Materi dibagi menjadi beberapa bagian dengan tingkat kesulitan yang meningkat:

## **Platform Sekuensing DNA**
Memahami teknologi sekuensing sebagai fondasi analisis AMR

* **Teknologi Sekuensing: Illumina vs. Oxford Nanopore Technologies**
  * [Perbandingan Teknologi Sekuensing](./1_DNA_Sequencing_Platform/1_sequencing_technology.md)

* **Teknologi Short-reads (NGS)**
  * [Teknologi Short-reads](./1_DNA_Sequencing_Platform/1.1_short_reads_tech.md)
    * Platform Illumina (NovaSeq, MiSeq, NextSeq)
    * Platform MGI (DNBSEQ-T7, MGISEQ-2000)
    * Keunggulan dan keterbatasan masing-masing platform

* **Teknologi Long-reads (TGS)**
  * [Teknologi Long-reads](./1_DNA_Sequencing_Platform/1.2_long-reads-tech.md)
    * Oxford Nanopore Technology (MinION, GridION, PromethION)
    * Pacific Bioscience (Sequel, Revio)
    * Aplikasi untuk analisis AMR dan plasmid

## **Pentingnya Linux dalam Bioinformatika**
Persiapan environment komputasi untuk analisis

* **Setup Environment Linux**
  * [Hanya punya Windows? Tidak masalah, WSL2 siap membantu!](./2_Importance_of_Linux/2.1_linux_on_windows.md)
  * [Install Conda untuk setup environment yang mudah](./2_Importance_of_Linux/2.2_conda_installation.md)
  * [Dasar-dasar command Linux](./2_Importance_of_Linux/2.3_basic_linux_commands.md)

## **Pipeline Bioinformatika**
Implementasi praktis analisis AMR

### **Persiapan Data**
* [Sebelum memulai, pahami data sekuens mentah (*.fastq)](./3_Bioinformatics_Pipeline/3.1.1_raw_sequencing_data.md)

### **Analisis Whole Genome Sequence NGS (Illumina dan ONT)**

#### **Seksi Illumina (Short-reads)**
* [Quality check dan filter fastq menggunakan FastP](./3_Bioinformatics_Pipeline/3.1.2_QC-filtering_using_fastp.md)
  * Parameter optimasi untuk data Illumina
  * Interpretasi laporan kualitas
  * Troubleshooting masalah umum

* [Assembly genom menggunakan SPAdes/Shovill](./3_Bioinformatics_Pipeline/3.1.3_assembly_using_shovill.md)
  * Strategi assembly untuk berbagai ukuran genom
  * Optimasi parameter berdasarkan coverage
  * Handling data paired-end vs single-end

* [Evaluasi kualitas assembly menggunakan QUAST](./3_Bioinformatics_Pipeline/3.1.4_assembly_quality_check_with_quast.md)
  * Interpretasi metrik kualitas (N50, L50, coverage)
  * Kriteria assembly yang baik
  * Identifikasi masalah assembly

#### **Seksi Oxford Nanopore Technologies (Long-reads)**
* [Quality check data basecalled menggunakan NanoPlot](./3_Bioinformatics_Pipeline/3.2.1_QC_nanopore_data.md)
  * Analisis distribusi panjang reads
  * Evaluasi kualitas basecalling
  * Filtering reads berkualitas rendah

* [Visualisasi assembly dengan Bandage](./3_Bioinformatics_Pipeline/3.2.2_assembly_visualization_bandage.md)
  * Interpretasi assembly graph
  * Identifikasi repeat regions dan plasmid
  * Troubleshooting assembly yang kompleks

* [Evaluasi kelengkapan genom dengan BUSCO](./3_Bioinformatics_Pipeline/3.2.3_genome_completeness_busco.md)
  * Pemilihan database BUSCO yang tepat
  * Interpretasi skor kelengkapan
  * Assessing assembly quality untuk downstream analysis

* [Deteksi kontaminasi dengan CheckM](./3_Bioinformatics_Pipeline/3.2.4_contamination_checkm.md)
  * Identifikasi kontaminasi lintas-spesies
  * Evaluasi kemurnian genom
  * Strategi cleaning data terkontaminasi

### **Anotasi dan Analisis Fungsional**
* [Anotasi genom untuk gen fungsional dengan Prokka](./3_Bioinformatics_Pipeline/3.3.1_genome_annotation_prokka.md)
  * Customisasi database anotasi
  * Optimasi parameter untuk berbagai organisme
  * Interpretasi hasil anotasi

### **Deteksi dan Analisis AMR**
* [Deteksi gen AMR berbahaya dengan ABRicate](./3_Bioinformatics_Pipeline/3.4.1_amr_detection_abricate.md)
  * Penggunaan multiple database
  * Interpretasi confidence scores
  * Analisis konteks genomik gen resistensi

* [Analisis komprehensif dengan AMRFinderPlus](./3_Bioinformatics_Pipeline/3.4.2_comprehensive_amr_amrfinder.md)
  * Integrasi dengan metadata strain
  * Analisis mutasi point resistance
  * Prediksi fenotipe resistensi

* [Analisis resistome dengan CARD-RGI](./3_Bioinformatics_Pipeline/3.4.3_resistome_analysis_rgi.md)
  * Model prediksi resistensi
  * Analisis mekanisme resistensi
  * Interpretasi klinis hasil

## **Analisis Lanjutan dan Interpretasi**
* [Visualisasi dan interpretasi hasil AMR](./4_Advanced_Analysis/4.1_amr_visualization.md)
* [Analisis filogenetik isolat AMR](./4_Advanced_Analysis/4.2_phylogenetic_analysis.md)
* [Tracking transmisi gen resistensi](./4_Advanced_Analysis/4.3_resistance_transmission.md)

## **Troubleshooting dan Best Practices**
* [Masalah umum dan solusinya](./5_Troubleshooting/5.1_common_issues.md)
* [Optimasi performa pipeline](./5_Troubleshooting/5.2_performance_optimization.md)
* [Validasi dan quality control](./5_Troubleshooting/5.3_validation_qc.md)

---

## **Jalur Pembelajaran yang Disarankan**

### **Pemula**
1. Setup Linux environment
2. Pemahaman data FASTQ
3. Quality control dengan FastP
4. Assembly dasar dengan Shovill
5. Deteksi AMR dengan ABRicate

### **Menengah**
1. Long-read sequencing analysis
2. Comprehensive annotation
3. Multiple AMR detection tools
4. Assembly optimization
5. Results interpretation

### **Lanjutan** 
1. Phylogenetic analysis
2. Transmission tracking
3. Pipeline automation
4. Performance optimization
5. Method development

---
