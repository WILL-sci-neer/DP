## Installation

On Ubuntu 20.04 you need to install the following apt packages for mujoco:
```console
sudo apt install -y libosmesa6-dev libgl1-mesa-glx libglfw3 patchelf
```

Clone the repository:
```bash
git clone ...
cd dp_simulation
```

We recommend [Mambaforge](https://github.com/conda-forge/miniforge#mambaforge) instead of the standard anaconda distribution for faster installation: 
```console
mamba env create -f conda_environment.yaml
```

## Training

Determine the dataset path in config/task. For example, for square_image_abs.yaml, determine:
```console
dataset_path: &dataset_path path/to/image_abs.hdf5
```

Activate conda environment and login to [wandb](https://wandb.ai) (if you haven't already):
```console
conda activate dp_sim
wandb login
python train.py --config-name=train_diffusion_transformer_hybrid_workspace.yaml
```
