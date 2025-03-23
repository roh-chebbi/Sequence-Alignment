# Sequence Alignment Comparison Script

This Python script reads two aligned sequences from a FASTA file and visualizes their alignment, highlighting matching positions.

## Description

The script performs the following tasks:
1. Reads a FASTA file containing two aligned sequences.
2. Compares the sequences base by base.
3. Outputs the sequences with a visual representation of their alignment:
   - Matching bases are indicated with a '|' character.
   - Mismatches are represented by a space.

## Usage

```
python sequence_alignment.py <FASTA_file>
```

### Arguments
- `<FASTA_file>`: Path to the input FASTA file containing two aligned sequences.

### Input File Format
The input FASTA file should contain two sequences in the following format:
```
>seq1
SEQUENCE1
>seq2
SEQUENCE2
```

## Example

Given a FASTA file `aligned.fna` with the following content:
```
>Pa
ACGTCCTGAGGGAGAAAGTGGGGGATCTTCGGACCTCACGCTATCAGATGAGCCTAGGTC
>Vc
AACCTCGCAAGAGCAAAGCAGGGGACCTTCGGGCCTTGCGCTACCGGATATGCCCAGGTG
```

Running the script:
```
python sequence_alignment.py aligned.fna
```

Will produce the output:
```
ACGTCCTGAGGGAGAAAGTGGGGGATCTTCGGACCTCACGCTATCAGATGAGCCTAGGTC
|    |  | |   ||||  ||||| |||||| |||  ||||| | |||  ||| ||||
AACCTCGCAAGAGCAAAGCAGGGGACCTTCGGGCCTTGCGCTACCGGATATGCCCAGGTG
```

## Requirements
- Python 3.x

## Notes
- The script assumes the input sequences are pre-aligned and of equal length.
- It processes only the first two sequences in the FASTA file.
- Ensure the input FASTA file is correctly formatted to avoid errors.
