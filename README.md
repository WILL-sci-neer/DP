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

### Running
Activate conda environment and login to [wandb](https://wandb.ai) (if you haven't already):
```console
[diffusion_policy]$ conda activate dp_sim
(robodiff)[diffusion_policy]$ wandb login
```
