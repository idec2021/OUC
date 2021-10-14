# <b>Results</b>

##<span style="color:royalblue">**1 Species identification and structural prediction**</span>

We constructed phylogenetic tree of 16S rRNA gene to identified a cyan light-emitting luminescent bacteria strain, *Vibrio FG-1*, which was isolated from the Yellow sea. Close phylogentic relationship between *Allivibrio finisterrensis* and *Vibrio FG-1* was reflected by MEGAX analysis. (Figure 2a) Phylogenetic tree construction of *luxA* has shown that the *luxA* of *Vibrio FG-1* is closely related to *luxA* of *Aliivibrio Salmonicida* and *Aliivibrio Fischeri* (Figure 2b).

<img src="https://user-images.githubusercontent.com/91862733/136695785-72b720b7-b856-49b2-9814-b1e4aa644c71.jpg" width = "600">

**Fig-2a.*FG-1*'s Phylogenetic tree of 16s**<br/>
Phylogenetic tree was constructed based on 16S rRNA genes. *Vibrio FG-1* belonged to *Allivibrio* group with a confidence level of 96% and has a high phylogentic relationship with *Aliivibrio* finisterrensis.

<img src="https://user-images.githubusercontent.com/91862733/136695842-22219e3b-de57-41f8-af5b-1e0ae4c81607.jpg" width = "600">

**Fig-2b.*lux* protein's Phylogenetic tree of *FG-1***<br/>
Phylogenetic tree construction of luxA has shown that Vibrio FG-1 is closely related to Aliivibrio Salmonicida and Aliivibrio Fischeri, with a confidence level of 95%.

We designed primers based on luciferase Lux of sequentially similar species, and amplified *luxA* and *luxB* genes of luciferase. In the predicted structure of the α and β subunit of the luciferase we obtained, similarities to the same subunits of *Vibrio harveyi* were observed. Under this circumstance, we hypothesized that this two subunits will combine with each other and form an asymmetrical structure (Figure 3a, b). The Asp113, RHis44, RLys112 and RHis45 at the α subunit we predicted (Figure 3e), which will electro statistically interact with each other after binding to FMN [8], indicates that this α subunit will also bind to FMN. In this luciferase, the FMN binding site at α subunit, Ala75, mutated to Gly (Figure 3c), but considering that this situation also exists in some bacterial luciferase [9], we could not confirm the influence of this substitute of amino acid. In addition, mutations in Cys106 at α subunit may lead to the instability of intermediate 4a,5-dihydro-4a-hydroperoxy flavin [10] and further reduce the enzyme activity. Also, the Substitutions Y151D on the β subunit (Figure 3d) may also lead to reductions in luciferase activity and total quantum yield [8]. Besides, A series of mutations occurred in amino acid residues on Mobile loop -- and F at position 272 was mutated to H, which did not appear in previous studies. Considering that mobile loop is the boundary between the active center and the outside world [10], the mutation of this contact site may lead to the decrease of enzyme activity, which deserves more attention. Furthermore, A series of mutations occurred on the mobile loop of α subunit, including an F272H, which has not been reported before. Given that the mobile loop worked as a boundary between the active center and the solvent [8], the mutation of this contact site may lead to the decrease of enzyme activity and deserves more attention.

<img src="https://user-images.githubusercontent.com/91862733/136696910-e6e25649-6735-4580-a5c4-03db1a234eb8.png" width = "300">

**Fig-3.The structure of the α and β subunit of the luciferase**<br/>
a, b. The asymmetrical dimer formed by this two subunits. c, d .Substitutions of some active site at α and β subunit that may lead to decrease in enzyme activity. e. The Asp113, RHis44, RLys112 and RHis45 at the α subunit, which will interact with each other after binding to FMN.

##<span style="color:royalblue">**2 Construction of  EvolvR system**</span>

We attempt to express luciferase in Escherichia.coli DH5α and directed mutate luciferase by using enCas9-Pol13M-TBD meidated EvolvR system. We construct and transform pTarget plasmid with luciferase gene and pEvolvR plasmid with sgRNA mediated EvolvR system into Escherichia.coli respectively. By observing the phenotype and testing wavelength of luciferase mutants, screening and amplifying, luciferase mutants with desired characteristics will be finally obtained .

2.1 Construction of pTarget 

We amplified luxA and luxB genes from Vibrio FG-1 by PCR, and added J23119 promoter to them. LuxAB fragment, AmpR fragment and P15A ori fragment were assembled by seamless cloning method. Three fragments with equal molar ratio and Seamless cloning MasterMix was added to incubate according to the instructions of seamless cloning kit. About 20bp homologous sequence between each fragment permit the construction of plasmid. Single colony will be screened on plate containing ampicillin, further colony PCR will be used to verified.

2.2 Design of sgRNA

We selected some sgRNA candidates to target luxA gene for directed mutation. sgRNA selection is mainly based on the following points:

- Expression of two gRNAs that nick separate strands at genomic loci separated within 100 bp was lethal, whereas nicking the same strand at this 100-bp distance was not lethal. 

- In this project, we used enCas9, a mutant of spCas9 (H840A). 20BP-NGG-spCas9 was used for Protospacer Adjacent Motif (PAM) when the online software CRISPROR was used to select and design gRNA.

- Avoiding GC levels that are too high (above 80%) or too low (20%).

- Select gRNA with low off-target rate.

- Due to uncertainty of the specific sites that potentially determine the change of luminescence wavelength of luciferase, we anlalyze the conserved domains of α unit of luciferase by MEME.

<img src="https://user-images.githubusercontent.com/91862733/136780048-a6c46ca3-e2eb-441b-a69f-476b807fdfcb.png" width = "700">

