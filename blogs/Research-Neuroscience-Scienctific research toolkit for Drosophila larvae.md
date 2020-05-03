---
layout: page
title: Scienctific research toolkit for Drosophila larvae
---

---
## Category of research methods
### Gene expression
* ***P element techonology*
* **Gal4-UAS binary system** 

 The GAL4-UAS system is a technique enabling the expression of a gene of choice in a defined spatiotemporal pattern. 
GAL4 is a tran-scription factor from yeast that was adapted for use in Drosophila by Brand and Perrimon. 
In short, when the expression of GAL4 is under the control of a particular enhancer 
(e.g., an enhancer that is activated in all mushroom body neurons), 
the GAL4 line can be used to express any gene of interest in the same pattern by cloning the coding cDNA behind the UAS sequence. 
When both components are present in the same fly, the GAL4 protein that is expressed will bind to the UAS sequence, 
activating the expression of the gene of interest. More recently, it has become possible to more finely control activation of 
GAL4-mediated gene expression via use of the Gal80 protein, which binds GAL4 and inhibits it from binding the UAS sequence.[1]
* **LexA/LexAOp**, which can be combined withe the Gal4 system
* **QF/QUAS**
* **Transgenic RNA interference (RNAi)**

  This method is used to knock down the expression of a given gene in a spatiotemporally controlled manner.

### Gene function
* **Rescue or overexpression experiments**
* **RNAi expression / Dominant-negative proteins expression**


### Neural morphology
* **Green/Red fluorescent protein (GFP/RFP)**
* **lacZ**


### Neural signal
* **Calcium imaging**
* **Electrophysiological measurement**


### Neural function
* **Electrophysical recording of neural activity -- classical method**
* **Optogenetics**
 
 Optogenetics is a developing series of techniques in which **light-sensitive channel proteins are expressed neuronally**, allowing either the **activation or silencing of the neuron upon illumination**. In Drosophila , the first use of a light-activated, but technically demanding, genetic system for neuronal activation was with P2X2, an ATP-gated ionotropic purinoceptor. More recently, the most widely used channel for controlled activation of neurons is **channelrhodopsin-2**. This cation channel from the green alga Chlamydomonas is activated by blue light, when in the presence of all-trans retinal which can be administered to the fly via the food, and leads to membrane depolarization. Advantages of channelrhodopsin-2 are that it is a monomer, making it easy to express via the GAL4 system, and its rapid activation and deactivation, which occurs in the millisecond range. While optogenetic tools for neuronal inactivation have also recently been developed, such as the halorhodopsin chloride pump NpHR, these have yet to be used in Drosophila [1].
 
* **Activation/Inhibition/Entire ablation of neurons**, largely determined by the activity of its ion channels.
  * **Silencing**
   1. **Use of *Shibire***, a temperature-sensitive mutant of the dynamin gene. At permissive temperature, shibire has no affect on neuronal function. However, when shifted to restrictive temperature, endocytosis of vesicles at the synapse is blocked, disrupting the normal release of neurotransmitters at the synapse.
   2. **Over-expression of K+ channels, such as Kir2.1, Shaker, or DORK via the UAS-GAL4 system**, which is the most widely used appproach for membrane hyperpolarization.
   3. **knocking down or reducing the function of existing Na+ or Ca2+ channels**, which will also result in a net hyperpolarization of the membrane potential.
  * **Activation**
   1. **Manipulation of ion channels** Manipulation of ion channels can also be used to activate neurons. Not surprisingly, these are the reciprocal manipulations used to silence neuronal activity. In the first experiments to artificially activate neurons, K+ channel activity was hindered by the expression of dominant-negative proteins (Shaker K+ dominant-negative, Shaw K+ dominant-negative), RNAi-mediated knockdown of K+ channels, or overexpression of Na + channels such as the bacterial- derived voltage-gated Na+ channel NaChBac, resulting in membrane depolarization and hyperexcitation of the neuron. More recently, techniques have been developed which allow neu- rons to be **artificially activated with a degree of temporal control**. This can be accomplished by overexpression of a temperature-responsive cation channel (**TrpA1**, which is activated at elevated temperatures, or **TrpM8**, which is activated at reduced tempera- tures.
  

### Neural manipulation
* **Sparse Predictive Activity through Recombinase Competition (SPARC)**
 
 a generalizable toolkit that can express any effector in precise proportions of post-mitotic cells in Drosophila

---
## Resources for learning Drosophila
###   Standard Brain
* **The Standard Brain**, a first effort published by the group of **Martin Heisenberg**. Insight for the brain function requires 1) the **overall architecutre** of the brain; 2) **neural connection**.
* **FlyCircuit**, by **Chiang and colleagues**, a database of tens of thousands of three-dimensional single neuron MARCM clones, which they used to reveal the connections between neuropils and develop a wiring diagram of the entire adult brain.
### Online resources
* **FlyBrain**, an online atlas and database of the Drosophila nervous system: http://flybrain.neurobio.arizona.edu . 
* **FlyCircuit**, a database of Drosophila brain neurons: http://www.flycircuit.tw . 
* **FlyView**, a Drosophila image database: http://flyview.unimuenster.de. 
* **Virtual Fly Brain (VFB)**: “An interactive tool for neurobiolo- gists to explore the detailed neuroanatomy, gene expression, and associated phenotypes of the adult Drosophila melanogaster brain” (verbatim from Web site): http://www.virtualflybrain.org.
### Antibodies
* **DSHB**
* **Wurzburg Hybridoma Library**
### Fly stocks
* **FlyView stock collection**: Enhancer trap lines from the FlyView project can be obtained at University of Muenster, Germany at http://flyview.uni-muenster.de/.
* **Flytrap**, a database of P{GAL4} enhancer traps and their expression in brains :
* **Flytrap**, University of Edinburgh, UK FlyTrap, Yale University, USA
* **GETDB**, a GAL4 enhancer trap database: GETDB, National Institute of Basic Biology, Okazaki, Japan 
* **NIG-FLY**: Fly stocks of the National Institute of Genetics: Stocks for RNA interference experiments may be obtained from the NIG RNAi fly unit at http://www.shigen.nig.ac.jp/fly/nigfly/. 
* **Transgenic RNAi Project**: TRiP at the Harvard Medical School plans to generate 6,250 transgenic RNAi lines targeted to attP2 on chromosome 3. Stocks are distributed through Bloomington Drosophila Stock Center (BDSC), http://www.flyrnai.org/TRiP-HOME.html. 
* **Vienna Drosophila RNAi Center**: The VDRC at IMP/IMBA in Vienna provides two genome-wide transgenic Drosophila RNAi libraries, http://www.vdrc.at. 
* **Janelia Farm Research Campus**: A major effort is under way to generate a collection of 5,000 transgenic lines that drive expression in patterns encompassing all neurons in the brain. This ongoing effort was described in a proof-of-principle paper. These transgenic lines will become available once this collection is complete and characterized.
* **Bloomington Stock Center**: Information about stocks at the BDSC at Indiana University, USA can be obtained at http://flystocks.bio.indiana.edu.
* **Gene Disruption Project**: Information about insertion lines pro- duced by the Gene Disruption Project (GDP), Baylor College of Medicine, Texas, USA can be found at http://flypush.imgen.bcm.tmc.edu/pscreen/.

