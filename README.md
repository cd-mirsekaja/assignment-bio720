# bio720 - Graded Assignment, Week 4
This directory contains the data and results of a phylogenetic analysis performed for the course "Marine Biodiversity". The solutions to all seven questions is below, while a detailed report can be found at both [report.md](report.md) and [report.html](report.html).

The websites and programs used in this project were:
- [Pearl](https://www.gear-genomics.com/pearl)
- [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
- [WoRMS](https://marinespecies.org)
- [Seaview](https://doua.prabi.fr/software/seaview/)
- [MEGA](https://www.megasoftware.net/)

## Results

### 1. Create consensus sequences
Consensus sequences were exported from [Pearl](https://www.gear-genomics.com/pearl/) after manual editing, then saved in separate files in [data/seq/consensus_edited](data/seq/consensus_edited/). There is also a combined FASTA file of these sequences in [data/seq/seq_consensus-m.fasta](data/seq/seq_consensus-m.fasta).
The complement sequences for these are found in [data/seq/seq_complement.fst](data/seq/seq_complement.fst).

### 2. BLAST consensus sequences
The results of the BLAST search are contained in [data/blast_results.csv](data/blast_results.csv).

### 3. Build and save NJ tree
A neighbour-joining tree was created in MEGA and can be found in [data/images/phylotree_filtered.pdf](data/images/phylotree_filtered.pdf). There is also a [version with branch lengths](data/images/phylotree_filtered_branchlengths.pdf) available (filtered to only show lengths over 0.15).

### 4. Count species
In total, 22 species were found in the dataset. Of these, two were ambiguous and could not conclusively be determined, and one was suspicous, not fitting the dataset.

### 5. Calculate distances
After grouping the sequences by species, a distance matrix of the mean distance between groups was created in MEGA. This can be found at [data/distance_matrix.csv](data/distance_matrix.csv).

### 6. Find the suspicous sequence
While almost all sequences in the dataset were identified as marine species, one fell out of that schema. `SR_303` was identified with high likelyhood to be from a human, with some possibility of it coming from the Arthropod family Scutigerellidae. This is likely due to contamination during the sample processing in the lab.

### 7. Find the ambiguous species and find out what is going on there (literature)
Three sequences in the dataset were not able to be identified clearly. For `PM2_06`, `PM2_07` and `PM3_03`, the likelyhood for them being *Liocarcinus holsatus* or *Polybius henslowii* was exactly the same percentage.

A literature review revealed this to be the result of a taxonomic regrouping. *Liocarcinus holsatus* was moved into the genus *Polybius* and is now *Polybius holsatus* (Garcia-Raso et al., 2024). *P. holsatus* seems to be a rather new species, resulting from a speciation in *P. henslowii* (Plagge et al., 2016). The two species are genetically very similar, which likely led to the ambiguous identification from BLAST. 
While the old name is still listed as a synonym on WoRMS (WoRMS Editorial Board, 2026), it is no longer valid. Since the regrouping of the species has happened fairly recently, the BLAST databases have likely not been updated yet, leading them to report an invalid name.

## Literature

1. García-Raso, E. et al. (2024) ‘A new cryptic species of Polybiidae (Crustacea: Decapoda: Portunoidea) from the East Atlantic, with considerations on the genus Polybius’, European Journal of Taxonomy, 930, pp. 277–313. Available at: https://doi.org/10.5852/ejt.2024.930.2501.
2. Plagge, C. et al. (2016) ‘Liocarcinus corrugatus (Pennant, 1777) (Crustacea: Brachyura: Portunidae): a cosmopolitan brachyuran species?’, Raffles Bulletin of Zoology. Available at: https://zoobank.org/References/73BA15E0-882D-432B-A097-C12C911609CF.
3. WoRMS Editorial Board (2026) ‘World Register of Marine Species’. VLIZ. Available at: https://doi.org/10.14284/170.
