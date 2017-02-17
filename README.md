# Rodents_project
This repository is for a rodent project with Ben and Jake. 
This repository is in complement of the one of Ben. In it, will be the scripts in order to try to improve the previous obtained results.

- 1st idea: improving the HiSeq assembly this time using the gene sequences available for mouse and rats (see [Wright et al. 2016](http://www.nature.com/articles/ncomms14251) for the idea).

((1st?) Might try to use *Apodemus sylvaticus* assembly to improve our assembly, see the notes below)

(1) Blast gene transcript or CDS from mouse and rat on the de novo assemblies (for the moment abyss assembly N50 ~ 6kb, which is pretty ok)

(2) Create "chromosomes" using blast results

a - Mouse/rat genes on same chromosomes. If multiple genes on 1 scaffold: if more than 2, consider as the good chromosome, the one for which we have the highest number of genes ; if 2 or more but same number of genes on each chromosomes, need to consider blast characteristics (e-value...)

b - Chromosome in the mouse but scaffold on the rat (or opposite): assign the scaffold to the chromosome

c - If different chromosomes on the mouse and on the rat: consider blast statistics

(3) Map HiSeq on newly formed "chromosomes": difference in coverage (can use windows in term on scaffold number and the increase resolution where there is a reduced coverage). Should check if the region where we have (if we have) a difference in coverage compared to the rest of the genome is ~ the same size between the 3 species. For that we also need to check the coverage of the assembly for the 3 species (can be done using k-mer distribution using jellyfish). In theory regions on X chromosome or Y chromosome that does not have an homologue on the other chromosome, should be half of the coverage of an autosome.

(4) Map GBS data and estimate heterozygozity between males and females (can again use scaffolds at 1st as windows) + estimate X:A ratio for each species

(5) Depending on the coverage, can perhaps have a look on the TEs distribution (diff between species, correlated with testis:body size ratio?)

**Notes:** 

- *Apodemus sylvaticus* has a genome available on NCBI. It is in a scaffold stage but can be very usefull to improve our assembly (perhaps good parts of each assembly are not the same), n50=245kb.

- *Microtus* genome is assembled into chromosomes. Not sure we can use it but considering the species has interesting sex-chromosome evolution. Considering the rapid evolution of rodents genomes and all the different sex-determining systems, it might be usefull to have other "chromosome assemblies" available. 

