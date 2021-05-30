# Face-Mask-Detection-Tool
This project is the submission for the individual assignment for WIX3001: Soft Computing.

This project trains a model to classify images of single people into ones with face-masks and ones without. Additionaly, if people do not wear masks properly, those images are also classified as people without masks.

The model was also evaluated, and it's loss and accuracy were recorded.  



## Model

CNN model using Keras is used here.  

The model architecture used here is represented in this image:  

![CNN Model Architecture](/repo_images/model_architecture.png)  

**`face_mask_detector.h5`** model is the pre-trained model used for classification, trained and generated from the notebook `(1) Train & Evaluate Model.ipynb`



## Data

**`img_data.zip`** is the zip file of images used for training and validating the model.

It's made up of nearly 10K images from [Real-World Masked Face Dataset](https://github.com/X-zhangyang/Real-World-Masked-Face-Dataset), [MaskedFace-Net](https://github.com/cabani/MaskedFace-Net), and some random images from [Google Images](https://www.google.com/imghp).

*Due to data cap and internet connectivity issues, only a portion of the datasets were used. This resulted in only images of disposable surgical masks being used here in the dataset. Additionally, to reduce model complexity and training times, the images have been resized to 70x70.*


The images have been categorized into two classes (or folders):

`with`:  5011 images of people properly wearing disposable surgical face-masks  
`without`:  5003 images of people without any masks, and people improperly wearing face-masks  


The following are sample images from the dataset used here:  

![Input #1](/repo_images/input_1.jpg)  
![Input #2](/repo_images/input_2.jpg)  
![Input #3](/repo_images/input_3.jpg)  



## Notebooks

**```(1) Train & Evaluate Model.ipynb```** is the notebook used to build, train and test the model for classification.  

**```(2) Using Pre-Trained Model.ipynb```** notebook uses the pre-trained model to run individual predictions on any image



## Output

The change in the model's training and validation loss for each epoch is represented in this image:  
![Loss](/repo_images/model_loss.png)  

The change in the model's training and validation accuracy for each epoch is represented in this image:  
![Accuracy](/repo_images/model_accuracy.png)  

The following images are examples showing the model classifying images of people with and without masks:  

![Output #1](/repo_images/output_1.png)  
![Output #2](/repo_images/output_2.png)  
![Output #3](/repo_images/output_3.png)  

As evident from the images, the model works fairly accurate, and works as intended.  

In output example 3, the model also correctly classifies the image of the person not wearing mask properly, as one without masks.
