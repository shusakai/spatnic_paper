# SPATNIC paper — main figures & tables

Reproduction notebooks for the **main figures (Fig 1–5)** and **main tables (Table 1–2)** of the
SPATNIC paper. Each notebook:

- inlines the **actual generating code** for that figure/table (copied from the analysis source), and
- embeds the **published result** so it renders without running.

## Contents

| Notebook | Content |
|---|---|
| [`Fig1.ipynb`](Fig1.ipynb) | Cancer/normal classification across primary & metastatic CRC (ROC, confusion, spatial) |
| [`Fig2.ipynb`](Fig2.ipynb) | Accuracy & compute efficiency on Xenium (benchmark, inference time, peak RAM) |
| [`Fig3.ipynb`](Fig3.ipynb) | Zero-shot generalization across platforms (applicability dot-plot, per-modality spatial, scRNA-seq confusion, deconvolution) |
| [`Fig4.ipynb`](Fig4.ipynb) | POU2F3⁺ tuft-like cancer population & relapse (marker heatmap, %tuft-like, fetal signature, Kaplan–Meier) |
| [`Fig5.ipynb`](Fig5.ipynb) | Patient-specific ADC target screening (Visium HD dot-plot) |
| [`Table1.ipynb`](Table1.ipynb) | Datasets (train + test) |
| [`Table2.ipynb`](Table2.ipynb) | Pooled performance |

## Running

The embedded result figures/tables display as-is — no setup needed to **view**.

To **re-run** a notebook, open the first "Configuration" cell and set the path roots to your local
checkout of the main SPATNIC repository and its data:

```python
REPO_ROOT     = Path("/path/to/spatnic")          # the main SPATNIC repo
BACKUP_ROOT   = Path("/path/to/backup")            # training atlas, cohort scores
DATA_ROOT     = Path("/path/to/data")              # GxD concat, refs, model checkpoints
BENCHMARK_DB  = Path("/path/to/benchmark_db")      # spatial modalities + HVG splits
VISIUMHD_ROOT = Path("/path/to/VisiumHD")          # Visium HD ADC track
```

The generating code and prediction/plot caches live in the main SPATNIC repository; this repository
holds only the paper's main figure/table reproduction notebooks.

Cost tags in each notebook: 🟢 light (reads caches) · 🟡 moderate · 🔴 heavy (GPU / multi-GB / long-running).

Non-code panels (schematics and H&E/IHC/Xenium micrographs) are not reproduced and are noted where they occur.
