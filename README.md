# Bioinfo1_2023

> LIN28A Is a Suppressor of ER-Associated Translation in Embryonic Stem Cells   
https://doi.org/10.1016/j.cell.2012.10.019

## 목표: Figure 2E 재현하기!
![figure2E](https://github.com/gaeunny/Bioinfo1_2023/assets/129571289/2b442b36-6d69-43de-b51a-8fda74763201)

### <논문리뷰>

**EXPERIMENTAL PROCEDURES**

Sequence reads were aligned to mouse genome (mm9 assembly) -> mm39   
https://hgdownload.soe.ucsc.edu/goldenPath/mm39/chromosomes/

* Binding Site Motif Analysis
  * extract neighboring sequences with cut-offs of **0.8 for CRES** and **50 for read depth**
  * The 20 nt long flanking sequences 
  * WebLogo version 3.2 (Crooks et al., 2004) with the default options for RNA sequence analysis
  * Hexamer (-2 to +3)
     * enrichment = log<sub>2</sub>(freq. of binding site / freq. of background )
     * background : from nonredundant subset of RefSeq (longest isoforms)

* Binding Site Secondary Structure Preference Analysis
  * crosslinked bases are centered at zero
  * Watson-Crick (WC) pair co-occurrence frequencies of two positions around LIN28A-binding sites
  * vs. background - randomly permuted sequences generated with ~~positional base probabilities~~ (??)
  * permutation
     * Binding sequences were permuted for 1,000 times 
     * by shuffling all bases in the same position of different sequences ~~-> positional base prob?~~
     * pooled the WC-pair co-occurrence between two positions on each permutation. ~~(pool? average?)~~
  * The enrichment level = log<sub>2</sub> ( observed WC-pair co-occurrence frequency near LIN28A-binding sequences / background )



### < 계획>   
(1) binding site (Guided Mission 3)   
(2) 20 nt long flanking sequence -> WebLogo   
(3) hexamer 순위에서 AAGNHG / AAGNGH (H: A,C,U) 확인하기   
(4) AAGNHG / AAGNGH flanking seq => Watson-Crick (WC) pair co-occurrence matrix (normalized) 구하기   
(5) visualization   

### < 확인사항 >
* Guided Mission에서는 유전자 단위로 했는데.. 전체 genome?
* position만 찾아서 mm39에서 hexamer.. 찾는건가?
* Secondary Structure Preference는 AAGNHG / AAGNGH 이 순서인 것들만 골라서 각각 하면 되는건가?
