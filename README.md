# Face-Mask-Detection-Tool
This project is the submission for the individual assignment for WIX3001: Soft Computing.

This project trains a model to classify images of single people into ones with face-masks and ones without. Additionaly, if people do not wear masks properly, those images are also classified as people without masks.

The model was also evaluated, and it's loss and accuracy were recorded.  



# Model

CNN model using Keras is used here.  

The model architecture used here is represented in this image:  

![CNN Model Architecture](/repo_images/model_architecture.png)  

**`face_mask_detector.h5`** model is the pre-trained model used for classification, trained and generated from the notebook `(1) Train & Evaluate Model.ipynb`



# Data



# Notebooks

```(1) Train & Evaluate Model.ipynb``` is the notebook used to build, train and test the model for classification.  

```(2) Using Pre-Trained Model.ipynb``` notebook uses the pre-trained model to run individual predictions on any image
