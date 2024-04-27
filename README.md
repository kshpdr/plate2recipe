# Plate2Recipe Project

First, install [mamba with Miniforge distribution](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html), a better conda environment manager.

Create new environment, activate and install pytorch:
```
mamba create -n plate2recipe python=3.10
mamba activate plate2recipe
```

If you're using PACE ICE, install pytorch with CUDA support with:
```
mamba install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia -c conda-forge
```

and activate it with:
```
mamba activate plate2recipe
```

Finally, allocate a node with GPU, load CUDA module and run the training script:
```
salloc -N1 --mem-per-gpu=12G -t0:30:00 --gres=gpu:V100:1 --ntasks-per-node=1
module load cuda/12.1.1-6oacj6
python -c "import torch; print('CUDA available:', torch.cuda.is_available())"
```
