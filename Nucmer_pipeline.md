# Idea
Using a similar approach described [here for the tetraploid frog species](https://github.com/caro46/Tetraploid_project/blob/master/pseudomolecules.md). 

- Nucmer: align our Abyss assembly onto the *Apodemus sylvaticus* assembly or *Apodemus speciosus* from NCBI to reduce our number of scaffolds. Or directly try to use the published assembly to make a chromosome assembly and then align ours. *A. sylvaticus* has a higher N50 so should try 1st with it, can be downloaded from [NCBI](ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/001/305/905/GCA_001305905.1_ASM130590v1/) 

- Nucmer/Promer: align our (improved?) assembly onto the rat and mouse. Compared the 2 index files and keep as sex-chromosomes only the scaffolds that are sex-chromosomes in rat + mouse, if in oly one - should identify the scaffolds as `X_chr_rat_only` ... 

- After using `bwa mem` to map reads onto the new assembly: identify sites that are heteroz in males on the X chr > identify them as `X_pseudo_autosomal` or do not use them in the analysis.

- Calculating pi for each chromosome, then compute the global ratio `X:autosome` for each species


