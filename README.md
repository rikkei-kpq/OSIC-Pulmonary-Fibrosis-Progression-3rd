# OSIC Pulmonary Fibrosis Progression 3rd place solution

## Introduction

[The competition]() is the challenge of predicting a patient’s severity of decline in lung function based on a CT scan of their lungs. The challenge is to use machine learning techniques to make a prediction with the image, metadata, and baseline FVC as input.

## Training, models and final submission

The final solution is the blend of two models, utilizing CT scan data and tabular data on patient information

1.  Efficient Net model for CT scan image

    Efficent Net fine tuned on CT image was provided by [Wei hao Khoong](https://www.kaggle.com/khoongweihao) as [Data Set](https://www.kaggle.com/khoongweihao/osic-model-weights).

    The final model using for this solution is 'b5' model from efficient net.

2. MLP model on clinical information of patients

    Clinical information from patient was transformed to extract:

    - Sex
    - Smoking status
    - Age
    - Percent of FVC within same category
    - Week compared to baseline CT scan time
    - Change in FVC of patient throughout the monitoring period

    Above information then feeded into MLP that has the embedding layer separates the categorical type data and continuous data.

3. Blending

    Final submission was simple blending between above 2 models result with tuned ratio for FVC and confidence separately.

## How to run

```change-cnn.ipnb``` contains the whole process to provide final submission.
    