**Fig-4.The conserved domain of the amino acid sequence of *luxA* protein**<br/>

a. the comparison of the conserved domain of the amino acid sequence of luxA protein of Vibrio fg-1 with other vibrio luxA. Rectangles with the same color represent the same motif. b. specific amino acid sequences of motif represented by each color rectangle.

According to above several rules, we design the following five gRNA candidates (figure 5a). Due to uncertainty of the specific sites that potentially determine the change of luminescence wavelength of luciferase, we design some gRNA targeting the active sites, and others targeting the conserved region (figure 5b).

<img src="https://user-images.githubusercontent.com/91862733/136781462-c0ed52f0-abfd-4699-8b18-19c563b82587.png" width = "700">

**Fig-5 .sgRNAcandidates**<br/>

The gray bands in the figure represent the conserved regions of *luxA* gene, and the colored lines mark the corresponding active sites of luciferase. We designed five gRNAs targeting luxA gene to mutate luxA individually or simultaneously

2.3 Construction of pEvolvR

We inserted promoter J23119 and gRNA in front of the sgRNA scaffold on the pEvolvR plasmids which were purchased from Addgene website by recombination. Five pEvolvR plasmids were seperately constructed for the five gRNA candidates. After E.coli was introduced, the expression of enCas9-Pol13M-TBD was induced by dehydrating tetracycline.

##<span style="color:royalblue">**3 Fluctuation analysis assay**</span>

To sensitively quantify the mutation rate, so as to verify that the mutagenesis is created by EvolvR system instead of higher basic mutation rates, we designed a Fluctuation analysis to verify. In order to optimize the culture scale, different glucose concentrations were applied to control the number of cell divisions when the culture reached saturation. Based on the colony number of gentamicin-sulfate resistant LB plate, the plate has no colony when the dilution ratio is 10-6. At this time, OD600 = 0.05 means colony number is 5106 CFU / ml (N0). After diluting to 106 CFU / 30ml, the plate is added to the LB liquid medium with different glucose concentration and coated on the complete LB medium. According to the experimental steps in Methods, when glucose concentration was 0.1%, 0.05%, 0.01% and 0.005%, the proportion of unmutated plates and total plates was 44.7%, 30.6%, 89% and 64.4% respectively. P0 method (Poisson distribution) requires that the percentage of culture medium (p0) without mutants should be between 10% and 80%, so 0.01% LB liquid culture medium with glucose concentration was selected. To calculate the viability and the mutation rate of bacterial according to the formula in Fig-7, we need to calculate the number of bacteria that have mutated (*a*), the total number of bacteria after culture (*Nf* ) and the actual number of viable bacteria (*b*) .

<img src="https://user-images.githubusercontent.com/91862733/136783340-7bccaefa-8b41-4b50-a0f1-d6a4cf41ea96.png" width = "200">

**Fig-6. The formula of fluctuation test**<br/>

The colony number (*a*) is 1.3 CFU per plate. After incubation for one day in the 96-well plate, OD600 = 0.0699, meaning total number of bacteria Nf = 2105 CFU. The actual number of viable bacteria coated in the complete culture medium(*b*) is 322.5 CFU per plate, and the viability of bacterial was calculated (viability = 0.0016). The number of mutated cells (c = 28.64 CFU) was obtained when they were coated in selective medium. Therefore, （zero-level events）p0 = 0.99986. （The mutation rate ）u =  4.38×10^-7. The original mutation rate is high, and the analysis results are inaccurate due to fewer samples and fewer repeated experiments.

##<span style="color:royalblue">**4 Multi-gRNAs**</span>

In industrial production, the desired product or phenotype often requires the expression of multiple genes to be co-regulated, such as changing a metabolic pathway, or try to study complex gene regulatory networks or polygenic diseases. The addition of multiple gRNAs to the EvolvR system will enhance the utility of the system. If EvolvR can target multiple loci of a family of genes and simultaneously direct the evolution of a family of genes, it has the potential to complete the co-directed evolution of an entire metabolic pathway or family of genes in a short period of time. EvolvR can increase the overall length of the mutation window by targeting mutations at different loci of the same gene, and could even customize the length of the mutation window by selecting the locus and number of gRNAs. In previous researches, the EvolvR system has been proved to make simultaneous diversification of genomic loci through co-expression of multiple gRNAs . The EvolvR system allows multiple gRNAs to simultaneously target two genes for targeted mutations and screen for mutants with two target phenotypes. However, studies have indicated that if multiple gRNAs were expressed at the same time, those repeated DNA sequences lead to increased difficulty in plasmid assembly and decreased genetic stability, especially in organisms with frequent homologous recombination . Alexander C et al. designed and screened a series of non-repeating sequence toolbox to help build multiple sgRNA Arrays targeting different loci . The toolkits consist of a sequence non-repeating series of promoters and spacers, and a series of non-repeating gRNA scaffolds designed through RNA structure prediction and Monte Carlo optimization, as well as experimental testing. In our design of the gRNA, we attempt to use nonrepetitive extra-long gRNA arrays (ELSA) from the literature to construct a series of gRNA arrays targeting different loci of luciferase genes  . 

<img src="https://user-images.githubusercontent.com/91862733/136788838-e9517692-222f-4204-9fa6-33fade5877a9.png" width = "700">

a. the non-repetitive extra-long sgRNA arrays literature, including promoters, gRNA handles, spacers and terminators. Different combination of these parts can help avoid repetition. b. the circuit of expressing gRNA. c. using some of parts candidates in ELSA library to construct the circuit of co-expressing our 5 gRNA candidates. 






