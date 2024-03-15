# OpenNeRF


### Setup

#### Install NerfStudio

After installing conda (see [here](https://docs.anaconda.com/free/miniconda/#quick-command-line-install)), setup the conda environment:

```
conda create --name opennerf -y python=3.8
conda activate opennerf
python -m pip install --upgrade pip
```

Install cuda and torch etc
```
conda install nvidia/label/cuda-12.1.1::cuda
conda install pytorch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 pytorch-cuda=12.1 -c pytorch -c nvidia
pip install ninja git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch
```

<!-- conda install -c "nvidia/label/cuda-11.8.0" cuda-toolkit
pip install torch==2.1.2+cu118 torchvision==0.16.2+cu118 --extra-index-url https://download.pytorch.org/whl/cu118
pip install ninja git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch -->


Install OpenNeRF
```
git clone https://github.com/opennerf/opennerf
cd opennerf
python -m pip install -e .
ns-install-cli
```

Running OpenNeRF (see launch.json)

---

Install LERF (not needed for this project)
```
git clone https://github.com/kerrj/lerf
cd lerf
python -m pip install -e .
ns-install-cli
```

Install OpenNeRF
```
pip install git+https://github.com/NVlabs/tiny-cuda-nn/#subdirectory=bindings/torch
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


## File Structure
We recommend the following file structure:

```
├── my_method
│   ├── __init__.py
│   ├── my_config.py
│   ├── custom_pipeline.py [optional]
│   ├── custom_model.py [optional]
│   ├── custom_field.py [optional]
│   ├── custom_datamanger.py [optional]
│   ├── custom_dataparser.py [optional]
│   ├── ...
├── pyproject.toml
```

## Registering with Nerfstudio
Ensure that nerfstudio has been installed according to the [instructions](https://docs.nerf.studio/en/latest/quickstart/installation.html). Clone or fork this repository and run the commands:

```
conda activate nerfstudio
cd nerfstudio-method-template/
pip install -e .
ns-install-cli
```

## Running the new method
This repository creates a new Nerfstudio method named "method-template". To train with it, run the command:
```
ns-train method-template --data [PATH]
```
