![collaboration-logo](./IM/Github_image_banner.png)

# Pipeline Analisis AMR

## Menghadapi Tantangan Resistensi Antimikroba di Era Modern

Resistensi Antimikroba (AMR) telah menjadi salah satu ancaman kesehatan global yang paling mendesak di abad ke-21. Fenomena ini terjadi ketika bakteri, virus, jamur, dan parasit mengembangkan kemampuan untuk melawan obat-obatan yang sebelumnya efektif dalam mengobati infeksi yang mereka sebabkan. Akibatnya, pengobatan standar menjadi tidak efektif, infeksi menjadi lebih sulit disembuhkan, dan risiko penyebaran penyakit, komplikasi serius, bahkan kematian meningkat drastis.

Di Indonesia, masalah AMR semakin mengkhawatirkan dengan meningkatnya kasus infeksi yang resisten terhadap antibiotik. Menurut data WHO, AMR dapat menyebabkan 10 juta kematian per tahun pada 2050 jika tidak ditangani dengan serius. Oleh karena itu, kemampuan untuk mengidentifikasi dan menganalisis mekanisme resistensi melalui teknologi sekuensing DNA menjadi kunci utama dalam memerangi masalah ini.

## Untuk Siapa Panduan Ini?

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

**Tidak diperlukan pengalaman sebelumnya dengan Linux atau pipeline bioinformatika!** Panduan ini dirancang untuk memandu Anda langkah demi langkah, mulai dari konsep dasar hingga analisis lanjutan.

## Apa yang Akan Anda Pelajari?
### Teknologi Sekuensing DNA
- **Platform Illumina vs Oxford Nanopore Technologies**: Perbandingan komprehensif kedua teknologi utama
- **Short-reads technology (NGS)**:
  - Platform Illumina dan kelebihan analisis presisi tinggi
  - Platform MGI sebagai alternatif cost-effective
- **Long-reads technology (TGS)**:
  - Oxford Nanopore Technology (ONT) untuk real-time sequencing
  - Pacific Bioscience untuk akurasi tinggi long-reads
- **Pemilihan strategi**: Kapan menggunakan teknologi tertentu untuk analisis AMR

### Pentingnya Linux dalam Bioinformatika  
- **Setup Environment**: Instalasi Windows Subsystem for Linux 2 (WSL2) untuk pengguna Windows
- **Conda Environment**: Pengelolaan software bioinformatika dengan mudah
- **Linux Command Basics**: Perintah fundamental untuk navigasi dan manipulasi data genomik
- **File Management**: Pengelolaan data sekuensing berukuran besar secara efisien

### Pipeline Bioinformatika _Whole Genome Sequencing_ Bakteri
#### Memahami Data Raw Sequence (*.fastq)
- Struktur dan format file FASTQ
- Quality scores dan interpretasinya
- Characteristics data Illumina vs ONT

#### Alur Kerja pipeline ini
- _Quality control_ dan _filtering data_
- Perakitan genom
- Evaluasi kualitas hasil _assembly_
- Visualisasi struktur _genome assembly graph_
- Evaluasi kelengkapan _genome assembly_
- Deteksi kontaminasi dalam assembly
- Anotasi fungsional gen dalam genom
- Identifikasi gen resistensi antimikroba


## Mengapa AMR Menjadi Fokus Utama?
### Dampak Global dan Lokal
Resistensi antimikroba bukan hanya masalah medis, tetapi juga:
- **Ekonomi**: Biaya perawatan yang meningkat drastis
- **Sosial**: Meningkatnya morbiditas dan mortalitas
- **Ketahanan Pangan**: Resistensi pada patogen tanaman dan hewan
- **Keamanan Nasional**: Potensi bioterrorisme menggunakan patogen resisten

### Kondisi di Indonesia
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


## Cara Menggunakan Panduan Ini
### Struktur Pembelajaran Bertahap
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

### Roadmap Pembelajaran:
**Langkah 1:** Pahami platform sekuensing → **Langkah 2:** _Setup Linux environment_ → **Langkah 3:** Praktik analisis Illumina → **Langkah 4:** Praktik analisis ONT → **Langkah 5:** Identifikasi gen AMR

