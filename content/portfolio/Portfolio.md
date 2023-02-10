---
enableToc: true
---

## Past Data Analyses
> These are mostly from the genetics lab I work at

---
### Spheroid Analysis
![[notes/images/inner_outer_seg.gif]]
> Example plot from one of my EDAs

Spheroids are 3D cultures that mimic tissues and micro tumors better than the 2D cultures we see in Petri dishes for a variety of reasons. When extending biological circuits from the 2D to the more realistic 3D, the morphology of the cells could affect things like protein production. Protein synthesis is an inherently stochastic process, so when creating biological circuits quantifying a measure of [noise](https://en.wikipedia.org/wiki/Cellular_noise) in the system is quite useful. This is extending the 2D [analysis](https://academic.oup.com/nar/article/48/16/9406/5893975?login=false)  to spheroids. You can find out more in my [slides](https://github.com/degtrdg/spheroid-analysis/tree/main/presentations).

Links:
- [Github](https://github.com/degtrdg/spheroid-analysis/) 
---
### Physically Unclonable Function (PUF) Pipeline and Analysis

PUFs are a type of fingerprint that is introduced in manufacturing to show the lineage of a device. They are mainly used in integrated circuits, but they can also be used in other domains like biology. Using CRISPR one can make a PUF to that is impossible to reproduce and can be used to determine the lineage of a cell line ([CRISPR-PUF](https://pubmed.ncbi.nlm.nih.gov/35507652/)). I wrote a pipeline to process the millions of DNA sequencing reads that are used to find a 'distance' between cell lines. If they are the same cell line the distance would be small, and it would be large if the cell lines are different.

Links:
- [Github](https://github.com/degtrdg/puf_analysis) 

---
### Finding Genomic Safe Harbors for CHO

![[notes/images/Pasted image 20230210133224.png]]
> Logic behind pipeline from [slides](https://github.com/degtrdg/genomic-safe-harbors-CHO/tree/main/presentation)

When you edit a cell line with techniques like CRISPR, if you add code without taking into account the function of the regions around it, there might be unintended consequences. There are certain regions that are considered [safe harbors](https://www.sciencedirect.com/science/article/pii/S2667237521002319) where your changes won't interfere with existing functionality. There was code from a paper which defined requirements for safe harbors for the human genome, but we needed it to work for the Chinese Hamster Ovary, so I wrote a Python port than can be extended to any genome. See [slides](https://github.com/degtrdg/genomic-safe-harbors-CHO/tree/main/presentation) for more info.

Links:
- [Github](https://github.com/degtrdg/genomic-safe-harbors-CHO) 

## Projects
---
### Small Molecule Autocomplete RNN
Trained LSTM based RNN to have model efficiently enumerate chemical space. Used BFS to take top few possibilities in the probability distribution, made design decisions to make model more creative and incentivized to give shorter outputs.
<iframe src="https://www.youtube.com/embed/eeZ6qKVMesk?rel=0&modestbranding=1&"
   width="100%"
   height="300em"
   allowfullscreen="allowfullscreen"
></iframe>
Links:
- [Demo](http://dangeorge.me/chem_autocomplete/) 
