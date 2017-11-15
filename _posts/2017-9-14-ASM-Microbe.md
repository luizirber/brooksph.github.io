---
layout: post 
title: Taxonomic Classification Of Microbial Metagenomes Using Minhash Signatures - ASM Microbe 2017
---

I'm extremely interested in metagenomics - especially assembly and classification. One of the projects I've been working on is taxonomic classification of metagenomes using sourmash - a tool for calculation and comparison of Minhash sketches. The authors of the Mash: fast genome and metagenome distance estimation using MinHash demonstrated the utility of minHash sketches for and accurate clustering of genomes and metagenomes. Using their work as inspiration our lab developed sourmash to explore some additional questions we're interested in. The sbt gather functionality of sourmash compares minHash signatures computed with sourmash to an index containing signatures calculated for all of the microbial genomes in the NCBI RefSeq database. My advisor, C. Titus Brown and Luis Irber, a graduate student in our lab describe method for [building the index](http://blog.luizirber.org/2016/12/28/soursigs-arch-1/) and its [functionality](http://ivory.idyll.org/blog/2016-sourmash-sbt-more.html).

Below is our abstract from some work we've done characterizing the synthetic and mock metagenomes from [Skakya et al., (2013)](http://onlinelibrary.wiley.com/doi/10.1111/1462-2920.12086/abstract). We've extended this work quite a bit since it was submitted in March. I presented this work at ASM Microbe in New Orleans in June and I'll write some blog posts describing this project as it progresses. You can read the abstract below or check out the entire [poster](https://mfr.osf.io/render?url=https://osf.io/mu4gk/?action=download%26mode=render) on the open science framework. 

Poster # AES LB10 6/2/2017 12:45 - 2:45 PM

Authors: Phillip T. Brooks, Luiz Irber, C. Titus Brown

Background: Metagenomics, the study of all of the genomic content in a sample taken directly from the environment can significantly expand our biological knowledge by letting us ask questions directly of ecosystems and their microbial inhabitants. For comparative DNA sequence analysis, we developed sourmash, a command line tool and Python library that calculates unique fingerprints (i.e. MinHash signatures) for DNA sequences. MinHash signatures are small relative to the full data set and can be rapidly compared. We hypothesized that sourmash could be used to discern the taxonomic structure of complex microbial communities by comparing signatures from metagenomes to an index containing signatures for all of the microbial genomes in the NCBI Reference Sequences (RefSeq) database.

Methods: We calculated signatures for 60,052 microbial genomes using sourmash and indexed them in a searchable sequence bloom tree (SBT). Calculation of all signatures took 36 CPU hours and yielded a 4.5 GB publicly available SBT index. Next, we calculated MinHash signatures for a synthetic metagenome (64 assembled genomes) and a mock metagenome (unassembled Illumina reads), and assigned taxonomy using sourmash ‘gather’ functionality. Sourmash gather classified sequences by comparing signatures for both metagenomes to indexes containing 64 or ~60,000 signatures representing organisms in the synthetic metagenome or the entirety of the microbial genomes in the NCBI RefSeq database, respectively.

Results: Accurate taxonomic classification was restricted by the number of representative k-mers and similarity between sequences such as organisms belonging to the same genus or species, when compared to the signatures for microbial genomes in the NCBI RefSeq database. Sensitivity was enhanced by increased k-mer representation when compared to either index.

Conclusions: Sourmash ‘gather’ functionality can be used for strain level taxonomic classification of complex microbial communities in the absence of assembly.
***Conclusions***: Sourmash ‘gather’ functionality can be used for strain level taxonomic classification of complex microbial communities in the absence of assembly.
