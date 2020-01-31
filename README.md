# Generative Adversarial Networks for Real-robot Missions

# Informations
- Author: [Pin-Wei "David" Chen](http://championway.github.io/)
- Thesis: [Website](https://championway.github.io/thesis/index.html), [PDF](https://championway.github.io/pdf/nctu_thesis_david.pdf)

# Development Environment
- Ubuntu 16.04
- Python3


# Setup
```
$ cd
$ git clone https://github.com/championway/gan_rv_thesis
```

# Semantic Segmentation

## Train Semantic Segmentation on PST900 Dataset
- [Download PST900 Dataset](https://github.com/ShreyasSkandanS/pst900_thermal_rgb)
-- Reference: [PST900: RGB-Thermal Calibration, Dataset and Segmentation Network](https://arxiv.org/abs/1909.10980)


### FCN-Pix2Pix
```
$ cd ~/gan_rv_thesis/Semantic_Segmentation/
$ jupyter-notebook PST_FCN_training.ipynb
```

### UNet-Pix2Pix
```
$ cd ~/gan_rv_thesis/Semantic_Segmentation/
$ jupyter-notebook PST_UNet-Pix2Pix_training.ipynb
```

### FCN-Pix2Pix
```
$ cd ~/gan_rv_thesis/Semantic_Segmentation/
$ jupyter-notebook PST_FCN-Pix2Pix_training.ipynb
```

# Virtual Dataset from Simulation to Real
## Download Sim2Real Dataset
- [Sim2Real Sample Dataset (25.9MB)](https://drive.google.com/open?id=1K8OyugZ_LuVETUveS2hBEwT8ffotn5jq)
- [Sim2Real Dataset (19.8GB)](https://drive.google.com/open?id=1Ylb2aHAvpTKEC0UktbZNYotTZbRH7ZbS)

## Training SSIM-CycleGAN
```
$ cd ~/gan_rv_thesis/Sim2Real/
$ python3 cyclegan_ssim.py
```

## Create GAN Sim2Real Dataset
```
$ cd ~/gan_rv_thesis/Sim2Real/
$ jupyter-notebook Create_GAN_Sim2Real_Dataset.ipynb
```