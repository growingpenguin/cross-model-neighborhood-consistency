# cross-model-neighborhood-consistency

Tests whether decoder LMs converge to similar internal geometry (Platonic Representation Hypothesis). Uses CKA, Spearman ρ, and k-NN on shared text, with permutation tests and Bonferroni correction.

## Key Findings

- **Training objective dominates geometry**: Models with the same objective show strong alignment (CKA > 0.75) regardless of architecture
- **CLIP pooling matters**: EOS (not CLS) pooling increases alignment from 0.0002 to 0.74
- **Trained probes reveal syntax**: Untrained correlation ρ ≈ 0.02 → trained probes ρ ≈ 0.53
- **Geometry predicts performance**: Linear probe accuracy differences correlate with CKA (ρ = −0.77)

## Contents

| Path | Description |
|------|-------------|
| `notebooks/` | `Cross_Model_Neighborhood_Consistency_fin10.ipynb` — main experiment (10 models, 15 experiments, 6 metrics). |
| `paper/` | NeurIPS-format paper with LaTeX source and figures. |
| `results/result10/` | Run outputs: executed notebook, figures, printed results. |
| `Final_Project_Pitch.pdf` | Project pitch. |
| `PAPERS.md` | Papers this project builds on. |

## Repo structure

```
cross-model-neighborhood-consistency/
├── README.md
├── PAPERS.md
├── Final_Project_Pitch.pdf
├── notebooks/
│   └── Cross_Model_Neighborhood_Consistency_fin10.ipynb
├── paper/
│   ├── paper_neurips.tex
│   ├── neurips_2023.sty
│   └── Figures/
└── results/
    └── result10/
        └── ... (executed notebook, figures)
```

## Reproducibility

- **Hardware**: NVIDIA A100-SXM4-40GB GPU (Google Colab)
- **Batch size**: 16
- **Max sequence length**: 256 tokens
- **Samples per dataset**: 400 sentences
- **Bootstrap iterations**: 100

## Citation

If you use this code, please cite:

```
Ryoo, G. (2026). Geometric Universality is Objective-Contingent: Testing the Platonic 
Representation Hypothesis Across Language and Vision-Language Models.
```

Papers are listed in PAPERS.md (Platonic Representation Hypothesis, structural probes, BERT geometry, semantic subspaces).

Branch workflow: feature → develop → main.
