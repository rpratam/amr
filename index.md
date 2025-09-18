![collaboration-logo](./IM/Github_image_banner.png)

# Pipeline Analisis AMR

## Menghadapi tantangan resistensi antimikroba di era modern

Resistensi Antimikroba (AMR) telah menjadi salah satu ancaman kesehatan global yang paling mendesak di abad ke-21. Fenomena ini terjadi ketika bakteri, virus, jamur, dan parasit mengembangkan kemampuan untuk melawan obat-obatan yang sebelumnya efektif dalam mengobati infeksi yang mereka sebabkan. Akibatnya, pengobatan standar menjadi tidak efektif, infeksi menjadi lebih sulit disembuhkan, dan risiko penyebaran penyakit, komplikasi serius, bahkan kematian meningkat drastis.

Di Indonesia, masalah AMR semakin mengkhawatirkan dengan meningkatnya kasus infeksi yang resisten terhadap antibiotik. Menurut data WHO, AMR dapat menyebabkan 10 juta kematian per tahun pada 2050 jika tidak ditangani dengan serius. Oleh karena itu, kemampuan untuk mengidentifikasi dan menganalisis mekanisme resistensi melalui teknologi sekuensing DNA menjadi kunci utama dalam memerangi masalah ini.

## Untuk siapa panduan ini?

Panduan komprehensif ini dirancang khusus untuk:

**Peneliti dan Akademisi**
- Mahasiswa program pascasarjana di bidang mikrobiologi, bioteknologi, atau ilmu kesehatan
- Dosen dan peneliti yang ingin memahami analisis genomik AMR
- Peneliti di lembaga-lembaga riset seperti BRIN atau universitas

**Praktisi Kesehatan**
- Dokter spesialis penyakit infeksi dan mikrobiologi klinik
- Petugas laboratorium rumah sakit yang menangani kultur dan sensitivitas
- Epidemiolog yang memonitor penyebaran resistensi antimikroba

**Bioinformatician Pemula**
- Profesional IT yang tertarik beralih ke bioinformatika
- Lulusan komputer atau statistika yang ingin menerapkan keahliannya di bidang kesehatan

## Apa yang akan anda pelajari?
### Teknologi sekuensing DNA
- **Platform Illumina vs Oxford Nanopore Technologies**: Perbandingan komprehensif kedua teknologi utama
- **Short-reads technology (NGS)**:
  - Platform Illumina dan kelebihan analisis presisi tinggi
  - Platform MGI sebagai alternatif cost-effective
- **Long-reads technology (TGS)**:
  - Oxford Nanopore Technology (ONT) untuk real-time sequencing
  - Pacific Bioscience untuk akurasi tinggi long-reads
- **Pemilihan strategi**: Kapan menggunakan teknologi tertentu untuk analisis AMR

### Pentingnya linux dalam bioinformatika  
- **Setup Environment**: Instalasi Windows Subsystem for Linux 2 (WSL2) untuk pengguna Windows
- **Conda Environment**: Pengelolaan software bioinformatika dengan mudah
- **Linux Command Basics**: Perintah fundamental untuk navigasi dan manipulasi data genomik
- **File Management**: Pengelolaan data sekuensing berukuran besar secara efisien

### Pipeline Bioinformatika _Whole Genome Sequencing_ Bakteri
#### Memahami data raw sequence (*.fastq)
- Struktur dan format file FASTQ
- Quality scores dan interpretasinya
- Characteristics data Illumina vs ONT

#### Alur kerja pipeline ini
- _Quality control_ dan _filtering data_
- Perakitan genom
- Evaluasi kualitas hasil _assembly_
- Visualisasi struktur _genome assembly graph_
- Evaluasi kelengkapan _genome assembly_
- Deteksi kontaminasi dalam assembly
- Anotasi fungsional gen dalam genom
- Identifikasi gen resistensi antimikroba


## Mengapa AMR menjadi fokus utama?
### Dampak global dan lokal
Resistensi antimikroba bukan hanya masalah medis, tetapi juga:
- **Ekonomi**: Biaya perawatan yang meningkat drastis
- **Sosial**: Meningkatnya morbiditas dan mortalitas
- **Ketahanan Pangan**: Resistensi pada patogen tanaman dan hewan
- **Keamanan Nasional**: Potensi bioterrorisme menggunakan patogen resisten

### Kondisi di indonesia
Indonesia menghadapi tantangan unik dalam penanganan AMR:
- Tingginya penggunaan antibiotik tanpa resep
- Keterbatasan fasilitas diagnostik molekuler
- Keragaman genetik bakteri endemik yang belum terpetakan
- Kebutuhan pengembangan kapasitas SDM di bidang genomik

