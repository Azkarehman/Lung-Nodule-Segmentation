
# Automatic Lung Nodule Detection in CT Scans using Hybrid CNNs Combined with False Positive Reduction Techniques
Lung cancer is one of the major causes of cancer-related deaths due to its aggressive nature and delayed detections at advanced stages. Early detection of lung cancer is very important for the survival of an individual, and is a significant challenging problem. Recently, deep learning based techniques have been proposed which utilizes Maximum intensity projection (MIP) images for the detection of pulmonary nodule. improve the detection of pulmonary nodules in radiological evaluation with computed tomography (CT) scans which is inspired by the clinical methodology of radiologists. It has been proven that MIP images significantly improve the detection and segmentation of nodule. However, such techniques significantly increases the False Positives (FP) rate since veins are also detected as nodules. To adress this issue, we propose a novel hybrid technique which incorporates original scan as well as MIPs to segment the lung nodule from CT scans.  Moreover, we utilized nodule size and nodule texture based technique to detect false positives. Our proposed method achieves global sensitivity of 96.86\% and sensitivity of 95.39\% per scan with 4 false positives per scan for lung nodule detection on the LIDC-IDRI dataset.
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
