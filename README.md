# Plate2Recipe Project

Clone the repo and create a new environment:

```
conda env create -f environment.yml
conda activate plate2recipe
```

For Mac users, install mamba first, a better conda environment manager:
```
conda install mamba -n base -c conda-forge
```

Create new environment, activate and install pytorch:
```
mamba create -n plate2recipe python=3.10
mamba activate plate2recipe
mamba install pytorch::pytorch torchvision torchaudio -c pytorch
```