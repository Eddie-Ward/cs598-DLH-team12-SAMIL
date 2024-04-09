# CS 598 DLH Team 12 Project: SAMIL

The code and results are based on the original paper "Detecting Heart Disease from Multi-View Ultrasound Images via Supervised Attention Multiple Instance Learning (MLHC'23)"

Link to [original paper](https://static1.squarespace.com/static/59d5ac1780bd5ef9c396eda6/t/64d19be5cdd05e1acf0405e9/1691458534144/ID49_Research+Paper_2023.pdf)

Link to original paper's [Github repo](https://github.com/tufts-ml/SAMIL/tree/main)

## Setup

### Dataset Access

We are using the TMED-2 dataset, specifically the `view_and_diagnosis_labeled_set`.
You will need to apply for access [here](https://tmed.cs.tufts.edu/).

### Folder Structure

Once the dataset has been downloaded you will need the following folder structure, and place the dataset, pretrained checkpoints, etc. accordingly. The pretrained view classifiers and MOCO pretrained checkpoints are available on the original paper's Github repo.

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

### Conda Environment

Use the included environment.yml file to create the conda environment.

```bash
conda env create -f environment.yml
```

### Archived Runs

Available to download here in this [Drive folder](https://drive.google.com/drive/folders/1zy9JNd9pbQJhMTkI03AuhuU7Ntf7dpgc?usp=sharing).

Put the entire folder of the selected run (e.g. SAMIL-70.2) in the `model_runs_archived/` folder.

## Project Citation

@article{huang2023detecting, title={Detecting Heart Disease from Multi-View Ultrasound Images via Supervised Attention Multiple Instance Learning}, author={Huang, Zhe and Wessler, Benjamin S and Hughes, Michael C}, journal={arXiv preprint arXiv:2306.00003}, year={2023} }
