# **Materials and Methods**
<hr style="height:3px;border:none;color:#808080;background-color:#808080;" />

##1.Seamless cloning MasterMix constructs plasmid

<div style="text-align: justify">

###1.1  DNA manipulation. 
PCR was performed with 2×Taq PCR MasterMix (Solarbio, Beijing, China). Plasmid DNA was isolated with the TIANprep Mini Plasmid Kit (TIANGEN, Bejing, China). DNA fragments were purifified from agarose gels by using the Universal DNA Purufucation Kit (TIANGEN, Bejing, China) or the Monarch DNA Gel Extraction Kit (NEB). DNA sequencing and primer synthesis were carried out by Sangon Biotech (Shanghai, China). 

###1.2  Plasmid construction. 
a.The plasmids and primers used in this study are listed in the supplemental material. 

b.To construct pTarget-*luxAB*, the coding regions of *luxAB*, p15A, and AmpR are amplifified from the genome of *Fg-1*, a plasmid from 2021OUC-China iGEM and Cloned UpB_4A3m with three different primer pairs luxAB-F/luxAB-R, p15A-R/p15A-F, AmpR-R/AmpR-F, respectively. The J23119 promoter is added to PCR products of luxAB by primersluxAB-F and J23119R, resulting in J&luxAB. Oligonucleotides are designed to contribute flanking homologous regions to adjacent DNA fragments of 20-25bp in length, resulting in p15A-homo and AmpR-Homo.

c.A new pEvolvR plasmid expressing enCas9-PolI3M-TBD with gRNA targeting *luxAB* is constructed. Three fragments pEA, pEB and pEC with flanking homologous regions to adjacent DNA fragments of 20-25bp are amplifified from pEvolvR-enCas9-PolI3M-TBD with primer pairs pEA-R/pEA-F, pEB-R/pEB-F, pEC-R/pEC-F, respectively. Double-stranded gRNA is gained after DNA annealing, and it is modified by the promoter with the primer pair——. Similarly, then homologous regions are added to produce J&gRNA-Homo.

d.Two plasmids were both constructed using the Seamless cloning Master Mix provided by Sangon Biotech (Shanghi, China). The plasmids pTarget-luxAB and pEvolvR were cotransformed into E. coli strainDH5α, following the specification steps provided.

##2.Structural forecasting

<div style="text-align: justify">

The nucleotide sequences of gene *luxa* and *luxb* of *fg-1* were translated into amino acid sequences from the first promoter. The structures of both *luxa* and *luxb* protein were predicted by [phyre2](http://www.sbg.bio.ic.ac.uk/phyre2/html/page.cgi?id=index) through homology modeling method. Futher analysis of protein structure including the alignment and sites labeling were accomplished by PyMol.

##3.Fluctuation Test

<div style="text-align: justify">

###3.1.Optimize the scale of training
- Start LB cultures of each E. coli strain and grow culturesovernight at 37°C with orbital shaking at 170 rpm.
- Prepare selective media.
- Dilute the bacteria until the culturedoes not produce colonies on the resistance plate.
- Determine the cell density of theovernight culture as precisely as possible，and thetotal number of cells at this time is N0.
- Depending on the measured bacterialdensity, the overnight culture was diluted to 30 ml with a complete medium withdifferent glucose concentrations (0.1%, 0.05%, 0.01%, 0.005%) so that each 30 mlsolution contained a total of 100,000 cells.
- Measure the cell density of the fourconditions to determine dilution.
- Divided into two 96-well plates (48holes per condition), each with 30ul.
- Incubate two plates (37℃) at the right temperature and do not shake.
- Obtain cell density for ten of the 48holes under each condition to ensure that cell counts vary with glucoseconcentration.
- The remaining holes add 70ul distilledwater to the 30ul culture and mix well before applying the plate to prevent thebottom residue. The coated plate remains dry.
- Calculate the number of colonies ofzero-level events and find an appropriate proportion of zero-level events (unmutated plates/total plates between 10% and 80%)

###3.2.Fluctuation test
- Overnight culture the bacteria liquid.
- Break up the bacteria liquid and measurecell density.
- Dilute the bacteria into a fullycultured solution at the selected glucose concentration.

###3.3.Apply a separate strain
- Confirm the dilution multiple, thenremove a certain volume of the bacteria fluid from the diluted bacteria to coatthe common medium, and then count the colonies (which can be used as theinitial number of cells in each hole).
- Add the diluted bacteria to 4 96-wellplates.
- Two of the 96-well plates were cultured,and the other two were coated in the same selected medium, where only mutatedbacteria could grow, and then count the colonies (the number of bacteria thathave mutated- “a”)
- After the culture of the two 96-wellplates, ten of the holes were extracted to measure the cultured bacterialdensity, and the total number of cultured bacteria (Nf) wascalculated. Then the ten holes of bacteria liquid coated into a completemedium, calculate the number of colonies, at this time the number of coloniesis the actual number of active bacteria (b), so as to obtain thesurvival rate of bacteria viability.
- Spread all remaining bacteria into thesame selected medium and count (number of mutant cells- “c”).

###3.4.Data analysis: 
Calculatemutation rates:

<img src="https://user-images.githubusercontent.com/91862733/136960017-409cda6c-779f-4798-bdd7-508933899141.PNG" width = "100">
