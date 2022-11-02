
# [MEDS-Net: Self-Distilled Multi-Encoders Network with Bi-Direction Maximum Intensity projections for Lung Nodule Detection](https://arxiv.org/pdf/2211.00003.pdf)
Early detection of lung cancer is an effective way
to improve the survival rate of patients. It is a critical step to
have accurate detection of lung nodules in computed tomography
(CT) images for the diagnosis of lung cancer. However, due to
the heterogeneity of the lung nodules and the complexity of the
surrounding environment, it is a challenge to develop a robust
nodule detection method. Numerous efforts have been made to
develop an efficient Computer-aided detection (CADe) systems,
albeit none compliance with the routine workflow of radiologists
which limits the adaptability of such CADe system. To overcome
this deficiency, in this study we propose a lung nodule detection
scheme which fully incorporates the clinic workflow of radiologists. Particularly, we exploit Bi-Directional Maximum intensity
projection (MIP) images of various thicknesses (i.e., 3, 5 and
10mm) along with 3D patch of CT scan, consisting of 10 adjacent
slices to feed into self distillation based Multi-Encoders Network
(MEDS-Net). The propose architecture first condense 3D patch
input to three channels by using dense block which consists
of dense units which effectively examines the nodule presence
from 2D axial slices. This condensed information, along with
the forward and backward MIP images is fed to three different
encoders to learn the most meaningful representation which is
forwarded into decoded block at various levels. At decoder block,
we employ self distillation mechanism by connecting the distillation block which contains five lung nodule detectors. It helps
to expedite the convergence and improves the learning ability of
proposed architecture. Finally, the propose scheme reduces the
false positives by complementing the main detector with auxiliary
detectors. The proposed scheme has been rigorously evaluated
on 888 scans of LUNA16 dataset and obtained a CPM score of
93.6%. The results demonstrate that incorporating of bi-direction
MIP images enables MEDS-Net to effectively distinguish nodules
from surroundings which helps to achieve the sensitivity of . false
positives per scans with the sensitivity of 91.5% and 92.8% with
the false positive rate of 0.25 and 0.5 per scan, respectively.
## Dataset
 [LIDC-IDRI dataset.](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI)
## Pipeline
The pipeline consists of several steps.


 - Image preprocessing (Lung segmentation using watershed algorithm, resizing and resampling of scans)
 - Segmentation of nodule
 - False positive reduction using
   texture and size based classification

 The segmentation model is shown in figure:
![enter image description here](https://github.com/Azkarehman/Lung-Nodule-Segmentation/blob/main/fig/lung.png)
