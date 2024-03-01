
# Project Title

A brief description of what this project does and who it's for

# Bioinformatics Linux Exercise

This repository contains files and scripts for a bioinformatics exercise performed in a Linux environment.

## Project Directory Structure

- `Exercise`: Main project directory.
  - `data`: Directory for storing dataset files.
    - `sequences`: Directory for sequence data files.
      - `Combined_data.fa`: Combined dataset file.
      - `nrf1_seq.fa`: Another dataset file.
  - `results`: Directory for storing result files.
  - `scripts`: Directory for storing scripts.
    - `extract_seq.sh`: Bash script for extracting sequence headers.

### Commands Used

The following commands were used to perform the tasks:

1. Create project directory:
   ```bash
   mkdir Exercise
2. Create project sub-directories:

   cd Exercise

    mkdir data results scripts

      cd data

       mkdir sequences
3. Copy datasets:

v
   cp /mnt/c/Users/User/Documents/      dataProject/*.fa  
   
 /home/milka/Assignment1/linux-exercise/Exercise/data/sequences

4.Extract sequence headers:

     grep '>' /home/milka/Assignment1/linux-exericise/Exercise/data/sequences/*.fa | cut -d' ' -f1 > ../../results/sequence_names.txt

5.Save extraction commands in ascript:

echo "grep '>' /home/milka/Assignment/linux-exercise/Exercise/data/sequences/*.fa | cut -d' ' -f1 > ../../results/sequence_names.txt" > ../scripts/extract_seq.sh

Make the file executable:

  chmod +x ../scripts/extract_seq.sh

6.Count the mRNA sequences:

grep -c 'mRNA' /home/milka/Assignment1//linux-exercise/Exercise/data/sequences/*.fa > ../../results/mRNA_count.txt

7.Count organisms without duplicates:

cat /home/milka/Assignment1/linux-exercise/Exercise/results/mRNA_count.txt | cut -d':' -f2 | sort -u > ../results/non_duplicate_organisms.txt

8.Count predicted organisms:



9.Count nucleotides and bases:
cat /home/milka/Assignment1/linux-exercise/Exercise/data/sequences/*.fa | grep -v '>' | tr -d '\n' | wc -c > ../../results/total_nucleotides.txt

grep -o -i -E 'A|T|C|G' /home/milka/Assignment1/linux-exercise/Exercise/data/sequences/*.fa | sort | uniq -c > ../../results/base_counts.txt

#### results
    sequence_names.txt: File containing extracted sequence headers    mRNA_count.txt: File with counts of mRNA and other sequences.

    non_duplicate_organisms.txt: File with organisms without duplicates.

    total_nucleotides.txt: File with the count of total nucleotides.

    base_counts.txt: File with counts of each nucleotide base.

 
