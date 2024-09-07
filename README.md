# Context-Aware Crowd Counting

This repository contains the implementation of the paper on **"Context-Aware Crowd Counting"**(https://ieeexplore.ieee.org/document/8954153) as part of Deep Learning Course (CO403) at DTU. The model was designed to improve the accuracy of crowd counting by incorporating contextual information, making it more robust against varying crowd densities, scales, and distributions. The work is compared by implementing current state-of-the-art models for crowd counting with the proposed Context-aware architecture. Following are the base models- CSRNet, SPNet, and MCNN.

## Project Overview

Crowd counting is a challenging task in computer vision, often complicated by factors like perspective distortion, scale variation, and occlusion. The context-aware model addresses these challenges by integrating contextual information to enhance counting accuracy.

In this project, we have implemented the **Context-Aware Crowd Counting** model and compared its performance with other popular crowd counting models:

- **SPNet** (Scale Pyramid Network)
- **MCNN** (Multi-column Convolutional Neural Network)
- **CSRNet** (Convolutional Neural Network with Dilated Convolutions)

## Models Implemented

### 1. **Context-Aware Crowd Counting**
The key contributions of this model include:
- Use of contextual information to handle variations in crowd density.
- Robustness to scale variations and occlusions.
- Enhanced performance across different crowd counting datasets.

### 2. **SPNet (Scale Pyramid Network)**
- Uses a scale pyramid architecture to address scale variation in crowd counting.
- Allows multi-scale feature extraction from different image regions.

### 3. **MCNN (Multi-column Convolutional Neural Network)**
- One of the early deep learning approaches for crowd counting.
- Uses multiple convolutional columns with different receptive fields to capture features at different scales.

### 4. **CSRNet (Convolutional Neural Network with Dilated Convolutions)**
- Uses dilated convolutions to increase the receptive field without losing resolution.
- Effective at capturing high-level semantic information for crowd density estimation.

## Datasets Used

The models were trained and evaluated on the **ShanghaiTech A** dataset.

## Results for Comparison
### SPNet
#### Ground-truth
<img width="450" alt="image" src="https://github.com/user-attachments/assets/45f4f049-e32b-48f4-a830-de5bc01132e7">

#### Prediction
<img width="450" alt="image" src="https://github.com/user-attachments/assets/e0cd0ff3-03a5-464a-962c-639756495286">

### CSRNet
#### Ground-truth
<img width="450" alt="image" src="https://github.com/user-attachments/assets/75f63037-309b-449f-b7e3-394519e5ee20">

#### Prediction
<img width="450" alt="image" src="https://github.com/user-attachments/assets/713da846-7b27-43fb-bc7f-fa81b41f0573">

### MCNN
#### Ground-truth
<img width="450" alt="image" src="https://github.com/user-attachments/assets/ab530726-9317-4f62-8793-4e9e3f00eed4">

#### Prediction
<img width="458" alt="image" src="https://github.com/user-attachments/assets/942f943e-c37f-4810-907f-7f14d3173e9d">



| Model                | ShanghaiTech A (MAE) | ShanghaiTech A (Train Loss)|
|----------------------|----------------------|----------------------------| 
| CANet (VGG)          | 91.8**               | 18.38                      |
| SPNet                | 36.98                | 11.51                      |
| MCNN                 | 25.67                | 0.000147                   |  
| CSRNet               | 23.15                | 0.4287                     |

**MAE** - Mean Absolute Error
** Original work achieved MAE of 62. 

## Sample Density Maps

## Installation

Clone the repository and install the required dependencies:
```bash
git clone https://github.com/yourusername/context-aware-crowd-counting.git
cd context-aware-crowd-counting
pip install -r requirements.txt

