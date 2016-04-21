---
layout: post
title: NSHA NGS Analysis Pipeline
---
In brief data was aligned to the human reference genome (GRCh37.75) with BWA[1] and
processed using Picard[2], the GATK[3], and VT[4]. Variants were called using six
different variant callers, each with different error profiles and performance
characteristics: MuTect[5], FreeBayes[6], VarDict[7], Pindel[8], Platypus[9],
and Scalpel[10] and then combined into a unified call set using bcbio-ensemble[11].
Variants were  annotated with snpEff[12] and VCFAnno[13] from a variety of data
sources including dbSNP[14], 1000 Genomes[15], The Exome Sequencing Project's EVS[16],
Ensembl[17], ClinVar[18], and COSMIC[19].

##References:

1. [BWA](https://)
2. [Picard](https://)  
3. [GATK](https://)  
4. [VT](https://)
5. [MuTect](https://)
6. [FreeBayes](https://)
7. [VarDict](https://)
8. [Pindel](https://)
9. [Platypus](https://)
10. [Scalpel](https://)
11. [bcbio-ensemble](https://)
12. [snpEff](https://)
13. [VCFAnno](https://)
14. [dbSNP](https://)
15. [100 Genomes](https://)
16. [EVS](https://)
17. [Ensemble](https://)
18. [ClinVar](https://)
19. [COSMIC](https://)
