# **Results**
<hr style="height:3px;border:none;color:#808080;background-color:#808080;" />

## 1. Species identification and structural prediction

We construct phylogenetic tree of 16S rRNA gene to identify a cyan light-emitting luminescent bacteria strain, *Vibrio FG-1*, which was isolated from the Yellow sea. Close phylogentic relationship between *Allivibrio finisterrensis* and *Vibrio FG-1* is reflected by MEGAX analysis(Figure 1). Phylogenetic tree construction of *luxA* has shown that the *luxA* of *Vibrio FG-1* is closely related to *luxA* of *Aliivibrio Salmonicida* and *Aliivibrio Fischeri* (Figure 2).

<img src="https://user-images.githubusercontent.com/91862733/137275203-c489b2fe-6ed8-4a34-8d60-f147add09787.png" width = "400">

<em><strong>Figure 1. Phylogenetic tree of vibrio FG-1 </strong> Phylogenetic tree was constructed based on 16S rRNA genes. *Vibrio FG-1* belonged to *Allivibrio* group with a confidence level of 96% and has a high phylogentic relationship with *Aliivibrio* finisterrensis.</em>

<img src="https://user-images.githubusercontent.com/91862733/137275204-0fbf06fa-3c62-432a-b9ba-f99583d92d2c.png" width = 400">

<em><strong>Figure 2. Phylogenetic tree of α subunit of luciferase</strong>Phylogenetic tree construction of luxA has shown that Vibrio FG-1 is closely related to *Aliivibrio Salmonicida* and *Aliivibrio Fischeri*, with a confidence level of 95%.</em>

We designed primers and amplified *luxA* and *luxB* genes of luciferase. In the predicted structure of the α and β subunit of the luciferase we obtained, similarities to the same subunits of *Vibrio harveyi* were observed. Under this circumstance, we hypothesized that two subunits will combine with each other and form an asymmetrical structure (Figure 3a, b). The Asp113, RHis44, RLys112 and RHis45 at the α subunit we predicted (Figure 3e), which will electrostatic stability interact with each other after binding to FMN [1], indicates that this α subunit will also bind to FMN. In this luciferase, the FMN binding site at α subunit, Ala75, mutated to Gly (Figure 3c), but considering that this situation also exists in some bacterial luciferase [2], we could not confirm the influence of this substitute of amino acid. In addition, mutations in Cys106 at α subunit may lead to the instability of intermediate 4a,5-dihydro-4a-hydroperoxy flavin [3] and further reduce the enzyme activity. Also, the substitutions Y151D on the β subunit (Figure 3d) may also lead to reductions in luciferase activity and total quantum yield [1]. Besides, A series of mutations occurred in amino acid residues on mobile loop， which did not report in previous studies. Considering that mobile loop is the boundary between the active center and the outside world [3], the mutation of contact site probably result in the decrease of enzyme activity.  Furthermore, A series of mutations occurred on the mobile loop of α subunit, including an F272H, which has not been reported before. Given that the mobile loop worked as a boundary between the active center and the solvent [1], the mutation of this contact site may lead to the decrease of enzyme activity and deserves more attention.

<img src="https://user-images.githubusercontent.com/91862733/136696910-e6e25649-6735-4580-a5c4-03db1a234eb8.png" width = "300">

<em><strong>Figure 3. The structure of the α and β subunit of the luciferase</strong>a, b. The asymmetrical dimer formed by α and β subunit. c, d. Substitutions of some active site at α and β subunit that may lead to decrease in enzyme activity. Red structure is FMN. e. The Asp113, RHis44, RLys112 and RHis45 at the α subunit interact with each other after binding to FMN. The structure is predicted phyre2 and labelled by PyMol.</em>

## 2. Construction of  EvolvR system

We attempt to express luciferase in Escherichia coli DH5α and directed evolve luciferase by using enCas9-Pol13M-TBD meidated EvolvR system. We construct and transform pTarget plasmid with luciferase genes *luxA* and *luxB*, as well as pEvolvR plasmid with gRNA mediated EvolvR system into *Escherichia coli*. By observing the phenotype, testing wavelength of luciferase mutants, screening and amplifying, luciferase mutants with desired characteristics will be finally obtained [4].

### *2.1 Construction of pTarget* 

We amplify luxA and luxB genes from Vibrio FG-1 by PCR, and added J23119 promoter to them. DNA fragments *luxAB*, *ampR* and *p15a* ori were assembled by seamless cloning method. About 20bp homologous sequence between each fragment permit the construction of plasmid. Single colony will be screened on plate containing ampicillin, further colony PCR will be used to verified.

### *2.2 Design of sgRNA*

