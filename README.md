# WQF7009 Assignment 2: XAI on brain MRI data

LRP and Grad-CAM explanations for a VGG16 brain tumour classifier, based on `05_lrp.py` from the DeepFindr xai-series (https://github.com/deepfindr/xai-series).

## Setup
Activate your Python environment, then install the packages:
```
pip install -r requirements.txt
```
For GPU use on Windows, install the CUDA build of PyTorch from https://pytorch.org/get-started/locally/.

## Run
Open `brain_mri_xai.ipynb` and run all cells.
The notebook downloads the dataset (https://github.com/SartajBhuvaji/Brain-Tumor-Classification-DataSet, commit `3ea9f4e`) into `data/brain_mri/training` and `data/brain_mri/testing`.

## Trained model
The results in the report come from the trained model `vgg16_brain_mri.pt` (seed `26062857`).
Download it from the [Releases](https://github.com/TanPH-UM/WQF7009-Assignment-2/releases) page and place it in the repository root.
The notebook then loads it instead of training.

## Train from scratch
Delete or leave out `vgg16_brain_mri.pt`, then run all cells.
The notebook trains a new model and saves it as `vgg16_brain_mri.pt`.
To train a different model, change `SEED` in the first code cell.
A new model gives results that differ from the report, even with the same seed, because GPU training is not fully deterministic.