### 🔧 Yang Perlu Dipersiapkan:
- Komputer dengan akses internet (Windows/Mac/Linux)
- Minimal 16Gb RAM (64GB recommended untuk dataset besar)  
- Ruang storage (SSD) 100GB+ untuk software dan sample data
- Koneksi internet stabil untuk download _tools_ dan _databases_

### 🛠️ Software Ecosystem yang Akan Dikuasai:
**Quality Control & Preprocessing:** Fastp, NanoPlot  
**Genome Assembly:** Spades, Shovill, Flye  
**Assembly Evaluation:** QUAST, BUSCO, CheckM  
**Visualization:** Bandage untuk assembly graphs  
**Annotation:** Prokka untuk functional genes  
**AMR Detection:** Abricate dengan multiple databases  
**Environment:** Conda untuk package management

Bila sudah siap, klik tautan berikut untuk memulai:
#### **[Panduan Analisis Pipeline AMR][AMR_Analysis_Pipeline]**


---

### Kontribusi dan Dukungan

**💡 Kontribusi:** Panduan ini adalah proyek open-source yang terus berkembang. Kami sangat menghargai kontribusi berupa:
- Pelaporan bug atau error dalam tutorial
- Saran improvement untuk konten
- Penambahan studi kasus baru

**🔄 Update Berkala:** Panduan ini diperbarui secara berkala untuk mencerminkan:
- Perkembangan terbaru dalam teknologi sekuensing
- Tools dan database AMR yang baru
- Best practices dalam analisis bioinformatika
- Feedback dari komunitas pengguna

---

## Referensi Ilmiah

Panduan ini dikembangkan berdasarkan literatur ilmiah terkini dari jurnal-jurnal bereputasi internasional. Berikut adalah referensi utama yang mendukung metodologi dan praktek terbaik yang dijelaskan dalam panduan:

- Bird, M. T., Greig, D. R., Nair, S., Jenkins, C., Godbole, G., & Gharbia, S. E. (2022). Use of Nanopore Sequencing to Characterise the Genomic Architecture of Mobile Genetic Elements Encoding blaCTX-M-15 in Escherichia coli Causing Travellers’ Diarrhoea. Frontiers in Microbiology, 13. https://doi.org/10.3389/fmicb.2022.862234

- Hendriksen, R. S., Bortolaia, V., Tate, H., Tyson, G. H., Aarestrup, F. M., & McDermott, P. F. (2019). Using Genomics to Track Global Antimicrobial Resistance. Frontiers in Public Health, 7, 242. https://doi.org/10.3389/fpubh.2019.00242

- McArthur, A. G., Waglechner, N., Nizam, F., Yan, A., Azad, M. A., Baylay, A. J., Bhullar, K., Canova, M. J., de Pascale, G., Ejim, L., Kalan, L., King, A. M., Koteva, K., Morar, M., Mulvey, M. R., O’Brien, J. S., Pawlowski, A. C., Piddock, L. J. v., Spanogiannopoulos, P., … Wright, G. D. (2013). The Comprehensive Antibiotic Resistance Database. Antimicrobial Agents and Chemotherapy, 57(7), 3348–3357. https://doi.org/10.1128/AAC.00419-13

- Murray, C. J. L., Ikuta, K. S., Sharara, F., Swetschinski, L., Robles Aguilar, G., Gray, A., Han, C., Bisignano, C., Rao, P., Wool, E., Johnson, S. C., Browne, A. J., Chipeta, M. G., Fell, F., Hackett, S., Haines-Woodhouse, G., Kashef Hamadani, B. H., Kumaran, E. A. P., McManigal, B., … Naghavi, M. (2022). Global burden of bacterial antimicrobial resistance in 2019: a systematic analysis. The Lancet, 399(10325), 629–655. https://doi.org/10.1016/S0140-6736(21)02724-0

- Struelens, M. J., Ludden, C., Werner, G., Sintchenko, V., Jokelainen, P., & Ip, M. (2024). Real-time genomic surveillance for enhanced control of infectious diseases and antimicrobial resistance. Frontiers in Science, 2. https://doi.org/10.3389/fsci.2024.1298248

