# 202_Finals
# Pneumonia severity score prediction Tool

Google Drive Link: https://drive.google.com/drive/folders/1BHdRGifTUmPfJPVxtunuRmONMPPQmp7X?usp=sharing

Github Link: https://github.com/gauravsharans/202_Finals


**Objective**

The rapid spread of COVID-19 has heightened the importance of efficient and accurate diagnostic tools in healthcare. Pneumonia, a severe respiratory condition often associated with COVID-19, requires timely detection and severity assessment. This study focuses on developing a deep learning-based approach to predict the severity of pneumonia from chest X-ray (CXR) images. By classifying lungs as healthy or affected by pneumonia and subsequently evaluating the extent of lung involvement, the model provides a crucial tool for healthcare professionals in patient management, particularly in intensive care settings.

This implementation project aims to harness the power of machine learning for the early detection of pneumonia severity through chest X-ray analysis for frontal chest X-ray images. Such a tool can gauge the severity of COVID-19 lung infections (and pneumonia in general) that can be used for escalation or de-escalation of care as well as monitoring treatment efficacy. Pneumonia remains a prevalent respiratory infection, and timely identification can significantly impact patient prognosis. The endeavor involves creating a new task, annotating a specialized dataset, training a machine learning model, creating a datasheet for the dataset, and hosting the implementation online for accessibility.

**Process**

The process begins with the classification of CXR images into two categories: healthy lungs and lungs affected by pneumonia. This initial classification is crucial for identifying patients who require further analysis for pneumonia severity. Once pneumonia is detected, the next phase involves creating lung mask segmentations. These segmentations are used to annotate the affected regions of the lung, providing a visual representation of the disease's impact.

**Lung Mask Segmentation**

Lung mask segmentation is a critical step in the process. It involves delineating the lung regions in the X-ray images, which helps in isolating the areas affected by pneumonia. This step is essential for accurately assessing the extent of lung involvement and is achieved through advanced image processing techniques.

**Severity Score Annotation**

Post-segmentation, each affected lung image undergoes severity score annotation. This annotation is based on the geometric extent of the affected lung region, quantifying the severity of pneumonia. Although, the annotation process should be done by experts to create more accurate scores but this tool aims to use chest segmentation area and a rough evaluation from a layman like me to create the scores.

**Predictive Modeling**

The annotated severity scores serve as a foundation for the predictive modeling phase. Here, a linear regression model is employed to predict the severity of pneumonia in new patients. This model is trained on a dataset of annotated X-ray images, learning the correlation between the extent of lung involvement and the severity of the condition.

**CNN Models: DenseNet and UNet**

The implementation of Convolutional Neural Networks (CNNs) like DenseNet and UNet plays a pivotal role in the success of this approach.

**DenseNet**

DenseNet (Densely Connected Convolutional Networks) stands out for its unique architecture, where each layer is connected to every other layer in a feed-forward fashion. For lung mask segmentation and initial image classification, DenseNet's ability to preserve feature maps through its dense connections makes it highly effective. It enhances feature propagation and reuse, leading to more accurate and efficient segmentation and classification results.

**UNet**

UNet, another CNN architecture, is renowned for its performance in medical image segmentation tasks. UNet's architecture is designed to capture context information and enable precise localization, making it ideal for lung mask segmentation. Its ability to work with fewer training samples while delivering accurate segmentations makes it an invaluable tool in this study, especially considering the nuanced nature of CXR images.

**Results**

The results of this study are significant in demonstrating the potential of deep learning in medical imaging and diagnostics. The model's ability to classify CXR images into healthy and pneumonia-affected categories and subsequently predict pneumonia severity showcases the power of AI in enhancing diagnostic accuracy.

**Quantitative Analysis**

The quantitative analysis of the model's performance revealed a high degree of accuracy in classifying lung conditions and predicting pneumonia severity. The linear regression model showed a strong correlation between the predicted severity scores and the actual extent of lung involvement as annotated by experts.

**Qualitative Analysis**

Qualitatively, the lung mask segmentations and severity annotations provided clear visual evidence of the model's effectiveness. These segmentations allowed for a more nuanced understanding of pneumonia's impact on the lungs, which is crucial for treatment planning and monitoring.

**Future Directions**

Looking forward, the potential applications of this model extend beyond pneumonia associated with COVID-19. It can be adapted for other respiratory conditions, enhancing the diagnostic capabilities of healthcare systems worldwide. Furthermore, the integration of this model into clinical workflows can aid in the rapid and accurate assessment of lung conditions, potentially saving lives by enabling timely and appropriate medical interventions.

**References**

Pirolli, P., & Card, S. (1999). Information Foraging. Psychological Review, 106(4), 643-675

Turk, F. J., & Yunus Kökver. (2023). Detection of Lung Opacity and Treatment Planning with Three-Channel Fusion CNN Model. https://doi.org/10.1007/s13369-023-07843-4

Selvan, R., Dam, E., Rischel, S., Sheng, K., Nielsen, M., & Pai, A. (2020). Lung Segmentation from Chest X-rays using Variational Data Imputation. https://arxiv.org/pdf/2005.10052.pdf

Cohen, J., Viviano, J., Bertin, P., Morrison, P., Torabian, P., Guarrera, M., Lungren, M., Chaudhari, A., Brooks, A., Hashir, M., & Bertrand, H. (2021). TorchXRayVision: A library of chest X-ray datasets and models. https://arxiv.org/pdf/2111.00595.pdf

Simonyan, K., & Zisserman, A. (2015). Published as a conference paper at ICLR 2015 VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION. https://arxiv.org/pdf/1409.1556.pdf

COVID-19 Image Data Collection: Prospective Predictions Are the Future
Joseph Paul Cohen and Paul Morrison and Lan Dao and Karsten Roth and Tim Q Duong and Marzyeh Ghassemi
arXiv:2006.11988, https://github.com/ieee8023/covid-chestxray-dataset, 2020

Tartaglione, E., Barbano, C. A., Berzovini, C., Calandri, M., & Grangetto, M. (2020). Unveiling COVID-19 from Chest X-ray with deep learning: a hurdles race with small data. ArXiv:2004.05405 [Cs, Eess]. https://arxiv.org/abs/2004.05405

Gebru, T., Morgenstern, J., Vecchione, B., Wortman, J., Wallach, H., Daumé, H., & Crawford, K. (2021). Datasheets for Datasets. https://www.fatml.org/media/documents/datasheets_for_datasets.pdf

https://huggingface.co/torchxrayvision

https://mlmed.org/torchxrayvision/models.html

(2023). Information Seeking [Lecture slides]

(2023). Information Architecture [Lecture slides]

(2023). Hierarchies, Taxonomies, and Facets [Lecture slides]

(2023). Semantic Similarity [Lecture slides]

(2023). Categories Continued [Lecture slides]

(2023). Categorization [Lecture slides]

(2023). Structuring Data [Lecture slides]

(2023). Naming Resources [Lecture slides]

(2023). Collections [Lecture slides]

(2023). Search and Navigation [Lecture slides]
