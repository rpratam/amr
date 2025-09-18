![collaboration-logo](../IM/Github_image_banner.png)

# **Teknologi Sekuensing: Illumina vs. Oxford Nanopore Technologies**

Pemilihan teknologi sekuensing sangat mempengaruhi pendekatan, kapabilitas, dan hasil analisis AMR berbasis WGS. Dua platform dominan saat ini memimpin bidang ini, masing-masing dengan keunggulan dan pertimbangan yang berbeda:

### Teknologi Sekuensing Illumina

**Platform Illumina** menggunakan konsep _sequencing-by-synthesis_ untuk menghasilkan _reads_ pendek berkualitas tinggi yang umumnya berkisar antara 75 hingga 300 pasang basa. Teknologi ini telah menjadi standar emas untuk sekuensing genomik karena akurasi yang luar biasa dan efektivitas biayanya.

**Karakteristik Utama:**
- **Akurasi tinggi**: Tingkat kesalahan umumnya <0,1%, memastikan variant calling yang dapat diandalkan
- **Throughput tinggi**: Mampu menghasilkan ratusan juta reads per run
- **Efektif biaya**: Biaya per-basa sekuensing yang lebih rendah, terutama untuk aplikasi throughput tinggi
- **Bioinformatika matang**: Pipeline analisis yang sudah mapan dan ketersediaan tools yang luas
- **Workflow terstandar**: Protokol yang dapat direproduksi dan banyak diadopsi dalam setting klinis dan penelitian

**Aplikasi dalam Analisis AMR:**
- Identifikasi akurat mutasi titik dan indel kecil
- Deteksi yang dapat diandalkan untuk gen resistensi yang dikenal
- Strain typing resolusi tinggi dan analisis filogenetik
- Studi surveilans skala besar dan genomik populasi
- Diagnostik klinis yang memerlukan akurasi tinggi

### Oxford Nanopore Technologies (ONT)

**Platform Oxford Nanopore** menggunakan teknologi nanopore sequencing untuk menghasilkan reads panjang, umumnya berkisar dari ratusan hingga ratusan ribu pasang basa. Teknologi ini menawarkan keunggulan unik untuk analisis genomik yang kompleks.

**Karakteristik Utama:**
- **Reads panjang**: Panjang read rata-rata 10-50 kb, dengan beberapa reads melebihi 100 kb
- **Sekuensing real-time**: Streaming data langsung memungkinkan analisis cepat selama sekuensing
- **Platform portabel**: Perangkat kompak yang cocok untuk point-of-care dan aplikasi lapangan
- **Sekuensing DNA/RNA langsung**: Tidak ada bias amplifikasi, mempertahankan modifikasi asli
- **Preparasi library cepat**: Workflow sampel-ke-sekuen dapat dicapai dalam hitungan jam

**Aplikasi dalam Analisis AMR:**
- Resolusi struktur genomik kompleks dan daerah repetitif
- Karakterisasi lengkap plasmid resistensi dan elemen genetik mobile
- Investigasi outbreak real-time dan pelacakan kontak
- Diagnostik point-of-care di setting dengan sumber daya terbatas
- Deteksi varian struktural dan rearrangement genomik skala besar

## Analisis Komparatif: Pertimbangan Pemilihan Teknologi

| Aspek | Illumina | Oxford Nanopore |
|--------|----------|-----------------|
| **Akurasi read** | >99,9% | ~95-98% (terus meningkat) |
| **Panjang read** | 75-300 bp | 10-50+ kb rata-rata |
| **Throughput** | Sangat tinggi | Sedang hingga tinggi |
| **Biaya per basa** | Rendah | Sedang |
| **Waktu penyelesaian** | 1-3 hari | Jam hingga 1 hari |
| **Biaya peralatan** | Tinggi | Rendah hingga sedang |
| **Portabilitas** | Terbatas | Tinggi |
| **Kualitas assembly** | Kontiguitas baik | Kontiguitas sangat baik |
| **Resolusi plasmid** | Menantang | Sangat baik |
| **Mutasi titik** | Deteksi sangat baik | Deteksi baik |

