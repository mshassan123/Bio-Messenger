# 🧬 BioMessenger

**Text ↔ DNA ↔ Protein ↔ Embedded PDB ↔ Message**  
Designed by Muhammad Sohaib Hassan  

---

## Overview

BioMessenger v7 is a cutting-edge computational biology platform that transforms ordinary text messages into biologically inspired molecules, including DNA sequences, proteins, and interactive 3D structures. This tool bridges computational science and molecular visualization, enabling users to explore their messages as if they were living biomolecules.

Key Features:

- Converts any text message into a DNA sequence using a custom binary encoding system.
- Translates DNA into a protein sequence via the universal codon table.
- Generates a synthetic 3D protein structure in PDB format.
- Embeds the original message and checksum into the PDB for secure and retrievable data.
- Interactive 3D visualization of proteins using Py3Dmol.
- Supports manual exploration on AlphaFold and ESMFold servers.
- Beautiful animations and cartoon-style molecular views.

---

## How it Works

1. **Text → DNA**  
   Each character is encoded into a unique nucleotide pattern, preserving the message in a biologically interpretable format.  

2. **DNA → Protein**  
   DNA sequences are translated to amino acids using standard codons.  

3. **Protein → 3D Structure**  
   Backbone coordinates are generated for interactive visualization.  

### Example: “Happy New Year”

```python
import py3Dmol

# Example protein sequence from the message
protein_seq = "GLN THR THR LEU THR ALA GLU ARG ALA PRO SER ARG THR ALA ALA ARG PRO SER TYR"

# Generate a PDB with basic coordinates
pdb_content = ""
x, y, z = 0.0, 0.0, 0.0
for i, aa in enumerate(protein_seq.split(), start=1):
    pdb_content += f"ATOM  {i:5d}  CA  {aa} A{i:4d}    {x:.3f}{y:.3f}{z:.3f}  1.00 20.00           C\n"
    x += 1.5
    y += 0.5
    z += 0.5
pdb_content += "END"

# Visualize interactively
view = py3Dmol.view(width=600, height=400)
view.addModel(pdb_content, "pdb")
view.setStyle({"cartoon": {"color": "spectrum"}})
view.zoomTo()
view.show()
