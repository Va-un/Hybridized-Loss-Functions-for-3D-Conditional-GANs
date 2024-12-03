# Optimizing 3D Voxel Image Synthesis through Hybrid Loss Functions in Conditional GANs
## Architecture 
![Architectue](Images\MAIN_ARCH_DIAGRAM.png)


## Overview
This project implements advanced loss functions for training conditional Generative Adversarial Networks (cGANs) to synthesize 3D voxel images. By hybridizing adversarial and non-adversarial loss functions, the study improves training stability and the quality of generated voxel structures. Metrics like **AAD** (Average Absolute Difference) and **AVAR** (Average Voxel Agreement Ratio) are used to measure the accuracy and structural coherence of the generated images. The findings provide insights into optimizing cGAN loss functions and open pathways for future research on 3D data processing.

---

## Prerequisites
- **Python**: 3.11
- **Jupyter Notebook**

---

## Dataset
### Download
You can download the dataset form the following link: [SyntheVox3D Dataset](https://www.kaggle.com/datasets/hche8927/synthevox3d) 
Note:If you're using the following dataset, Cite the respective owners.

---

## Workflow

### Option 1: Full Workflow
1. **Download Dataset**  
   - Download the dataset from the provided link or you can use the provided voxel converted images.

2. **Preprocessing**  
   - Open and run `preprocessing.ipynb`.  
   - This notebook prepares the data for model training and evaluation.
   - This notebook primary helps in creating N conditions required by the user.

3. **Model Training**  
   - Open and run `Training.ipynb`.  
   - This notebook trains the model and evaluates its performance.

### Option 2: Quick Evaluation
1. **Direct Evaluation**  
   - Open `Evaluation_metric.ipynb`.  
   - Run the notebook to directly compute metrics and generate images.

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

   1. <strong>Generated Plane Images</strong>
   <table>
     <tr>
       <td><strong>BCE + BCEWithLogitsLoss</strong><br /><img src="Images\Plane\BCE_BceLL_model_state_400.jpg"/></td>
       <td><strong>BCE + MSE (0.6 + 0.4)</strong><br /><img src="Images\Plane\CustomHybridLossBM_model_state_dict_400.jpg" /></td>
     </tr>
     <tr>
       <td><strong>BCE + MSE (0.4 + 0.6)</strong><br /><img src="Images\Plane\CustomHybridLossMB_model_state_dict_400.jpg"  /></td>
       <td><strong>BCE + LOGIT + (BCEWithLogitsLoss+MSE)</strong><br /><img src="Images\Plane\Triple_Loss_model_state_dict_400.jpg" /></td>
     </tr>
   </table>

   2. <strong> Generated Car Images</strong>
   <table>
   <tr>
      <td><strong>BCE + BCEWithLogitsLoss</strong><br /><img src="Images\Car\BCE_BceLL_model_state_400.png"/></td>
      <td><strong>BCE + MSE (0.6 + 0.4)</strong><br /><img src="Images\Car\CustomHybridLossBM_model_state_dict_400.png"  /></td>
   </tr>
   <tr>
      <td><strong>BCE + MSE (0.4 + 0.6)</strong><br /><img src="Images\Car\CustomHybridLossMB_model_state_dict_400.png"  /></td>
      <td><strong>BCE + LOGIT + (BCEWithLogitsLoss+MSE)</strong><br /><img src="Images\Car\Triple_Loss_model_state_dict_400.png" /></td>
   </tr>
   </table>



- <p>You can access the model by clicking on the respective model</p>
### Table 1: Loss Function Evaluation for Plane Dataset
   
| SL NO. | Loss Function Weights                   | AAD    | AVAR   |
|--------|-----------------------------------------|--------|--------|
| 1      | [BCE + BCEWithLogitsLoss (0.7 + 0.3)](Models/Plane/BCE_BLL_model_state_dict_400.pth)     | 0.1346 | 0.8654 |
| 2      | [BCE + MSE (0.4 + 0.6)](Models/Plane/CustomHybridLossMB_model_state_dict_400.pth)                | 0.2579 | 0.7121 |
| 3      | [BCE + MSE (0.6 + 0.4)](Models/Plane/CustomHybridLossBM_model_state_dict_400.pth)                   | Not converged | Not converged |
| 4      | [BCE + LOGIT + (BCEWithLogitsLoss+MSE) (0.4 + 0.3 + 0.3) ](Models/Plane/Triple_Loss_model_state_dict_400.pth)  | 0.2582 | 0.7418 |

### Table 2: Loss Function Evaluation for Car Dataset
| SL NO. | Loss Functions Weights                  | AAD    | AVAR   |
|--------|-----------------------------------------|--------|--------|
| 1      | [BCE + BCEWithLogitsLoss (0.7 + 0.3)](Models/Car/BCE_BLL_model_state_dict_400.pth)     | 0.1968 | 0.8032 |
| 2      | [BCE + MSE((0.4 + 0.6))](Models/Car/CustomHybridLossMB_model_state_dict_400.pth)                   | Not converged | Not converged |
| 3      | [BCE + MSE(0.6 + 0.4)](Models/Car/CustomHybridLossBM_model_state_dict_400.pth)                   | Not converged | Not converged |
| 4      | [BCE + LOGIT + (BCEWithLogitsLoss+MSE) ](Models/Car/Triple_Loss_model_state_dict_400.pth) | 0.1630 | 0.8370 |


---

## Contact

**Varun Chindage**  
- Email: [varunchindage@gmail.com](mailto:varunchindage@gmail.com)  
- LinkedIn: [Varun Chindage](https://www.linkedin.com/in/varunchindage)

**Manasvini Puja Iyer**  
- Email: [pujaiyer04@gmail.com](mailto:pujaiyer04@gmail.com)  
- LinkedIn: [Manasvini Puja Iyer](https://www.linkedin.com/in/manasvini-puja-iyer-97aa40231)