---
## Important questions
1. **the identification and description of pre-and postsynaptic sites in neural networks**: 
  *  *the use of antibodies that recognize numerous pre- and postsynaptic markers, whether in the axons or dendrites*. However, this requires that the pre-synaptic marker can be expressed cleanly in one neuron and the postsynaptic marker in the other, a prerequisite that is often notobvious.
2. **the description of the networks by means of transsynaptic markers**
  * *wheat germ agglu- tinin conjugated to HRP (WGA-HRP)*, which when expressed or injected into a neuron can be transported via the synapse to the synaptic partner, which also becomes labeled by the marker and thus identified. This technique, however, has only had very limited success in Drosophila.
3. **the selective perturbation of limited numbers of neurons within networks by means of intersectional strategies and novel tools**
  * *GAL4-mediated activation of a transgene*
   1. *With Gal80 --(Gal4 & Gal80 + UAS-transgene == expression)*. For example, one might have a GAL4 line that expresses in the αβ lobes of the mushroom body as well as a few neurons elsewhere in the brain, and a Gal80 line that expresses specifically in all mushroom body neurons. When both the GAL4 and the Gal80 lines are present together with a UAS-transgene, the transgene would only be expressed in those few neurons outside the mushroom body.
   2. *Split-Gal4 --(DBD & AD +UAS-transgene == expression)*. In this system, the DNA-binding domain (DBD) and the activation domain (AD) of GAL4 are split and driven by two separate enhancers. Only in cells that express both the DBD and AD, which then reassociate via a leucine zipper to form an active GAL4 protein, will the UAS-transgene be expressed.
   3. *LexA/LexAOp*, which can be combined together with GAL4 system.
   4. *Qsystem*, which can be combined together with GAL4 system.
4. **in vivo imaging of a functioning brain when performing various tasks**
  * **Functional interfernce**
   1. *MARCM*
   2. *IMAGO*, uses an integrase-based technique to generate knock-out or tagged alleles of a gene of interest conditionally, thus providing more experimental freedom in comparison to MARCM.
   3. *FIAsH-FALI*, is a method allowing proteins expressing a tetracysteine tag to be inhibited upon illumination with light at 488nm when in the presence of the fluorophore FlAsH. Furthermore, it is possible with a relatively straightforward recombineering strategy to tag any protein of interest with a tetracysteine tag (or any other tag of interest), providing a method for the temporal and local inhibition of protein function, enabling its study in a given process.
  * **In vivo imaging**, involves the *direct visualization of neuronal activation by means of a fluorescent signa*. This signal comes from a *genetically encoded calcium indicator* in which calmodulin is linked to GFP that has been circularly permuted, such as cameleons and the G-CaMPs with higher signal-to-noise. Action potentials trigger a rise in intracellular Ca2+, which in turn is bound by the calmodulin of the indicator causing a change in the conformation of the GFP and leading to increased fluorescence.
   1. *cameleons*
   2. *G-CaMPs*
  
---
#### Reference
1. [The Making and Un-Making of Neuronal Circuits in Drosophila, 2012](https://link.springer.com/book/10.1007/978-1-61779-830-6)
