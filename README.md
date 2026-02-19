# cross-model-neighborhood-consistency

Tests whether decoder LMs converge to similar internal geometry (Platonic Representation Hypothesis). Uses CKA, Spearman ρ, and k-NN on shared text, with permutation tests and Bonferroni correction.

## Contents

| Path | Description |
|------|-------------|
| notebooks/ | `Cross_Model_Neighborhood_Consistency_fin8.ipynb` — main experiment (6 decoder LMs, WikiText-2, COCO, alignment metrics). |
| results/result10/ | Run outputs: executed notebook, figures, printed results. |
| Final_Project_Pitch.pdf | Project pitch. |
| PAPERS.md | Papers this project builds on. |

## Repo structure

```
cross-model-neighborhood-consistency/
├── README.md
├── PAPERS.md
├── Final_Project_Pitch.pdf
├── notebooks/
│   └── Cross_Model_Neighborhood_Consistency_fin8.ipynb
└── results/
    └── result10/
        └── ... (executed notebook, figures, ASSESSMENT.md)
```

Papers are listed in PAPERS.md (Platonic Representation Hypothesis, structural probes, BERT geometry, semantic subspaces).

Branch workflow: feature → develop → main.
