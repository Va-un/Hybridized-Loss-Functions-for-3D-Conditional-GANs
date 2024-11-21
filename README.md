# Hybridized Loss Functions for Enhanced 3D Voxel

## Overview
This project presents a implementation of loss functions in training conditional Generative Adversarial Networks (cGANs) for 3D voxel image synthesis. It explore hybridizing adversarial and non-adversarial losses to enhance training stability and generation quality. Using metrics like AAD and AVAR, the study demonstrates improved accuracy and structural coherence of generated voxel images, providing insights for optimizing cGAN loss functions and future research on 3D data formats.

## Prerequisites
- Python 3.11
- Jupyter Notebook


## Dataset

### Download
Download the dataset from: https://www.kaggle.com/datasets/hche8927/synthevox3d

## Workflow

### Option 1: Full Workflow
1. **Download Dataset**
   - Download the dataset from the provided link
   
2. **Preprocessing**
   - Open and run `preprocessing.ipynb`
   - This notebook prepares the data for model training/evaluation
   
3. **Model Training**
   - Open and run `Training.ipynb`
   - This notebook will train the data for model evaluation

### Option 2: Quick Evaluation
1. **Direct Evaluation**
   - Open `Evaluation_metric.ipynb`
   - Run the notebook to generate results and images

## Models
Pre-trained models are available in the `Models/` folder.

## Generated Outputs
Running the notebooks will generate:
- Evaluation metrics
- Visualizations




## Requirements
Install required packages:
```bash
pip install -r requirements.txt
```

## Contact
**Varun Chindage**
- Email: [varunchindage@gmail.com]
- LinkedIn: [https://www.linkedin.com/in/varunchindage]

**Manasvini Puja Iyer**
- Email: [pujaiyer04@gmail.com]
- LinkedIn: [https://www.linkedin.com/in/manasvini-puja-iyer-97aa40231]




