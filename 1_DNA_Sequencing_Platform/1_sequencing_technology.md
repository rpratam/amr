![collaboration-logo](../IM/Github_image_banner.png)

# **Sequencing Technologies: Illumina vs. Oxford Nanopore Technologies**

The choice of sequencing technology significantly impacts the approach, capabilities, and outcomes of WGS-based AMR analysis. Two dominant platforms currently lead the field, each with distinct advantages and considerations:

### Illumina Sequencing Technology

**Illumina platforms** utilize sequencing-by-synthesis chemistry to generate high-quality, short reads typically ranging from 75 to 300 base pairs. This technology has been the gold standard for genomic sequencing due to its exceptional accuracy and cost-effectiveness.

**Key Characteristics:**
- **High accuracy**: Error rates typically <0.1%, ensuring reliable variant calling
- **High throughput**: Capable of generating hundreds of millions of reads per run
- **Cost-effective**: Lower per-base sequencing costs, especially for high-throughput applications
- **Mature bioinformatics**: Well-established analysis pipelines and extensive tool availability
- **Standardized workflows**: Reproducible protocols widely adopted in clinical and research settings

**Applications in AMR Analysis:**
- Accurate identification of point mutations and small indels
- Reliable detection of known resistance genes
- High-resolution strain typing and phylogenetic analysis
- Large-scale surveillance studies and population genomics
- Clinical diagnostics requiring high accuracy

### Oxford Nanopore Technologies (ONT)

**Oxford Nanopore platforms** employ nanopore sequencing technology to generate long reads, typically ranging from hundreds to hundreds of thousands of base pairs. This technology offers unique advantages for complex genomic analyses.

**Key Characteristics:**
- **Long reads**: Average read lengths of 10-50 kb, with some reads exceeding 100 kb
- **Real-time sequencing**: Live data streaming enables rapid analysis during sequencing
- **Portable platforms**: Compact devices suitable for point-of-care and field applications
- **Direct RNA/DNA sequencing**: No amplification bias, preserves native modifications
- **Rapid library preparation**: Sample-to-sequence workflows achievable in hours

**Applications in AMR Analysis:**
- Resolution of complex genomic structures and repetitive regions
- Complete characterization of resistance plasmids and mobile genetic elements
- Real-time outbreak investigation and contact tracing
- Point-of-care diagnostics in resource-limited settings
- Detection of structural variants and large-scale genomic rearrangements

## Comparative Analysis: Technology Selection Considerations

| Aspect | Illumina | Oxford Nanopore |
|--------|----------|-----------------|
| **Read accuracy** | >99.9% | ~95-98% (improving) |
| **Read length** | 75-300 bp | 10-50+ kb average |
| **Throughput** | Very high | Moderate to high |
| **Cost per base** | Low | Moderate |
| **Turnaround time** | 1-3 days | Hours to 1 day |
| **Equipment cost** | High | Low to moderate |
| **Portability** | Limited | High |
| **Assembly quality** | Good contiguity | Excellent contiguity |
| **Plasmid resolution** | Challenging | Excellent |
| **Point mutations** | Excellent detection | Good detection |

## Integrated Workflow Overview

Modern WGS-based AMR analysis often benefits from hybrid approaches that leverage the strengths of both technologies. However, platform-specific workflows are also highly effective when optimized appropriately.

**Core Analysis Steps:**
1. **Quality Control and Preprocessing**: Raw sequencing data assessment and filtering
2. **Genome Assembly**: Reconstruction of genomic sequences from sequencing reads
3. **Assembly Quality Assessment**: Evaluation of assembly completeness and accuracy
4. **Assembly Visualization**: Structural analysis of genomic organization
5. **Resistance Gene Detection**: Identification and characterization of AMR determinants
6. **Phylogenetic Analysis**: Evolutionary relationships and transmission tracking
7. **Report Generation**: Comprehensive AMR profile summarization

## Clinical and Public Health Applications

WGS-based AMR analysis has transformative applications across multiple domains:

**Clinical Microbiology:**
- Rapid resistance profiling for treatment guidance
- Infection control and hospital epidemiology
- Precision antimicrobial therapy selection

**Public Health Surveillance:**
- National and international AMR monitoring
- Early detection of emerging resistance mechanisms
- Policy development for antimicrobial stewardship

**Research Applications:**
- Evolution and dissemination of resistance mechanisms
- Novel resistance gene discovery
- Epidemiological outbreak investigations

## Pipeline Overview

The following sections will provide detailed, step-by-step protocols for implementing WGS-based AMR analysis workflows tailored for both Illumina and ONT sequencing platforms. Each section includes practical examples, parameter explanations, and best practices to ensure reproducible and reliable results.

Our comprehensive pipeline covers essential analysis steps from raw data quality control through final resistance characterization, providing researchers and clinicians with the tools necessary to harness the full potential of genomic technologies in combating antimicrobial resistance.

### References

- Ellington, M. J., Ekelund, O., Aarestrup, F. M., Canton, R., Doumith, M., Giske, C., ... & Woodford, N. (2017). **The role of whole genome sequencing in antimicrobial susceptibility testing of bacteria: report from the EUCAST Subcommittee**. *Clinical Microbiology and Infection*, 23(1), 2-22.

- Hendriksen, R. S., Bortolaia, V., Tate, H., Tyson, G. H., Aarestrup, F. M., & McDermott, P. F. (2019). **Using genomics to track global antimicrobial resistance**. *Frontiers in Public Health*, 7, 242.

- Gwinn, M., MacCannell, D., & Khabbaz, R. (2017). **Integrating advanced molecular technologies into public health**. *The Journal of Clinical Investigation*, 127(4), 1174-1182.

- Wick, R. R., Judd, L. M., Gorrie, C. L., & Holt, K. E. (2017). **Completing bacterial genome assemblies with multiplex MinION sequencing**. *Microbial Genomics*, 3(10), e000132.

- Punina, N. V., Makridakis, N. M., Remnev, M. A., & Topunov, A. F. (2015). **Whole-genome sequencing targets drug-resistant bacterial infections**. *Human Genomics*, 9(1), 1-9.
