# OpenNeRF


### Setup

#### Install NerfStudio

After installing conda (see [here](https://www.google.com](https://docs.anaconda.com/free/miniconda/#quick-command-line-install)) , setup the conda environment:

```
conda create --name nerfstudio -y python=3.8
conda activate nerfstudio
python -m pip install --upgrade pip
```
Install cuda and torch etc
```
conda install nvidia/label/cuda-12.1.1::cuda
pip3 install torch torchvision torchaudio
pip install ninja git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch
```

Install LERF (not needed for this project)
```
git clone https://github.com/kerrj/lerf
cd lerf
python -m pip install -e .
ns-install-cli
```

Install OpenNeRF
```
```


## BibTeX :pray:
```
@inproceedings{engelmann2024opennerf,
  title={{OpenNerf: Open Set 3D Neural Scene Segmentation with Pixel-Wise Features and Rendered Novel Views}},
  author={Engelmann, Francis and Manhardt, Fabian and Niemeyer, Michael and Tateno, Keisuke and Pollefeys, Marc and Tombari, Federico},
  booktitle={The Twelfth International Conference on Learning Representations},
  year={2024}
}
```
