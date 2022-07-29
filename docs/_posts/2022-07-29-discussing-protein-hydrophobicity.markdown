---
layout: post
title:  "Discussing protein hydrophobicity"
date:   2022-07-29 09:52:03 +0100
categories: [protein hydrophobicity]
typora-root-url: ../../docs
---

Proteins-water interactions are **complex**. Different regions of protein surfaces have been characterised as hydrophobic/hydrophilic according to very different metrics. 

*To me, it is not clear how these different ideas on hydrophobicity link back to macroscopic phenomena such as surface phase transitions.*

Following a brainstorming discussion with Jennifer McManus, I have collected some relevant points:

- Patchy particles are used to model the phase behaviour of protein assembly, for example, in work by [P. Charbonneau](https://reader.elsevier.com/reader/sd/pii/S0927776515300576?token=17D5209262A942FA6B76F55C60B7616CAE10423E9FED85B9BAD494CAB8CE1843EFD82A7357AEC7B65D9D3205DAFCA973&originRegion=eu-west-1&originCreation=20220729100636). They are tuned empirically, with ad-hoc parameters and patches to represent hydrophobic effects in implicit solvent calculations. This means, for example, having specific patches with stronger protein-protein interactions. It is not clear to me if there is a consesus on the robustness of this coarse-graining. But it has the undeniable advantage of making protein phase behaviour computationally accessible. 
- An even more simplified picture to gradually blend between the macroscopic notion of surface phase transitions and the patchiness of protein surfaces was proposed by Jennifer: why not explore patterned wall-fluid interactions with tunable length scales? Possible ideas include checkerboards or random stripes. These would, in fact, embed finite-size effects (of the patches/stripes) as a *feature*, exploring the interplay between parallel correlation lengths in the solvent and the sizes of the patterns. This approach has the advantage of being easy to explore in the grand canonical ensemble and (potentially) in 2d classical density functional theory approaches.
- A very curious physical picture (that is apparently popular) emerged from the conversation: it seems that there is a common belief that hydrophobicity is linked to the formation of **clathrate hydrates**, i.e. cages formed by water around hydrophobic molecules. These cages somehow would be longer-lived than other water density fluctuations; they would occur at the surface of the proteins (somehow), and they would lead to the formation of density difference at the surface (with a film of low density close to the surface and maybe some higher density away from it when the cage would exist). A useful article by [Parui and Jana](https://pubs.acs.org/doi/10.1021/acs.jpcb.8b11172) seems to link confinement to the appearance of these structure.
  