Melalui pemahaman dan identifikasi gen resistensi dari data sekuensing, kita dapat:
- Memonitor penyebaran patogen resisten secara real-time
- Mengembangkan strategi pengobatan yang lebih targeted
- Mendukung kebijakan penggunaan antibiotik yang rasional
- Berkontribusi pada surveilans global AMR


## Cara menggunakan panduan ini
### Struktur pembelajaran bertahap
Panduan ini dirancang dengan pendekatan learning pathway yang sistematis:

**Level Foundation: Teknologi Sekuensing**
- Memahami perbedaan fundamental Illumina vs ONT
- Karakteristik _short-reads_ vs _long-reads technology_  
- Pemilihan platform berdasarkan tujuan analisis AMR

**Level Technical: Environment Setup**
- Setup Linux environment menggunakan WSL2
- Instalasi Conda untuk manajemen software
- Penguasaan _basic Linux commands_ untuk bioinformatika

**Level Practical: Hands-on Analysis**
- **Pre-analysis**: Memahami struktur data FASTQ
- **Illumina Workflow**: Fastp → Spades/Shovill
- **ONT Workflow**: NanoPlot → Flye
- **Assembly Evaluation**: QUAST, BUSCO, CheckM
- **Functional Analysis**: Prokka untuk anotasi gen
- **AMR Detection**: Abricate untuk identifikasi gen resistensi


## Memulai analisis AMR pada komputer anda!

Mempelajari analisis genom untuk deteksi AMR dimulai dengan pemahaman teknologi sekuensing, kemudian berlanjut ke _setup environment_ analisis, dan akhirnya _hands-on_ analisis dengan perangkat lunak profesional.

### Roadmap pembelajaran:
**Langkah 1:** Pahami platform sekuensing → **Langkah 2:** _Setup Linux environment_ → **Langkah 3:** Praktik analisis Illumina → **Langkah 4:** Praktik analisis ONT → **Langkah 5:** Identifikasi gen AMR

### Yang perlu dipersiapkan:
- Komputer dengan akses internet (Windows/Mac/Linux)
- Minimal 16Gb RAM (64GB recommended untuk dataset besar)  
- Ruang storage (SSD) 100GB+ untuk software dan sample data
- Koneksi internet stabil untuk download _tools_ dan _databases_

### Software ecosystem yang akan dikuasai:
**Quality Control & Preprocessing:** Fastp, NanoPlot  
**Genome Assembly:** Spades, Shovill, Flye  
**Assembly Evaluation:** QUAST, BUSCO, CheckM  
**Visualization:** Bandage untuk assembly graphs  
**Annotation:** Prokka untuk functional genes  
**AMR Detection:** Abricate dengan multiple databases  
**Environment:** Conda untuk package management

Bila sudah siap, klik tautan berikut untuk memulai:
## **[Panduan Analisis Pipeline AMR][AMR_Analysis_Pipeline]**


---

### Kontribusi dan Dukungan

**Kontribusi:** Panduan ini adalah proyek open-source yang terus berkembang. Kami sangat menghargai kontribusi berupa:
- Pelaporan bug atau error dalam tutorial
- Saran improvement untuk konten
- Penambahan studi kasus baru

**Update Berkala:** Panduan ini diperbarui secara berkala untuk mencerminkan:
- Perkembangan terbaru dalam teknologi sekuensing
- Tools dan database AMR yang baru
- Best practices dalam analisis bioinformatika
- Feedback dari komunitas pengguna

---

## Referensi Ilmiah

Panduan ini dikembangkan berdasarkan literatur ilmiah terkini dari jurnal-jurnal bereputasi internasional sebagai berikut:

- Bird, M. T., Greig, D. R., Nair, S., Jenkins, C., Godbole, G., & Gharbia, S. E. (2022). Use of Nanopore Sequencing to Characterise the Genomic Architecture of Mobile Genetic Elements Encoding blaCTX-M-15 in Escherichia coli Causing Travellers’ Diarrhoea. Frontiers in Microbiology, 13. https://doi.org/10.3389/fmicb.2022.862234

- Feldgarden, M., Brover, V., Gonzalez-Escalona, N., Frye, J. G., Haendiges, J., Haft, D. H., Hoffmann, M., Pettengill, J. B., Prasad, A. B., Tillman, G. E., Tyson, G. H., & Klimke, W. (2021). AMRFinderPlus and the Reference Gene Catalog facilitate examination of the genomic links among antimicrobial resistance, stress response, and virulence. Scientific Reports, 11(1). https://doi.org/10.1038/s41598-021-91456-0

