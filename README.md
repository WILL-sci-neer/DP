## Installation

On Ubuntu 20.04 you need to install the following apt packages for mujoco:
```console
sudo apt install -y libosmesa6-dev libgl1-mesa-glx libglfw3 patchelf
```

We recommend Mambaforge instead of the standard anaconda distribution for faster installation: 
```console
$ cd dp_sim
$ mamba env create -f conda_environment.yaml
```

## Training

Set the dataset path in the configuration file located in `diffusion_policy/config/task`. For example, for `square_image_abs.yaml`, set:
```console
dataset_path: &dataset_path path/to/image_abs.hdf5
```

Activate the conda environment and login to wandb (if you haven't already):
```console
conda activate dp_sim
wandb login
```
Run:
```console
python train.py --config-name=train_diffusion_transformer_hybrid_workspace.yaml
```
The success rate can be viewed under `test/mean_score` on the wandb page.

## Training (data augmentation)
```console
$ export PYTHONPATH=$PYTHONPATH:/home/clear/dp_sim/robosuite
$ export PYTHONPATH=$PYTHONPATH:/home/clear/dp_sim/robosuite-task-zoo
$ export PYTHONPATH=$PYTHONPATH:/home/clear/dp_sim/mimicgen
```

