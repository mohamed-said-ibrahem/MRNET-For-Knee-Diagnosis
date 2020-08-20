# MRNET-For-Knee-Diagnosis:
Magnetic resonance imaging (MRI) of the knee is the standard-of-care imaging modality to evaluate knee disorders.
Due to the quantity and detail of images in each knee MRI exam, accurate interpretation of knee MRI is time-intensive and prone to inter and intra-reviewer variability.
An automated system for interpreting knee MRI images has a number of potential applications, such as quickly prioritizing high-risk patients in the radiologist workflow and assisting radiologists in making diagnoses.
Deep learning approaches, in being able to automatically learn layers of features, are well suited for modeling the complex relationships between medical images and their interpretations.
In this study, we present MRNet, a fully automated deep learning model for interpreting knee MRI, and compare the model’s performance to that of general radiologists.

# Background:
Magnetic resonance imaging (MRI) of the knee is the preferred method for diagnosing knee injuries. However, interpretation of knee MRI is time-intensive and
subject to diagnostic error and variability. In this study we developed a deep learning model for detecting general abnormalities and specific diagnoses.

# What we want to achieve from this study?
### 1. We wanted to determine whether a deep learning model could improve the diagnostic accuracy, specificity, or sensitivity of clinical experts, including general radiologists and orthopedic surgeons.
### 2. We wanted to see if a deep learning model could succeed in the clinically important task of detecting disorders in knee magnetic resonance imaging (MRI) scans.

# What did the researchers do and find and what do these findings mean?
1. We experimented with providing model outputs to general radiologists and orthopedic surgeons during interpretation and observed statistically significant
improvement in diagnosis of ACL tears with model assistance.
2. Our deep learning model predicted 3 outcomes for knee MRI exams (anterior cruciate ligament [ACL] tears, meniscal tears, and general abnormalities) in a matter of seconds and with similar performance to that of general radiologists.
3. When externally validated on a dataset from a different institution, the model picked up ACL tears with high discriminative ability.
4. Deep learning has the potential to provide rapid preliminary results following MRI exams and improve access to quality MRI diagnoses in the absence of specialist radiologists.
5. Providing clinical experts with predictions from a deep learning model could improve the quality and consistency of MRI interpretation.

# Dataset
A dataset of 1,370 knee MRI examinations. The dataset contained 1,104 (80.6%)
Abnormal exams, with 319 (23.3%) ACL tears and 508 (37.1%) Meniscal tears.
ACL tears and Meniscal tears occurred concurrently in 194 (38.2%) exams.
The exams were split into a Training set (1,130 exams, 1,088 patients), a Tuning set (120 exams, 111 patients), and a Validation set (120 exams, 113 patients).
To form the Validation and Tuning sets, stratified random sampling was used to ensure that at least 50 positive examples of each label (Abnormal, ACL tear, and Meniscal tear) were present in each set.
All exams from each patient were put in the same split.

# Model performance
For abnormality detection, ACL tear detection, and meniscal tear detection, the model achieved AUCs of 0.937 (95% CI 0.895, 0.980), 0.965 (95% CI 0.938, 0.993), and 0.847 (95% CI 0.780, 0.914), respectively.
The model achieved a sensitivity of 0.879 (95% CI 0.800, 0.929) and accuracy of 0.850 (95% CI 0.775, 0.903), while the general radiologists achieved a sensitivity of 0.905 (95% CI 0.881, 0.924) and accuracy of 0.894 (95% CI 0.871, 0.913).
The model was highly specific for ACL tear detection, achieving a specificity of 0.968.

# Tools Used
Keras, Google Colab.
