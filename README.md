# 🧬 BioMessenger v7.2

**Transform your messages into living molecules.**
**Text ↔ DNA ↔ Protein ↔ Embedded PDB ↔ Message**  
Designed by Muhammad Sohaib Hassan  

---

## Overview

BioMessenger is an advanced computational biology platform that converts ordinary text into DNA sequences, proteins, and synthetic 3D structures. Each message is encoded, translated, and visualized in a biologically inspired way, allowing for interactive molecular exploration and digital art.

**Core Pipeline:**
1. **Text → DNA**: Binary encoding of text into nucleotide sequences.
2. **DNA → Protein**: Translation via the universal codon table.
3. **Protein → 3D Structure**: Synthetic 3D backbone coordinates.
4. **Embedded Messages**: Each PDB contains base64-encoded DNA and a checksum for integrity.

**Built With:**
- Python 3.x
- ipywidgets
- py3Dmol
- Base64 & hashlib for message embedding
- Inspired by Microsoft and Harvard computational biology approaches

---

## Example Workflow

**Input Message:** `Happy New Year`

### Step 1: Text → DNA
CAGGTTCCGGAACCTTAA...

shell
Copy code

### Step 2: DNA → Protein
GLN-VAL-PRO-GLU-THR-LEU...

yaml
Copy code

### Step 3: 3D Structure Visualization

![3D Protein Cartoon](https://via.placeholder.com/500x300.png?text=3D+Protein+Cartoon+Animation)

**Animation:** The protein backbone is represented as dynamic cartoon ribbons. You can rotate, zoom, and explore interactively.

---

## Features

- **Text-to-DNA-to-Protein-to-PDB pipeline**
- **Embedded messages** with checksum verification
- **Interactive 3D visualizations** with py3Dmol
- **Manual folding options**: AlphaFold & ESMFold
- **Beautiful animations** generated from code
- **Educational & research-friendly**

---

## Try It Yourself

- [View PDB Online](https://sciencecodons.com/tools/pdb-file-viewer/)
- [AlphaFold Server](https://alphafold.ebi.ac.uk/)
- [ESMFold Server](https://esmatlas.com/resources?action=fold)

---

## Dependencies

```bash
pip install py3Dmol ipywidgets