We selected some gRNA candidates to target luxA gene for directed mutation. Our gRNA design is mainly based on the following key points:

- Expression of two gRNAs that nick separate strands at genomic loci separated within 100 bp was lethal, whereas nicking the same strand at this 100-bp distance was not lethal. 

- In this project, we used enCas9, a mutant of Cas9 (H840A). So 20bp-NGG-spCas9 was used for Protospacer Adjacent Motif (PAM) searching when the online software CRISPROR was used to select and design gRNA [5,6].

-  Avoid GC levels that are too high (above 80%) or too low (20%).

- Select gRNA candidates with low off-target rate.

- Due to the uncertainty of which sites will determine the change of luminescence wavelength of luciferase, we analyze the conserved domains of α unit of luciferase by MEME (Figure 4).  Referring the structure and conserved domain prediction to choose the targeting site.

<img src="https://user-images.githubusercontent.com/91862733/136780048-a6c46ca3-e2eb-441b-a69f-476b807fdfcb.png" width ="700">

<em><strong>Figure 4. The conserved domain of the amino acid sequence of luxA protein</strong>a. the comparison of the conserved domain of the amino acid sequence of luxA protein of Vibrio *FG-1* with other *vibrio luxA*. Rectangles with the same color represent the same motif. b. specific amino acid sequences of motif represented by each color rectangle.</em>

According to above several rules, we design the following five gRNA candidates (Figure 5a). Due to uncertainty of the specific sites that potentially determine the change of luminescence wavelength of luciferase, we design some gRNA targeting the key domain, gRNA candidates 1,2,3, and others targeting the conserved region, gRNA candidates 4 and 5 (Figure 5b).

<img src="https://user-images.githubusercontent.com/91862733/136781462-c0ed52f0-abfd-4699-8b18-19c563b82587.png" width = "700">

<em><strong>Figure 5. gRNA candidates targeting sites</strong>a. five gRNAs candidates sequences b. The gray bands in the figure represent the conserved regions(motifs) of luxA gene. The colored lines mark the corresponding active sites of luciferase. </em>

### *2.3 Construction of pEvolvR*

We inserted promoter J23119 and gRNA in front of the gRNA scaffold on the pEvolvR plasmids by recombination. Five pEvolvR plasmids were separately constructed for the five gRNA candidates. After pEvolvR was introduced, the expression of enCas9-Pol13M-TBD was induced by dehydrating tetracycline.

## 3. Fluctuation analysis assay

To sensitively quantify the mutation rate, so as to verify that the mutagenesis is created by EvolvR system instead of the basic mutation rates, we designed a Fluctuation analysis to verify. 
 
In order to optimize the culture scale, different glucose concentrations were applied to control the number of cell divisions when the culture reached saturation. Based on the colony number of gentamicin-sulfate resistant LB plate, the plate has no colony when the dilution ratio is 10-6. At this time, OD600 = 0.05 corresponds to colony number is 5x10^6 CFU / ml (N0). After diluting to 106 CFU / 30ml, the plate is added to the LB liquid medium with different glucose concentration and coated on the complete LB medium. According to the experimental steps in Methods, the glucose concentration 0.1%, 0.05%, 0.01% and 0.005%, respectively refer to the ratios of unmutated plates to total plates 44.7%, 30.6%, 89% and 64.4%. P0 method (Poisson distribution) requires that the percentage of culture medium (p0) without mutants should be between 10% and 80%, so 0.01% LB liquid culture medium with glucose concentration was selected. To calculate the viability and the mutation rate of bacteria in formula (Figure 6), we calculate the number of bacteria that have mutated (a), the total number of bacteria after culture (Nf ) and the actual number of viable bacteria (b) [7].

<img src="https://user-images.githubusercontent.com/91862733/136783340-7bccaefa-8b41-4b50-a0f1-d6a4cf41ea96.png" width = "200">

<em><strong>Figure 6.The colony number (a) is 1.3 CFU per plate. After incubation for one day in the 96-well plate, OD600 = 0.0699, meaning total number of bacteria Nf = 2x10^5 CFU. The actual number of viable bacteria coated in the complete culture medium(b) is 322.5 CFU per plate, and the viability of bacterial was calculated (viability=0.0016). The number of mutated cells (c =28.64 CFU) was obtained when they were coated in selective medium. Therefore, (zero-level events)p0 = 0.99986. The mutation rate - u = 4.38x10^-7. The original mutation rate is higher than our expectation, and the analysis results are inaccurate due to fewer samples and fewer repeated experiments. Due to the restriction of time, we have not test the basic mutation rate of  E.coli with EvolvR system. 

## 4. Optimization for Multiple gRNAs construction