- Gurevich, A., Saveliev, V., Vyahhi, N., & Tesler, G. (2013). QUAST: Quality assessment tool for genome assemblies. Bioinformatics, 29(8), 1072–1075. https://doi.org/10.1093/bioinformatics/btt086

- Hendriksen, R. S., Bortolaia, V., Tate, H., Tyson, G. H., Aarestrup, F. M., & McDermott, P. F. (2019). Using Genomics to Track Global Antimicrobial Resistance. Frontiers in Public Health, 7, 242. https://doi.org/10.3389/fpubh.2019.00242

- Kolmogorov, M., Yuan, J., Lin, Y., & Pevzner, P. A. (2019). Assembly of long, error-prone reads using repeat graphs. Nature Biotechnology, 37(5), 540–546. https://doi.org/10.1038/s41587-019-0072-8

- Manni, M., Berkeley, M. R., Seppey, M., Simão, F. A., & Zdobnov, E. M. (2021). BUSCO Update: Novel and Streamlined Workflows along with Broader and Deeper Phylogenetic Coverage for Scoring of Eukaryotic, Prokaryotic, and Viral Genomes. Molecular Biology and Evolution, 38(10), 4647–4654. https://doi.org/10.1093/MOLBEV/MSAB199

- McArthur, A. G., & Tsang, K. K. (2017). Antimicrobial resistance surveillance in the genomic age. Annals of the New York Academy of Sciences, 1388(1), 78–91. https://doi.org/10.1111/nyas.13289

- McArthur, A. G., Waglechner, N., Nizam, F., Yan, A., Azad, M. A., Baylay, A. J., Bhullar, K., Canova, M. J., de Pascale, G., Ejim, L., Kalan, L., King, A. M., Koteva, K., Morar, M., Mulvey, M. R., O’Brien, J. S., Pawlowski, A. C., Piddock, L. J. v., Spanogiannopoulos, P., … Wright, G. D. (2013). The Comprehensive Antibiotic Resistance Database. Antimicrobial Agents and Chemotherapy, 57(7), 3348–3357. https://doi.org/10.1128/AAC.00419-13

- Murray, C. J. L., Ikuta, K. S., Sharara, F., Swetschinski, L., Robles Aguilar, G., Gray, A., Han, C., Bisignano, C., Rao, P., Wool, E., Johnson, S. C., Browne, A. J., Chipeta, M. G., Fell, F., Hackett, S., Haines-Woodhouse, G., Kashef Hamadani, B. H., Kumaran, E. A. P., McManigal, B., … Naghavi, M. (2022). Global burden of bacterial antimicrobial resistance in 2019: a systematic analysis. The Lancet, 399(10325), 629–655. https://doi.org/10.1016/S0140-6736(21)02724-0

- Schwengers, O., Jelonek, L., Dieckmann, M. A., Beyvers, S., Blom, J., & Goesmann, A. (2021). Bakta: rapid and standardized annotation of bacterial genomes via alignment-free sequence identification. Microbial Genomics, 7(11). https://doi.org/10.1099/mgen.0.000685

- Seemann, T. (2014). Prokka: rapid prokaryotic genome annotation. Bioinformatics, 30(14), 2068–2069. https://doi.org/10.1093/bioinformatics/btu153

- Struelens, M. J., Ludden, C., Werner, G., Sintchenko, V., Jokelainen, P., & Ip, M. (2024). Real-time genomic surveillance for enhanced control of infectious diseases and antimicrobial resistance. Frontiers in Science, 2. https://doi.org/10.3389/fsci.2024.1298248

- Wang, Y., Zhao, Y., Bollas, A., Wang, Y., & Au, K. F. (2021). Nanopore sequencing technology, bioinformatics and applications. Nature Biotechnology, 39(11), 1348–1365. https://doi.org/10.1038/s41587-021-01108-x

---

**Didukung oleh:**

*This work is enabled by the support from [The UK Aid Fleming Fund Country Grant to Indonesia Phase II][Fleming Fund].*

[AMR_Analysis_Pipeline]: https://github.com/rpratam/amr/blob/main/AMR_Analysis_Pipeline.md
[Fleming Fund]: https://www.flemingfund.org/publications/phase-ii-of-fleming-fund-launches-in-indonesia/

---

**Kontak & Dukungan**
Jika Anda memiliki pertanyaan atau memerlukan bantuan, jangan ragu untuk membuka issue di repository ini atau menghubungi tim pengembang.

**Selamat belajar dan berkontribusi dalam perjuangan melawan resistensi antimikroba!**
