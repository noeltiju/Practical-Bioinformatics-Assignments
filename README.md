# Practical-Bioinformatics-Assignments

## Assignment 1: Origins of Replication in Baker's Yeast

### Introduction

This assignment focuses on identifying the origins of replication (ORI) in the genome of **Saccharomyces cerevisiae** (Baker's yeast). ORIs are specific locations in the genome where DNA replication begins. In yeast, these origins are often associated with **Autonomously Replicating Sequences** (ARS), which contain a highly conserved **ARS Consensus Sequence** (ACS). By analyzing the yeast genome, we can identify potential ARS sites based on known ACS patterns.

### Parts of the Assignment

1. **Downloading Chromosome Sequences**:
    - The sequences for all 16 chromosomes of Saccharomyces cerevisiae are downloaded and stored in files named `chromosomeN.fasta`.
    - These sequences are also stored in a dictionary called `chromosome_sequences` for easy access.
    - Example mapping:
        ```
        'chromosome1':'NC_001133.9',
        'chromosome2':'NC_001134.8',
        ...
        'chromosome16':'NC_001148.4'
        ```

2. **Identifying ARS Features**:
    - The second part involves finding the presence of ORIs in the genome. ORIs have distinct features called **Autonomously Replicating Sequence** (ARS).
    - Different ACS patterns from research papers are used to identify potential ARS sites.
    - Reference patterns used:
        - 11 BP: (A/T)TTTAT(A/G)TTT(A/T)
        - 17 BP: (A/T)(A/T)(A/T)-{ACS}-(G/T)(A/T)(A/T)
        - 17 BP: WWWWTTTAYRTTTWGTT, where W = A or T, Y = C or T, and R = A or G

    - Results include:
        - `ACS_count` & `ACS_indices`: Likely positions using 11BP sequence.
        - `EACS_count` & `EACS_indices`: Likely positions using first 17BP sequence.
        - `ACS_17_count` & `ACS_17_indices`: Likely positions using second 17BP sequence.

---

## Assignment 2: PDC Gene Sequences in Yeast

### Introduction

This assignment involves analyzing the PDC genes in Saccharomyces cerevisiae, which are important for winemaking. The genes PDC1, PDC5, and PDC6 are studied, with PDC1 and PDC6 requiring reverse complementing due to their positions on opposite strands.

### Parts of the Assignment

1. **Downloading PDC Gene Sequences**:
    - Download sequences for PDC1, PDC5, and PDC6.
    - PDC1 and PDC6 are reverse complemented as they lie on the opposite strands.
    - Links for sequences:
        - [PDC1](https://yeastgenome.org/locus/S000004034/sequence)
        - [PDC5](https://www.yeastgenome.org/locus/S000004124/sequence)
        - [PDC6](https://www.yeastgenome.org/locus/S000003319/sequence)

2. **Running BLAST and Finding SNPs**:
    - Perform BLAST against various strains of Baker's yeast.
    - The `blast_routine` function is called, which further calls the `SNP_writer` function to write SNP results to `snp_results_{PDC_no}.txt`.

3. **Translating the Sequences**:
    - Translate each of the Highest Scoring Pairs (HSPs) into `translate_results_{PDC_no}.txt`.
    - Information included:
        - **hsp.score**: Score of the alignment.
        - **hsp.expect**: Expectation value.
        - **hsp.query**: Query sequence.
        - **hsp.sbjct**: Subject sequence.

4. **Running PolyPhen-2**:
    - Analyze amino acid substitutions using PolyPhen-2.
    - A sample report is attached: `PolyPhen-2 report PDC1.pdf`.

---

Please refer to the respective directories and files for detailed code and results for each assignment.
