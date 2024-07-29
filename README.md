# nnUNet_MRI_leg_muscles
This repository stores nnUNet weights for lower leg muscle segmentation from mDixon MRI scans.

The nnUNet was trained on 275 mDixon MRI scans obtained on the lower legs of typically developing children and children with cerebral palsy.

Some muscles were grouped together because they were difficult to separate from each other. The network contains the following labels:

1,LG,Lateral gastrocnemius
2,MG,Medial gastrocnemius
3,SOLP,Soleus posterior
4,SOLA,Soleus anterior
5,PL,Plantaris
6,TA,Tibialis anterior
7,TP,Tibialis posterir
8,EEP,Extensor digitorum longus/Extensor hallucis longus/Peroneus tertius
9,PBL,Peroneus brevis/longus
10,POP,Popliteus
11,FDL,Flexor digitorum longus
12,FHL,Flexor hallucis longus
13,TIB,Tibia
14,FIB,Fibula
15,TAL,Talus
16,CAL,Calcaneus

The default nnUNet settings were used for training. The weights are the result of training a 2d model for one fold using all training data available.