In industrial production, the desired product or phenotype often requires the co-regulations of multiple genes, such as regulating the metabolic pathway, studying complex gene regulatory networks or polygenic diseases. Multiple gRNAs-guided EvolvR system is of great application value.  If multiple gRNAs guided EvolvR system is designed to target a series of genes and simultaneously direct evolve them, it has the potential to complete the co-directed evolution of an entire metabolic pathway or family of genes in a short period of time. If multiple gRNA guided EvolvR system used to target the same gene, it will increase the overall length of the mutation window, and could even customize the length of the mutation window by selecting the locus and number of gRNAs. 

EvolvR system has been proved to simultaneously diversify several genomic locus by expressing gRNAs [1]. However, only five gRNAs system was tested in the research, EvolvR system with more gRNAs need further verification. 
 
However, some studies have indicated that if multiple gRNAs were expressed at the same time in CRISPR/Cas9 system, those repeated DNA sequences increase difficulty in plasmid assembly and decrease genetic stability, especially in organisms with frequent homologous recombination [8,9]. The problem also need to be solved in EvolvR system, which is adapted from CRISPR/Cas9 system. Alexander C et al. designed and screened a series of non-repeating sequence toolbox to help build multiple gRNA Arrays targeting different loci [10]. The toolkits consist of a sequence non-repeating series of promoters and spacers, and a series of non-repeating gRNA scaffolds designed through RNA structure prediction and Monte Carlo optimization, as well as experimental testing. In our design of the gRNA, we attempt to use nonrepetitive extra-long gRNA arrays (ELSA) from the literature to construct a series of gRNA arrays targeting different loci of luciferase genes for EvolvR system(Figure 7c) [10]. 

<img src="https://user-images.githubusercontent.com/91862733/136788838-e9517692-222f-4204-9fa6-33fade5877a9.png" width = "700">

<em>Figure 7. Introduction of Nonrepetitive parts of ELSA to develop the EvolvR systema. a. the non-repetitive extra-long sgRNA arrays literature, including promoters, gRNA handles, spacers and terminators. Different combination of these parts can help avoid repetition. b. the circuit of expressing gRNA. c. using some of parts candidates in ELSA library to construct the circuit of co-expressing our 5 gRNA candidates.</em>

# **References** 
[1] Campbell, Zachary T.; Weichsel, Andrzej; Montfort, William R.; Baldwin, Thomas O. (2009). Crystal Structure of the Bacterial Luciferase/Flavin Complex Provides Insight into the Function of the β Subunit. Biochemistry, 48(26), 6085–6094.

[2] Thompson, T. B. (1996). The 1.5-A Resolution Crystal Structure of Bacterial Luciferase in Low Salt Conditions. Journal of Biological Chemistry, 271(36), 21956–21968.

[3] Abu-Soud, H. M., Clark, A. C., Francisco, W. A., Baldwin, T. O., and Raushel, F. M. (1993) Kinetic destabilization of the hydroperoxy flavin intermediate by site-directed modification of the reactive thiol in bacterial luciferase. J. Biol. Chem. 268, 7699–7706.]

[4] Halperin, S.O., Tou, C.J., Wong, E.B. et al. CRISPR-guided DNA polymerases enable diversification of all nucleotides in a tunable window. Nature 560, 248–252 (2018). doi: 10.1038/s41586-018-0384-8

[5] Haeussler, M., Schönig, K., Eckert, H. et al. Evaluation of off-target and on-target scoring algorithms and integration into the guide RNA selection tool CRISPOR. Genome Biol 17, 148 (2016). https://doi.org/10.1186/s13059-016-1012-2

[6] Concordet, Jean-Paul; Haeussler, Maximilian (2018). CRISPOR: intuitive guide selection for CRISPR/Cas9 genome editing experiments and screens. Nucleic Acids Research, (), –. doi:10.1093/nar/gky354

[7] Fluctuation analysis  https://fangman-brewer.genetics.washington.edu/fluctuation.html#optimization

[8] Stapley, J., Feulner, P. G., Johnston, S. E., Santure, A. W. & Smadja, C. M. Variation in recombination frequency and distribution across eukaryotes: patterns and processes. Phil. Trans. R. Soc. B 372, 20160455 (2017).

[9] Vos, M. & Didelot, X. A comparison of homologous recombination rates in bacteria and archaea. ISME J. 3, 199 (2009)

[10] Reis, Alexander C.; Halper, Sean M.; Vezeau, Grace E(2019). Simultaneous repression of multiple bacterial genes using nonrepetitive extra-long sgRNA arrays. Nature Biotechnology, doi:10.1038/s41587-019-0286-9







