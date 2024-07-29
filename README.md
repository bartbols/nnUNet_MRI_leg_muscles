# nnUNet_MRI_leg_muscles
This repository stores nnUNet weights for lower leg muscle segmentation from mDixon MRI scans.

## Training data
The nnUNet was trained on water-only images of the lower legs of typically developing children (n=197) and children with cerebral palsy (n=78), obtained from 2-point mDixon MRI scans (3T Philips Ingenia CX). The following scan parameters were used:

Sequence	2-point 3D T1-FFE  
TR/TE1/TE2	6.0-6.2/3.5/4.6 ms  
FOV		160×160 mm  
voxel size	1×1×2 mm (recon to 1x1x1 mm)  
flip angle	6°  
Number of slices 290-485  
NSA		2  

## nnUNet settings
The default nnUNet settings were used for training. The weights are the result of training a 2d model for one fold using all training data (n=275).

The network contains the following labels. Note that some muscles were grouped together because they were difficult to separate from each other.

1, Lateral gastrocnemius  
2, Medial gastrocnemius  
3, Soleus (posterior part)  
4, Soleus (anterior part)  
5, Plantaris  
6, Tibialis anterior  
7, Tibialis posterior  
8, Extensor digitorum longus/Extensor hallucis longus/Peroneus tertius  
9, Peroneus brevis/longus  
10, Popliteus  
11, Flexor digitorum longus  
12, Flexor hallucis longus  
13, Tibia  
14, Fibula  
15, Talus  
16, Calcaneus  

## How to use the pretrained model for segmentation of new scans
Using the trained model to segment new scans requires [Version 2 of the nnUNet](https://github.com/MIC-DKFZ/nnUNet) to be installed.
The weights are stored as a ZIP-file created with nnUNet's command [nnUNetv2_export_model_to_zip](https://github.com/MIC-DKFZ/nnUNet/blob/master/documentation/how_to_use_nnunet.md). To export, use the command nnUNetv2_install_pretrained_model_from_zip and follow the instructions on the [nnUNet GitHub page](https://github.com/MIC-DKFZ/nnUNet).