-

- Kolmogorov, M., Yuan, J., Lin, Y., & Pevzner, P. A. (2019). Assembly of long, error-prone reads using repeat graphs. *Nature Biotechnology*, *37*(5), 540-546.

- Soto, D. C., Sheath, D. J., Pham, J., Taggart, E., Baker, C., Oforka, L. C., ... & Goldfeder, R. L. (2022). Accelerated identification of disease-causing variants with ultra-rapid nanopore genome sequencing. *Nature Biotechnology*, *40*(7), 1035-1041.

- Wang, Y., Zhao, Y., Bollas, A., Wang, Y., & Au, K. F. (2021). Nanopore sequencing technology, bioinformatics and applications. *Nature Biotechnology*, *39*(11), 1348-1365.

### Genome Assembly Quality Assessment
- Gurevich, A., Saveliev, V., Vyahhi, N., & Tesler, G. (2013). QUAST: quality assessment tool for genome assemblies. *Bioinformatics*, *29*(8), 1072-1075.

- Mikheenko, A., Prjibelski, A., Saveliev, V., Antipov, D., & Gurevich, A. (2018). Versatile genome assembly evaluation with QUAST-LG. *Bioinformatics*, *34*(13), i142-i150.

- Simão, F. A., Waterhouse, R. M., Ioannidis, P., Kriventseva, E. V., & Zdobnov, E. M. (2015). BUSCO: assessing genome assembly and annotation completeness with single-copy orthologs. *Bioinformatics*, *31*(19), 3210-3212.

- Seppey, M., Manni, M., & Zdobnov, E. M. (2019). BUSCO: assessing genome assembly and annotation completeness. In *Gene prediction* (pp. 227-245). Humana Press.

### Genome Annotation & AMR Detection Tools
- Seemann, T. (2014). Prokka: rapid prokaryotic genome annotation. *Bioinformatics*, *30*(14), 2068-2069.

- Schwengers, O., Jelonek, L., Dieckmann, M. A., Beyvers, S., Blom, J., & Goesmann, A. (2021). Bakta: rapid and standardized annotation of bacterial genomes via alignment-free sequence identification. *Microbial Genomics*, *7*(11).

- Hunt, M., Mather, A. E., Sánchez-Busó, L., Page, A. J., Parkhill, J., Keane, J. A., & Harris, S. R. (2017). ARIBA: rapid antimicrobial resistance genotyping directly from sequencing reads. *Microbial Genomics*, *3*(10).

### Bioinformatics Pipeline & Sequence-based AMR Analysis
- Hendriksen, R. S., Bortolaia, V., Tate, H., Tyson, G. H., Aarestrup, F. M., & McDermott, P. F. (2019). Using genomics to track global antimicrobial resistance. *Frontiers in Public Health*, *7*, 242.

- McArthur, A. G., & Tsang, K. K. (2017). Antimicrobial resistance surveillance in the genomic age. *Annals of the New York Academy of Sciences*, *1388*(1), 78-91.

- Zankari, E., Hasman, H., Cosentino, S., Vestergaard, M., Rasmussen, S., Lund, O., ... & Larsen, M. V. (2012). Identification of acquired antimicrobial resistance genes. *Journal of Antimicrobial Chemotherapy*, *67*(11), 2640-2644.

---

**Didukung oleh:**

*This work is enabled by the support from [The UK Aid Fleming Fund Country Grant to Indonesia Phase II][Fleming Fund].*

[AMR_Analysis_Pipeline]: https://github.com/rpratam/amr/blob/main/AMR_Analysis_Pipeline.md
[Fleming Fund]: https://www.flemingfund.org/publications/phase-ii-of-fleming-fund-launches-in-indonesia/

---

**Kontak & Dukungan**
Jika Anda memiliki pertanyaan atau memerlukan bantuan, jangan ragu untuk membuka issue di repository ini atau menghubungi tim pengembang.

**Selamat belajar dan berkontribusi dalam perjuangan melawan resistensi antimikroba!**
