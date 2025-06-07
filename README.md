# Multi-Dataset Adversarial Attack Generation for Evaluating Deepfake Detection Model Resilience

## Researchers

- **Gabriel Aldrich Calubayan** · [@gabrielcalubayan72](https://github.com/gabrielcalubayan72)  
- **Angelo Joaquin A. Ogerio** · [@ajogerio](https://github.com/ajogerio)

## Overview

This study evaluates the robustness of the [Deepfake vs Real Image Detection ViT Model](https://huggingface.co/dima806/deepfake_vs_real_image_detection) by Dmytro Iakubovskyi against adversarial attacks. This is an extension of the work of Raborar et. al. (2024) where we test the model under three different training and evaluation setups using two different datasets. Using the FGSM L1, L2, and L∞ attacks, we were able to simulate white-box and black-box scenarios and evaluate their effects on the model.

**Full paper available on Overleaf:** [Read here](https://www.overleaf.com/read/frccfhzxqhxd#1a6b80)

---

## 📁 Repository Structure

| File Path | Description |
|-----------|-------------|
| `huggingface_deepfake_vs_real_image_detection/transformer-attack.ipynb` | Generates FGSM L1, L2, and L∞ adversarial examples on the **Deepfake and Real Images dataset** (Karki, n.d.). Also, it simultaneously evaluates model accuracy and stores the results in CSV files. |
| `huggingface_deepfake_vs_real_image_detection/transformer-attack (New Dataset).ipynb` | Same process as above, but uses the **DiFF dataset** (Cheng et al., 2024) for evaluation. |
| `huggingface_deepfake_vs_real_image_detection/HuggingFaceViT (Modified).ipynb` | Trains and evaluates the ViT model on the **Deepfake and Real Images dataset** (Karki, n.d.). |
| `huggingface_deepfake_vs_real_image_detection/HuggingFaceViT (New Dataset).ipynb` | Trains and evaluates the ViT model on the **DiFF dataset** (Cheng et al, 2024). |
| `cs199/huggingfacevit/*.csv` | Stores all the CSV files generated from the files above. |
| `huggingface_deepfake_vs_real_image_detection/analysis.ipynb` | Aggregates results from all CSVs from the huggingfacevit folder and generates visualization graphs for error counts and accuracy. |

