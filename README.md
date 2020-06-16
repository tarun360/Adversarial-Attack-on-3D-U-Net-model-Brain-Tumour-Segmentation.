# Brain Tumor Segmentation using UNET -  Adversarial Attack.

The BraTS dataset contains MRI images of brain of size (240, 240, 155). For more information visit [here](http://braintumorsegmentation.org/).


### GIFs:

Adversarial attacks have been done on patches of size (160, 160, 16) to reduce computational time. The colors used in GIFs correspond to following:
* Red is edema
* Green is a non-enhancing tumor
* Blue is an enhancing tumor.

### Iterative Fast Gradient Sign Method (iFGSM):

* Dice Coefficient of prediction before attack: 0.7913155
* Dice Coefficient of prediction after attack: 0.43321887

![GIF of Ground Truth for iFGSM](/GIFs/iFGSM/GroundTruth.gif)
![GIF of Ground Truth for iFGSM](/GIFs/iFGSM/PredBeforeAttack.gif)
![GIF of Ground Truth for iFGSM](/GIFs/iFGSM/PredAfterAttack.gif)

### Targeted Iterative Fast Gradient Sign Method (tiFGSM):

* Dice Coefficient of prediction before attack: 0.8463957
* Dice Coefficient of prediction after attack: 0.53347206


![GIF of Ground Truth for iFGSM](/GIFs/tiFGSM/GroundTruth.gif)
![GIF of Ground Truth for iFGSM](/GIFs/tiFGSM/PredBeforeAttack.gif)
![GIF of Ground Truth for iFGSM](/GIFs/tiFGSM/PredAfterAttack.gif)

### Carlini and Wagner Attack (CW):

* Dice Coefficient of prediction before attack: 0.840131
* Dice Coefficient of prediction after attack: 0.45113495


![GIF of Ground Truth for iFGSM](/GIFs/CW/GroundTruth.gif)
![GIF of Ground Truth for iFGSM](/GIFs/CW/PredBeforeAttack.gif)
![GIF of Ground Truth for iFGSM](/GIFs/CW/PredAfterAttack.gif)
