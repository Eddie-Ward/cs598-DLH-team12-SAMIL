Place the `test_studies.csv`, `train_studies.csv`, and `val_studies.csv` files here that denote Split 1 from the original GitHub repo.

Place `TMED2SummaryTable.csv` in the parent `data_info` folder.

```
.
├── data_info/
│   ├── seed0/
│   │   ├── test_studies.csv
│   │   ├── train_studies.csv
│   │   └── val_studies.csv
│   ├── seed1 (not used)
│   ├── seed2 (not used)
│   └── TMED2SummaryTable.csv
├── echo_data/
│   ├── labeled/
│   │   ├── 9s1_0.png
│   │   └── ... put all labeled images here
│   └── unlabeled/
│       ├── 9s1_0.png
│       └── ... put all unlabeled images here
├── model_checkpoints/
│   ├── MOCO_Pretraining_ImageLevel/
│   │   ├── seed0_checkpoint.pt
│   │   └── ... other checkpoints
│   ├── MOCO_Pretraining_StudyLevel/
│   │   └── ... same as above
│   └── view_classifier/
│       └── ... same as above
├── model_runs/
│   ├── ABMIL/
│   │   └── ...checkpoints and csvs will be saved here by default
│   ├── SAMIL-bag-pretrain
│   ├── SAMIL-imgcl
│   └── SAMIL-no-pretrain
├── model_runs_archived/
│   └── ... download any saved checkpoints for use here
└── Notebook.ipynb
```
