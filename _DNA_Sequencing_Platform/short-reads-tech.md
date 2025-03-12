![collaboration-logo](./IM/Github_image_banner.png)

# The technology that initiate massive parallel sequencing

​Short-read sequencing technologies have revolutionized genomics by enabling high-throughput, accurate, and cost-effective DNA sequencing. Two prominent platforms in this domain are Illumina and MGI, each employing distinct methodologies to achieve rapid and precise sequencing results.​ There are several

## Illumina Sequencing Technology

Illumina's sequencing platforms are based on the principle of "sequencing by synthesis" (SBS), a method that determines DNA sequences through the incorporation of fluorescently labeled nucleotides during DNA synthesis. The general workflow involves several key steps:​

1. **Library Preparation:** Genomic DNA is fragmented into smaller pieces, typically ranging from 50 to 500 base pairs. Adapters containing specific sequences are then ligated to both ends of these fragments. These adapters serve multiple purposes: they facilitate the attachment of DNA fragments to the flow cell, provide priming sites for amplification and sequencing, and allow for sample multiplexing through unique index sequences.
 ​
2. **Cluster Generation:** The adapter-ligated DNA fragments are introduced into a flow cell, a glass slide with lanes coated with oligonucleotides complementary to the adapter sequences. Through a process called bridge amplification, each DNA fragment is clonally amplified to form clusters of identical sequences. This amplification enhances the signal during sequencing, ensuring accurate base calling. ​

3. **Sequencing by Synthesis:** During this step, fluorescently labeled reversible terminator nucleotides are incorporated into the growing DNA strand by DNA polymerase. Each of the four nucleotides emits a distinct fluorescent signal upon incorporation, allowing real-time detection of the added base. After each incorporation, the fluorescent label and the terminating group are chemically removed, permitting the next cycle of nucleotide addition. This cyclic process is repeated, enabling the determination of the DNA sequence in a massively parallel manner. ​

Illumina's platforms, such as the MiSeq, NextSeq, and NovaSeq series, are widely adopted due to their high accuracy, scalability, and versatility across various genomic applications. ​
en.wikipedia.org

## MGI Sequencing Technology

MGI, a subsidiary of BGI Group, offers sequencing platforms that leverage DNA nanoball sequencing combined with combinatorial probe-anchor synthesis (cPAS) technology. This approach encompasses the following steps:​

1. **Library Preparation:** Similar to Illumina, genomic DNA is fragmented, and adapters are ligated to the fragments. These adapters contain sequences necessary for subsequent amplification and sequencing processes.
​
2. **DNA Nanoball (DNB) Formation:** The adapter-ligated DNA fragments undergo rolling circle replication, resulting in the formation of DNA nanoballs—highly compact, circular DNA structures. This amplification method is PCR-free, reducing amplification bias and errors associated with PCR. ​

3. **Loading onto Patterned Arrays:** The DNBs are loaded onto a patterned array chip, ensuring uniform spacing and high-density packing. This arrangement enhances sequencing accuracy and throughput by allowing precise imaging and reduced signal interference. ​

4. **Sequencing by cPAS:** Using combinatorial probe-anchor synthesis, fluorescently labeled nucleotides are incorporated based on the template sequence. The emitted fluorescence is detected to determine the DNA sequence. This method allows for high-throughput sequencing with reduced error rates. ​

MGI's platforms, such as the DNBSEQ series, are recognized for their high throughput, cost-effectiveness, and suitability for large-scale genomic projects. ​
