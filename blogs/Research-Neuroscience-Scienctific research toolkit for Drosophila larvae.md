---
layout: page
title: Scienctific research toolkit for Drosophila larvae
---

## Category of research methods
### Gene expression
* **Gal4-UAS system** 

 The GAL4-UAS system is a technique enabling the expression of a gene of choice in a defined spatiotemporal pattern. 
GAL4 is a tran-scription factor from yeast that was adapted for use in Drosophila by Brand and Perrimon. 
In short, when the expression of GAL4 is under the control of a particular enhancer 
(e.g., an enhancer that is activated in all mushroom body neurons), 
the GAL4 line can be used to express any gene of interest in the same pattern by cloning the coding cDNA behind the UAS sequence. 
When both components are present in the same fly, the GAL4 protein that is expressed will bind to the UAS sequence, 
activating the expression of the gene of interest. More recently, it has become possible to more finely control activation of 
GAL4-mediated gene expression via use of the Gal80 protein, which binds GAL4 and inhibits it from binding the UAS sequence.[1]

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
  * **Use of *Shibire***, a temperature-sensitive mutant of the dynamin gene. At permissive temperature, shibire has no affect on neuronal function. However, when shifted to restrictive temperature, endocytosis of vesicles at the synapse is blocked, disrupting the normal release of neurotransmitters at the synapse.
  * **Over-expression of K+ channels, such as Kir2.1, Shaker, or DORK via the UAS-GAL4 system**, which is the most widely used appproach for membrane hyperpolarization.
  * **knocking down or reducing the function of existing Na+ or Ca2+ channels**, which will also result in a net hyperpolarization of the membrane potential.
 * **Activation**
  * **Manipulation of ion channels** Manipulation of ion channels can also be used to activate neurons. Not surprisingly, these are the reciprocal manipulations used to silence neuronal activity. In the first experiments to artificially activate neurons, K+ channel activity was hindered by the expression of dominant-negative proteins (Shaker K+ dominant-negative, Shaw K+ dominant-negative), RNAi-mediated knockdown of K+ channels, or overexpression of Na + channels such as the bacterial- derived voltage-gated Na+ channel NaChBac, resulting in membrane depolarization and hyperexcitation of the neuron. More recently, techniques have been developed which allow neu- rons to be **artificially activated with a degree of temporal control**. This can be accomplished by overexpression of a temperature-responsive cation channel (**TrpA1**, which is activated at elevated temperatures, or **TrpM8**, which is activated at reduced tempera- tures.
  

### Neural manipulation
* **Sparse Predictive Activity through Recombinase Competition (SPARC)**
 
 a generalizable toolkit that can express any effector in precise proportions of post-mitotic cells in Drosophila


#### Reference
1. [The Making and Un-Making of Neuronal Circuits in Drosophila, 2012](https://link.springer.com/book/10.1007/978-1-61779-830-6)