## Gambaran Workflow Terintegrasi

Analisis AMR berbasis WGS modern sering mendapat manfaat dari pendekatan hibrid yang memanfaatkan kekuatan kedua teknologi. Namun, workflow spesifik platform juga sangat efektif ketika dioptimalkan dengan tepat.

**Langkah Analisis Inti:**
1. **_Quality Control_ dan _Preprocessing_**: Penilaian dan filtering data sekuensing mentah
2. **_Genome Assembly_**: Rekonstruksi sekuens genomik dari reads sekuensing
3. **Penilaian Kualitas _Assembly_**: Evaluasi kelengkapan dan akurasi assembly
4. **Visualisasi _Assembly_**: Analisis struktural organisasi genomik
5. **Deteksi Gen Resistensi**: Identifikasi dan karakterisasi determinan AMR
6. **Analisis Filogenetik**: Hubungan evolusioner dan pelacakan transmisi
7. **Pembuatan Laporan**: Ringkasan profil AMR yang komprehensif

## Aplikasi Klinis dan Kesehatan Masyarakat

Analisis AMR berbasis WGS memiliki aplikasi transformatif di berbagai domain:

**Mikrobiologi Klinis:**
- Profiling resistensi cepat untuk panduan pengobatan
- Pengendalian infeksi dan epidemiologi rumah sakit
- Pemilihan terapi antimikroba presisi

**Surveilans Kesehatan Masyarakat:**
- Monitoring AMR nasional dan internasional
- Deteksi dini mekanisme resistensi yang muncul
- Pengembangan kebijakan untuk antimicrobial stewardship

**Aplikasi Penelitian:**
- Evolusi dan diseminasi mekanisme resistensi
- Penemuan gen resistensi baru
- Investigasi outbreak epidemiologi

## Gambaran Pipeline

Bagian-bagian berikut akan menyediakan protokol langkah demi langkah yang rinci untuk mengimplementasikan workflow analisis AMR berbasis WGS yang disesuaikan untuk platform sekuensing Illumina dan ONT. Setiap bagian mencakup contoh praktis, penjelasan parameter, dan praktik terbaik untuk memastikan hasil yang dapat direproduksi dan dapat diandalkan.

Pipeline komprehensif kami mencakup langkah-langkah analisis penting dari quality control data mentah hingga karakterisasi resistensi akhir, memberikan peneliti dan klinisi tools yang diperlukan untuk memanfaatkan potensi penuh teknologi genomik dalam memerangi resistensi antimikroba.

### Referensi

- Ellington, M. J., Ekelund, O., Aarestrup, F. M., Canton, R., Doumith, M., Giske, C., ... & Woodford, N. (2017). **The role of whole genome sequencing in antimicrobial susceptibility testing of bacteria: report from the EUCAST Subcommittee**. *Clinical Microbiology and Infection*, 23(1), 2-22. DOI: https://doi.org/10.1016/j.cmi.2016.11.012

- Hendriksen, R. S., Bortolaia, V., Tate, H., Tyson, G. H., Aarestrup, F. M., & McDermott, P. F. (2019). **Using genomics to track global antimicrobial resistance**. *Frontiers in Public Health*, 7, 242. DOI: https://doi.org/10.3389/fpubh.2019.00242

- Gwinn, M., MacCannell, D., & Khabbaz, R. (2017). **Integrating advanced molecular technologies into public health**. *The Journal of Clinical Investigation*, 127(4), 1174-1182. DOI: https://doi.org/10.1128/jcm.01967-16

- Wick, R. R., Judd, L. M., Gorrie, C. L., & Holt, K. E. (2017). **Completing bacterial genome assemblies with multiplex MinION sequencing**. *Microbial Genomics*, 3(10), e000132. DOI: https://doi.org/10.1099/mgen.0.000132

- Punina, N. V., Makridakis, N. M., Remnev, M. A., & Topunov, A. F. (2015). **Whole-genome sequencing targets drug-resistant bacterial infections**. *Human Genomics*, 9(1), 1-9. DOI: https://doi.org/10.1186/s40246-015-0037-z
