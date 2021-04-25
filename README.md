# COVID-19-Cough-Detection
An attempt at the Covid-19 Cough Sub-Challenge at the INTERSPEECH 2021 Computational Paralinguistics Challenge (ComParE).
Baseline paper: http://www.compare.openaudio.eu/wp-content/uploads/2021/02/Interspeech_2021_ComParE.pdf
Our attempts,results and improvements - 

1. Augmentation : 

For data-augmentation, the cough data was split based on silence thereby isolating individual cough from an audio input of multiple coughs.
Gaussian noise and Frequency masking applied. Audio shifted for augmentation. 

This improve the Baseline scores as follows:
  a. Feature extraction using opensmile and classification using SVM - 5% increase in UAR (unweighted average recall) in comparison to the baseline.
  b. Feature extraction using opensmile and classification using XGBoost - 2% increase in UAR as compared to non-augmented and SVM classification as mentioned in baseline.
  c. Feature extraction using Deep Spectrum and classification using SVM- 1% increase in UAR in comparison to the baseline.
  
2. Attempt at implementing a BIOMARKER:
   Motivation : https://ieeexplore.ieee.org/document/9208795
   - Cough recording is split into 6 second audio chunks, padded as needed, processed with the MFCC package
   -  Apply poisson mask on each example to mimic muscular degradation during cough.
   

The Repository for the Bsseline paper: https://github.com/EIHW/ComParE2021


