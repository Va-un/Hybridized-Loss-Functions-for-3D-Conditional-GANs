# Optimizing 3D Voxel Image Synthesis through Hybrid Loss Functions in Conditional GANs

## Overview
This project implements advanced loss functions for training conditional Generative Adversarial Networks (cGANs) to synthesize 3D voxel images. By hybridizing adversarial and non-adversarial loss functions, the study improves training stability and the quality of generated voxel structures. Metrics like **AAD** (Average Absolute Difference) and **AVAR** (Average Voxel Agreement Ratio) are used to measure the accuracy and structural coherence of the generated images. The findings provide insights into optimizing cGAN loss functions and open pathways for future research on 3D data processing.

---

## Prerequisites
- **Python**: 3.11
- **Jupyter Notebook**

---

## Dataset

### Download
Download the dataset from: [SyntheVox3D Dataset](https://www.kaggle.com/datasets/hche8927/synthevox3d)

---

## Workflow

### Option 1: Full Workflow
1. **Download Dataset**  
   - Download the dataset from the provided link.

2. **Preprocessing**  
   - Open and run `preprocessing.ipynb`.  
   - This notebook prepares the data for model training and evaluation.

3. **Model Training**  
   - Open and run `Training.ipynb`.  
   - This notebook trains the model and evaluates its performance.

### Option 2: Quick Evaluation
1. **Direct Evaluation**  
   - Open `Evaluation_metric.ipynb`.  
   - Run the notebook to directly compute metrics and generate images.

---

## Models
Pre-trained models are available in the `Models/` folder.

---

## Generated Outputs
Running the notebooks will generate:
- Evaluation metrics in tabular format.
- Visualizations of generated voxel images.

---

## Requirements
Install the required packages using:
```bash
pip install -r requirements.txt
```

---

## Cautionary Notes
1. **Check File Paths:** Ensure all file paths in the notebooks are correctly set before execution.
2. **Variable Results:** The metrics and visualized outputs may vary with each execution due to the stochastic nature of GAN training and evaluation.

---

## Performance Metrics

### Table 1: Loss Function Evaluation for Plane Dataset
| SL NO. | Loss Function Weights                   | AAD    | AVAR   |
|--------|-----------------------------------------|--------|--------|
| 1      | BCE + BCEWithLogitsLoss (0.7 + 0.3)     | 0.1346 | 0.8654 |
| 2      | BCE + MSE (0.4 + 0.6)                   | 0.2579 | 0.7121 |
| 3      | BCE + MSE (0.6 + 0.4)                   | Not converged | Not converged |
| 4      | BCE + LOGIT + (BCEWithLogitsLoss+MSE) (0.4 + 0.3 + 0.3) | 0.2582 | 0.7418 |

### Table 2: Loss Function Evaluation for Car Dataset
| SL NO. | Loss Functions Weights                  | AAD    | AVAR   |
|--------|-----------------------------------------|--------|--------|
| 1      | BCE + BCEWithLogitsLoss (0.7 + 0.3)     | 0.1968 | 0.8032 |
| 2      | BCE + MSE (0.4 + 0.6)                   | Not converged | Not converged |
| 3      | BCE + MSE (0.6 + 0.4)                   | Not converged | Not converged |
| 4      | BCE + LOGIT + (BCEWithLogitsLoss+MSE) (0.4 + 0.3 + 0.3) | 0.1630 | 0.8370 |

---

## Contact

**Varun Chindage**  
- Email: [varunchindage@gmail.com](mailto:varunchindage@gmail.com)  
- LinkedIn: [Varun Chindage](https://www.linkedin.com/in/varunchindage)

**Manasvini Puja Iyer**  
- Email: [pujaiyer04@gmail.com](mailto:pujaiyer04@gmail.com)  
- LinkedIn: [Manasvini Puja Iyer](https://www.linkedin.com/in/manasvini-puja-iyer-97aa40231)
