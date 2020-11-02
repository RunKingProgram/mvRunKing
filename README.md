# GEMMAX
## Downloading GEMMAX

GEMMAX can be downloaded from https://github.com/YuxinSong-prog/GEMMAX.

## Input Files
GEMMAX requires three main input files : PLINK BED genotype file, phenotype file and relatedness matrix.<br>
#### PLINK BED genotype file
PLINK 1 binary file and the structure of these files is described in http://www.cog-genomics.org/plink/1.9/formats#bed. 
#### Phenotype file
Phenotype file that only contains phenotypic variates, and the order of individuals should be the same as genotype file. One should include multiple correlated phenotypes in multiple columns in the phenotype file. <br>
#### Relatedness matrix file
Relatedness matrix is a  n × n matrix, where each row and each column corresponds to individuals in the same order as in the .fam file, and *i*th row and *j*th column is a number indicating the relatedness value between *i*th and *j*th individuals. <br>

## Association Tests

Currently GEMMAX takes only PLINK BED files as input format. You can specify different columns of phenotypes for association tests by using “-n [num1] [num2]...[numd]”, where “-n 1 2 ” uses the original 1st and 2nd columns as phenotypes, and “-n 2 3 5” uses the 2nd, 3rd and 5th columns, and so on. 

The basic usages for association analysis are:
```
./GEMMAX -bfile [plinkfile] -p [phenofile] -k [kinshipfile] -SeparateGEMMAX -n [num1] [num2]...[numd] -o [outputfilename]

./GEMMAX -bfile [plinkfile] -p [phenofile] -k [kinshipfile] -JiontGEMMAX -n [num1] [num2]...[numd]  -o [outputfilename]

```
