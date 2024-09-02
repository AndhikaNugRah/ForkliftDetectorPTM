Forklift Warning Detection using Pre-Trained ResNet50 Model

Overview

This project utilizes a pre-trained ResNet50 model to detect forklifts in a factory lane and provide warnings. 
The model has been selected after experimenting with other architectures, including VGG16 and InceptionV3, and has achieved a balance between performance and accuracy.

Model Architecture

The pre-trained ResNet50 model is used as the base architecture for this project. The model has been trained on the ImageNet dataset and has achieved state-of-the-art performance on various image classification tasks.

Preprocessing

The input frames are preprocessed using the following steps:

Resizing the frames to (224, 224)
Converting the frames to uint8 data type
Expanding the dimensions of the frames to (1, 224, 224, 3)

Detection

The preprocessed frames are then passed through the ResNet50 model to obtain predictions. The predictions are decoded using the decode_predictions function from the tf.keras.applications.imagenet_utils module.

Warning System

If the detected object is a forklift with a confidence score of 75% or higher, a warning message is displayed on the frame. The warning message includes the label "forklift" and the confidence score.

Experimentation

The following models were experimented with before selecting the ResNet50 model:

VGG16
InceptionV3
The ResNet50 model achieved a balance between performance and accuracy, making it the most suitable choice for this project.

Future Work

To improve the performance of the model, the following steps can be taken:

Collect more data to increase the size of the training set

Experiment with different architectures, such as transfer learning or attention mechanisms

Fine-tune the hyperparameters to optimize the model's performance

Video Source:
https://www.youtube.com/watch?v=w_S7zd37F1c
