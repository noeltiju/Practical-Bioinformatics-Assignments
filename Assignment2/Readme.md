**PB Assignment 2**

Name: Noel Abraham Tiju  
Rollno: 2022338

Q1: Downloading PDC gene sequences

    From research I found out that PDC1, and PDC5 belong in chromosome 12 at particular indices whereas PDC6 belongs in chromosome7. These are the predominant genes responsible for winemaking.

    Based on research I performed I found out that PDC1 and PDC6 have to be reverse complemented as these genes lie on the opposite strands to perform blast for the same. I realised it from this:

1. [PDC1](https://yeastgenome.org/locus/S000004034/sequence)
2. [PDC5](https://www.yeastgenome.org/locus/S000004124/sequence)
3. [PDC6](https://www.yeastgenome.org/locus/S000003319/sequence) 

Q2: Running Blast and finding SNPs

    After downloading the sequences, the three sequences are blasted against various strains of Bakers yeast. Then blast_routine function is called which further calls SNP_writer function to write into various files of the format snp_results {PDC_no}.txt. This will contain information regarding each alignment along with SNP's for each HSP (Highest Scoring Pairs).

Q3: Translating the sequences

    Next part is to translate each of HSP pairs into translate_results {PDC_no}.txt. 

1. **hsp.score** -> Score of the alignment
2. **hsp.expect** -> Expectation value
3. **hsp.query** -> The query sequence you performed blast with
4. **hsp.sbjct** -> A particular section of a strain against with alignment was 

Q4: Running Polyphen-2:

    There is a report attached PolyPhen-2 report PDC1.pdf


This is report for amino acid substitution for:

**Title**: gi|1586061137|gb|CP036478.1| Saccharomyces cerevisiae strain ySR128 chromosome XII, complete sequence

**Positions**
410631 - 412322

**PDC Amino Acid**

At position 15 I noticed there was a mutation from K -> S. I used [Polyphen-2](http://genetics.bwh.harvard.edu/ggi/pph2/757f2671575867bab9da8be0c3509da251312f4b/9647091.html)