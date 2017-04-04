Need abyss scaffold as reference
```
/Users/evanslab/ncbi-blast-2.2.31+/bin/makeblastdb -in /Users/Ben/rat_genomes/ABTC26654_abyss_kmer_65/ABTC26654-8.fa -dbtype nucl -title ABTC26654 -out /Users/Ben/rat_genomes/ABTC26654_abyss_kmer_65/blast/ABTC_blastable
```
```
/Users/evanslab/ncbi-blast-2.2.31+/bin/blastn -evalue 1e-60 -query /Users/evanslab/Documents/caroline/rat_projects/CCDS_nucleotide.20161208.fna.gz -db /Users/Ben/rat_genomes/ABTC26654_abyss_kmer_65/blast/ABTC_blastable -out /Users/Ben/rat_genomes/ABTC26654_abyss_kmer_65/blast/ABTC_mouse_CCDS -outfmt 6 -max_target_seqs 1

gunzip -c /Users/evanslab/Documents/caroline/rat_projects/CCDS_nucleotide.20161208.fna.gz | /Users/evanslab/ncbi-blast-2.2.31+/bin/blastn -evalue 1e-60 -query - -db /Users/Ben/rat_genomes/ABTC26654_abyss_kmer_65/blast/ABTC_blastable -out /Users/Ben/rat_genomes/ABTC26654_abyss_kmer_65/blast/ABTC_mouse_CCDS -outfmt 6 -max_target_seqs 1
```
