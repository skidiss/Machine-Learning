# Machine-Learning
# Skin Disease Image Classification Notebook

In this notebook, we're making an image classifier which can classify six skin diseases: 
* Acne and Rosacea
* Atopic Dermatitis
* Herpes HPV and other STD
* Poison Ivy and other Contact Diseases
* Psoriasis or Lichen
* Scabies Lyme Disease and other Infestations and Bites

Sometimes these skin deseases look similar and indistinguishable with the regular symptoms such as rashes and redish. 

Can we use deep learning to classify these deseases? What model architecture should we use? How should we train our models? This project hopes to answer these questions/

# Download DATASET
You can choose between this two methods below :
## Google Drive
Google Drive is faster to use

## Google Cloud

# Data Pre-Processing
In data pre-processing we do : 
1.   Image resizing
2.   Image rescaling
3.   Image Augmentation


# MODELLING
* Were using 4 inputs layer with convolutional layer and maxpooling layer with 'relu' activation
* We also add Flatten and Dropout layer to prevent our model from overfitting

# COMPILING 
we using loss 'sparse_categorical_crossentropy' with 'Adam' optimizer and 'accuracy' as the metrics

# Save the Model

To load the trained model into TensorFlow Serving we first need to save it in the [SavedModel](https://www.tensorflow.org/guide/saved_model) format.  This will create a protobuf file in a well-defined directory hierarchy, and will include a version number.  [TensorFlow Serving](https://www.tensorflow.org/tfx/serving/serving_config) allows us to select which version of a model, or "servable" we want to use when we make inference requests.  Each version will be exported to a different sub-directory under the given path.

## TF LITE CONVERT
For the deployment on our Android apps we choose to using TF LITE
