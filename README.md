# ENGR010-E4

# Engineering Assignment 4 – DNA Sequencing

This project converts DNA sequences into amino acid sequences using a translation matrix. It includes functions for reading DNA files, parsing codon–amino acid mappings, translating sequences, and verifying accuracy against official protein files.


## Objective
Build a pipeline that:
- Reads and cleans DNA sequence files  
- Loads a codon → amino acid translation dictionary  
- Converts DNA (in codons) to amino acid sequences  
- Reads official protein sequences  
- Compares translated sequences to official sequences  
- Repeats the process for multiple DNA/protein pairs  

## Workflow Summary

### 1. Read DNA Data
- Removes formatting, whitespace, and invalid characters  
- Returns a clean list of DNA bases (`A`, `T`, `C`, `G`)

### 2. Read Translation Table
- Parses a text file containing codon–amino acid pairs  
- Builds a usable dictionary for translation

### 3. DNA → Amino Acid Conversion
- Slices DNA using biological indexing (start/stop)  
- Groups bases into codons (3‑letter chunks)  
- Converts each codon using the translation dictionary  
- Returns the amino acid sequence as a string

### 4. Read Official Amino Acid Sequence
- Reads protein files directly  
- Returns the sequence as a list or string

### 5. Compare Sequences
- Checks whether translated DNA matches the official protein  
- Returns `"True"` or `"False"`

### 6. Repeat for Additional DNA Files
- Translation and comparison performed for:
  - DNA_NM_1 → Protein_1  
  - DNA_NM_2 → Protein_2  
  - DNA_NM_3 → Protein_3  
- All comparisons returned **True**

## Key Findings
- DNA translation works correctly across multiple test files.
- Cleaning input data is essential for accurate codon grouping.
- The translation dictionary must be parsed carefully to avoid formatting errors.
- All translated sequences matched their official protein counterparts.

## Sources
- https://www.genome.gov/genetics-glossary/DNA  
- https://www.ncbi.nlm.nih.gov/Class/MLACourse/Original8Hour/GeneticCode.html
