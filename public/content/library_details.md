# Library Details

## Molecule Identification

These molecules were identified from the Reaxys database by searching for the cyano(hetero)arenes substructure. The total results of this search were limited to substances marked commercially available, MW < 500, and the number of fragments= 1 (to exclude salts). Additional functional groups were excluded: dithiols, carboxylic acids, nitro and derivatives, alkynes, alcohols, oximes/N-oxides, cyanates, isocyanates, isothiocyanates, organometallics, pyridiniums, diazos, hydrazines, azides, and carboxylic acid azides were removed. 

## Conformational Searching & Conformer Selection

Molecular mechanics conformational searches were performed using the OPLS4 force field via Schrödinger MacroModel. Conformation searches were calculated in the gas phase, with a maximum of 10,000 interactions and a convergence threshold of 0.001. A collection of conformers within 21 kJ/mol (5.02 kcal/mol) energy window of the minimum were retained, excluding mirror-image-conformers. Ensembles that contained more than 20 conformers were reduced by atomic root mean square deviation (RMSD)-clustering to the minimum Kelley penalty value and taking the centroids of the resultant clusters.

## DFT Computations

All DFT geometry optimizations and sequent frequency calculations (Gaussian 16, rev C.01) were performed at the B3LYP-D3(BJ)/6-31G(d,p) level of theory. The corresponding geometries were used for a series of single-point energy calculations at the M06-2X/def2-TZVP level of theory. 

From the DFT calculations, global, atomic, and bond-level properties were collected for each conformer using a [Get Properties](https://github.com/SigmanGroup/Get_Properties). 

Atoms in the conserved cyanoarene group were consistently numbered as shown below, and the numbers are referenced in the descriptor names.

<div class="centered-container">
     <img src="content/cyanoarene_atom_numbering.png" alt="Cyanoarene Atom Numbering">
</div>

The dynamic range of properties across the conformational ensemble of a single cyanoarene was summarized by using four condensed measures for each of the properties.

| Descriptor              | Definition                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------|
| Boltz                   | Boltzmann-weighted average of a property from all the conformers in an ensemble (T = 298.15 K)  |
| max                     | highest value of a property given by any conformer in an ensemble                               |
| min                     | lowest value of a property given by any conformer in an ensemble                                |
| low_E                   | value of a property from the lowest energy conformer in the ensemble                            |

## Citation
Dantas, J. A.; Hardy, M. A.; Sigman, M. S. Cyanoarene Descriptor Library. **2024** [https://descriptor-libraries.molssi.org/cyanoarenes](https://descriptor-libraries.molssi.org/cyanoarenes)
