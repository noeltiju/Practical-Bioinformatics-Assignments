# Assignment 1 - ORI's in Bakers Yeast

    Name: Noel Abraham Tiju
    RollNo: 2022338
#### Part 1: Downloading the sequence for Bakers Yeast

The first part of the assignment is to download the sequences for 16 chromosomes of the **Saccharomyces Cerevisiae**. The sequences are written to files named **chromsomeN.fasta** in fasta format. The sequences are also stored in a dictionary called **chromosome_sequences**.

    'chromosome1':'NC_001133.9' 
    'chromosome2':'NC_001134.8' 
    'chromosome3':'NC_001135.5' 
    'chromosome4':'NC_001136.10' 
    'chromosome5':'NC_001137.3' 
    'chromosome6':'NC_001138.5' 
    'chromosome7':'NC_001139.9' 
    'chromosome8':'NC_001140.6' 
    'chromosome9':'NC_001141.2' 
    'chromosome10':'NC_001142.9'
    'chromosome11':'NC_001143.9' 
    'chromosome12':'NC_001144.5' 
    'chromosome13':'NC_001145.3' 
    'chromosome14':'NC_001146.8' 
    'chromosome15':'NC_001147.6' 
    'chromosome16':'NC_001148.4'

#### Part 2: Finding ARS features for the sequences

The second part of the assignment is to find presence of ORI's in the organism. ORI's have some distinct features called **Autonomously Replicating Sequence** (ARS). ARS's contain a particular sequence called **ACS** (Consensus sequence). From various research papers I found different 'ACS' sequences from research papers. Each sequence is explained in the code block in the notebook.

[Reference 1](https://www.sciencedirect.com/science/article/pii/S0923250812000435#bib72)

    11 BP: (A/T)TTTAT(A/G)TTT(A/T)
    17 BP: (A/T)(A/T)(A/T)-{ACS}-(G/T)(A/T)(A/T)


[Reference 2](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2004-5-4-r22#:~:text=Autonomously%20replicating%20sequences%20(ARSs)%20function,binds%20the%20origin%20recognition%20complex.)

    17 BP: WWWWTTTAYRTTTWGTT, where W = A or T, Y = C or T, and R = A or G

#### Note:

    ACS_count && ACS_indices are likely positions using reference 1 11BP sequence.
    EACS_count && EACS_indices are likely positions using reference 1 17BP sequence.
    ACS_17_count && ACS_17_indices are likely positions using reference 2 17BP sequence.