# Liver & Lung Tumor Segmentation with Synthetic Data
Project *"Liver & Lung Tumor Segmentation with Synthetic Data"* for the **2024/2025 Neural Networks course**.

This repository reimplements and extends the method proposed by [Hu et al., *Label-Free Liver Tumor Segmentation*, CVPR 2023](https://openaccess.thecvf.com/content/CVPR2023/papers/Hu_Label-Free_Liver_Tumor_Segmentation_CVPR_2023_paper.pdf).  
We tested whether synthetic tumors generated automatically can replace manual annotations for training segmentation models, and extended the pipeline from liver to lung CT scans.


## Overview

- Synthetic liver tumor generation

<img src="assets/liver_tumor.png" width="70%">

- Synthetic lung nodule generation

<img src="assets/lung_nodule.png" width="70%">

---

## Datasets

We used two different datasets in our experiments:

- **Liver tumor generation**  
  For the liver experiments we strictly followed the instructions provided in the official repository of the paper: [Hu et al. – Label-Free Liver Tumor Segmentation (official repo)](https://github.com/MrGiovanni/SyntheticTumors/blob/main/INSTALL.md)

- **Lung nodule generation**  
  For the lung experiments we used the [LNDb dataset](https://doi.org/10.48550/arXiv.1911.08434), which contains **294 annotated CT scans** collected at the Centro Hospitalar e Universitário de São João (Porto, Portugal) between 2016 and 2018.  

You can download processed versions of the datasets, along with the JSON files, here: [Download datasets](https://www.youtube.com/watch?v=dQw4w9WgXcQ)


## Models Weights
The models weights are available here: [Download weights](https://www.youtube.com/watch)

---
## Results

### Liver Experiments

| Model             | Dice (Tumor) | Dice (Liver)| Total mean dice |
|-------------------|--------------|-------------|-----------------|
| U-Net (Synthetic) |     31.06%   |  84.13%     | 57.60%          |

### Lung Experiments

| Model             | Dice (Nodule) | Dice (Lungs)| Total mean dice |
|-------------------|--------------|--------------|-----------------|
| U-Net (Synthetic) |     **.**%   |  **.**%      | **.**%          |


## Conclusions
- Synthetic tumors are competitive with real annotations, showing potential for label-free segmentation.
- Transferring the method from liver to lung is feasible, though more challenging due to anatomy and intensity differences.

- Future work: improve realism of synthetic lesions using generative models.

---

## Repository Structure

```plaintext

├── FINAL_NOTEBOOK.ipynb     # Main Jupyter Notebook with full pipeline
├── assets                   # Images used for README.md
  ├── liver_tumor.png        # Image of a synthetic liver tumor
  └── lung_nodule.png        # Image of a synthetic lung nodule
├── LungNodule_Generation.ipynb  # Lung nodule notebook for reproduciibility
├── LiverTumor_Generation.ipynb  # Liver tumor notebook for reproduciibility
└── README.md              # Project documentation
```
---
## Authors
- [A. Infantino 1922069](https://github.com/alessiainf)
- [A. Di Chiara 1938462](https://github.com/AlessandroDiChiara)
- [F. Fragale 2169937](https://github.com/Bannfrost99)


## Acknowledgments
- We thank Hu et al. for their work on label-free liver tumor segmentation.
- We acknowledge the authors of the LNDb dataset and other public medical datasets.
- Frameworks used: PyTorch, MONAI.


