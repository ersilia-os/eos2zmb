# Fit folder: hdac1-inhibition (eos2zmb)

This folder holds the data, code and results needed to rebuild the model. It is stored with
[eosvc](https://github.com/ersilia-os/eosvc) in the **public** bucket; only this README is
tracked in git.

## Data processing

`notebooks/00_data_analysis.ipynb` builds the two training sets in `data/ml_datasets/` from the ChEMBL target 325 pIC50 data in `data/chembl325_ic50.csv`.

## Model building

`src/01_fit_oof.py` builds one LazyQSAR 3.9.3 classifier per task, in slow mode. For each task
it runs five-fold stratified out-of-fold (OOF) cross-validation (seed 42), so every compound
gets one prediction from a model that never saw it. It writes the OOF predictions and metrics to
`results/`, then trains the final model on all compounds into `model/checkpoints/<task>/`.
`src/02_performance.py` plots the OOF ROC curve and the OOF rank of actives and inactives per
task, and collects all metrics in `results/oof_metrics.json`.

```bash
cd src
OMP_NUM_THREADS=1 python 01_fit_oof.py        # or one task: python 01_fit_oof.py pic7
python 02_performance.py
```

| Task | Output column | Training file | Compounds | Actives | OOF AUROC | Descriptors in final model |
|---|---|---|---|---|---|---|
| `pic7` | `hdac1_pic50_7_rank` | `data/ml_datasets/chembl325_pIC50_7.csv` | 9,892 | 3,817 | 0.932 | chemeleon, clamp, morgan |
| `pic8` | `hdac1_pic50_8_rank` | `data/ml_datasets/chembl325_pIC50_8.csv` | 9,892 | 1,210 | 0.939 | chemeleon, clamp, morgan |
