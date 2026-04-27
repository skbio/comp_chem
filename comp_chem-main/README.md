# comp_chem
Python scripts for RDKit-based molecular analysis and cheminformatics

comp_chem

* **01_Basics**: SMILES conversion, drawing, and sanitization.
* **02_Descriptors**: Lipinski rules, LogP, and chemical fingerprints.
* **03_Virtual_Screen**: Similarity searching and library filtering.
* **04_3D_Conformance**: 3D coordinate generation and minimization.
* **data**: Sample `.smi` or `.sdf` files.


🧠 COMPLETE CLASSIFICATION OF RDKit (~200) DESCRIPTORS
1. 🧪 Physicochemical Descriptors

These describe global drug-like properties.

Examples:

MolWt (Molecular weight)
MolLogP (hydrophobicity)
MolMR (molar refractivity)
TPSA (Topological polar surface area)

Meaning:

Solubility
Permeability
Lipophilicity
2. ⚛️ Constitutional (1D) Descriptors

Simple atom/bond counts.

Examples:

NumHDonors
NumHAcceptors
NumRotatableBonds
HeavyAtomCount
NumValenceElectrons
NumRadicalElectrons

Meaning:

Size
Flexibility
Basic composition
3. 🔬 Topological (2D graph-based) Descriptors

Based on molecular graph connectivity.

Examples:

Chi0, Chi1, Chi2, Chi3, Chi4
Kappa1, Kappa2, Kappa3
BertzCT
BalabanJ
HallKierAlpha
WienerIndex (variants)

Meaning:

Shape complexity
Branching
Molecular connectivity
4. 🧬 Ring & Aromaticity Descriptors

Describe cyclic structure.

Examples:

RingCount
NumAliphaticRings
NumAromaticRings
NumSaturatedRings
NumRingAtoms
NumRingBonds

Meaning:

Rigidity
Aromatic stabilization
Structural constraints
5. 🔗 Fragment / Functional Group Descriptors

Count specific structural motifs.

Examples:

Fragments like:
aliphatic OH count
aromatic nitrogens
halogen counts
NumAmideBonds
NumHeteroatoms
NumSaturatedCarbocycles

Meaning:

Reactivity
Binding potential
Toxicity signals
6. ⚡ Electronic / Charge-related Descriptors

Limited in RDKit core but still important.

Examples:

MaxPartialCharge
MinPartialCharge
MaxAbsPartialCharge
MinAbsPartialCharge

Meaning:

Reactivity
Electrostatic interactions
7. 🧩 Surface / Polar Descriptors

Interface-related molecular properties.

Examples:

TPSA (already in physicochemical group but often separated)
LabuteASA (approx surface area)

Meaning:

Binding affinity
Solvent accessibility
8. 🧱 Structural Complexity Descriptors

Describe overall molecular complexity.

Examples:

BertzCT (also topological)
Complexity indices
FractionCSP3 (sp3 character)
Asphericity-like indices (if extended)

Meaning:

Drug-likeness
Synthesis difficulty
9. 🔄 Flexibility Descriptors

Describe molecular motion.

Examples:

NumRotatableBonds
Rotatable bond ratios

Meaning:

Binding entropy
Conformational freedom
