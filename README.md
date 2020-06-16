# Adversarial Attack on 3D U-Net model: Brain Tumour Segmentation.

### Overview:

In this project, I have tested the robustness of 3D UNet model for medical image segmenation. UNet model has been very succesful for medical image segmentation. Here, we look at its robustness for brain tumour segmenation. The model was trained on the BraTS dataset. BraTS dataset contains MRI images of brain of size (240, 240, 155). For more information visit [here](https://pubmed.ncbi.nlm.nih.gov/25494501/).

### Visualization:

The colors used in GIFs correspond to following:
* Red is edema
* Green is a non-enhancing tumour
* Blue is an enhancing tumour.

# Adversarial Attacks:
Adversarial attacks have been done on patches of size (160, 160, 16) to reduce computational time. In all the methods below, the parameters were as follows:
* Iterations: 10
* Epsilon: 0.2
* Alpha: 0.02

### Iterative Fast Gradient Sign Method (iFGSM):

* Dice Coefficient of prediction before attack: 0.7913155
* Dice Coefficient of prediction after attack: 0.43321887

Ground Truth:

![GIF of Ground Truth for iFGSM](/GIFs/iFGSM/GroundTruth.gif)

Prediction before attack:

![GIF of Ground Truth for iFGSM](/GIFs/iFGSM/PredBeforeAttack.gif)

Prediction after attack:

![GIF of Ground Truth for iFGSM](/GIFs/iFGSM/PredAfterAttack.gif)

### Targeted Iterative Fast Gradient Sign Method (tiFGSM):

* Dice Coefficient of prediction before attack: 0.8463957
* Dice Coefficient of prediction after attack: 0.53347206

Ground Truth:

![GIF of Ground Truth for iFGSM](/GIFs/tiFGSM/GroundTruth.gif)

Prediction before attack:

![GIF of Ground Truth for iFGSM](/GIFs/tiFGSM/PredBeforeAttack.gif)

Prediction after attack:

![GIF of Ground Truth for iFGSM](/GIFs/tiFGSM/PredAfterAttack.gif)

### Carlini and Wagner Attack (CW):

* Dice Coefficient of prediction before attack: 0.840131
* Dice Coefficient of prediction after attack: 0.45113495

Ground Truth:

![GIF of Ground Truth for iFGSM](/GIFs/CW/GroundTruth.gif)

Prediction before attack:

![GIF of Ground Truth for iFGSM](/GIFs/CW/PredBeforeAttack.gif)

Prediction after attack:

![GIF of Ground Truth for iFGSM](/GIFs/CW/PredAfterAttack.gif)

### References:

First half of the code dealing with building model in Notebook.ipynb and util.py has been borrowed from [here](https://www.coursera.org/learn/ai-for-medical-diagnosis).

For more information regarding the algorithms and model used in this project, one can read the papers below:

* U-Net: Convolutional Networks for Biomedical Image Segmentation ([link](https://arxiv.org/abs/1505.04597)).
* Adversarial examples in the physical world ([link](https://arxiv.org/abs/1607.02533)).
* Towards Evaluating the Robustness
of Neural Networks ([link](https://arxiv.org/abs/1608.04644)).
