# Dynetan correlation analyses: (1) path sums across variants + (2) domain bubble plot

This repository contains two Dynetan-based workflows:

1. **Path correlation sums across variants (apo vs ligand)**  
   Computes per-replicate (per-window) **sum of correlations** along a user-defined residue-pair path, across multiple variants.

2. **Domain–domain correlation bubble plot (N-domain vs C-domain)**  
   Computes N×C domain correlation submatrices across replicates and visualizes the **mean correlations** as a bubble plot.

---

## Assumptions (do not ignore)

These scripts assume:

- **Each Dynetan window corresponds to an independent replicate** (e.g., independent trajectories).  
  The statistics (Welch / permutation) treat windows as independent samples.
- **Dynetan nodes correspond to residues** (one node per residue).
- Residue IDs used in `RESIDUE_PAIRS` and domain lists exist in the system and are uniquely mapped in the node selection.

If your windows are time slices from the same trajectory, **p-values are not interpretable** (pseudo-replication).

---

## Requirements

- Python 3.9+
- `dynetan`
- `numpy`, `pandas`, `matplotlib`, `scipy`

Install:

```bash
pip install dynetan numpy pandas matplotlib scipy
