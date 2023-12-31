## Driver Drowsiness Detection System
## Testing Demo

https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/7d96cafa-00ce-4b70-9649-2ec0ace2e194



## Dataset

This dataset is just one part of The MRL Eye Dataset, the large-scale dataset of human eye images. It is prepared for classification tasks This dataset contains infrared images in low and high resolution, all captured in various lighting conditions and by different devices. The dataset is suitable for testing several features or trainable classifiers. In order to simplify the comparison of algorithms, the images are divided into several categories, which also makes them suitable for training and testing classifiers.

The full dataset is available here : http://mrl.cs.vsb.cz/eyedataset

Our dataset includes 84,898 images for both closed and open eye categories.

Training images : 59,713

Validation images : 14,928

Testing images : 10,257

Original image size is not fixed here. so we resized the every image to (32,32,3).

Resized (32,32,3) -> smaller image size means less training time !

Dataset has been already balanced,i.e both categories have same number of images. Thus, we shall only look at Accuracy metric.

Key metric to consider model performance -> val_categorical_accuracy

## Training the model


ResNet50 Transfer learning ( Baseline ) : 89.91%

ResNet50 Transfer learning + Regularization : 90.29%

ResNet50 Fine Tuning : 94.25%

Our Custom ConvNEt : 92.24%

Although fine-tuned ResNet50 improved validation accuracy on our dataset, our custom ConvNet still stands as the best performance model.

We test the model on test data too. We used confusion matrix, for evaluating the performance of a machine learning classification model. We got an accuracy of 90.69% & 90.65% for CNN and ResNet50 fine tuning. Both are almost equal. We used here ResNet50 Fine Tuning here. 

## CNN:
![CNN_Image](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/a7cabbf7-15a2-4894-b53f-5d3fc77301b9)

### Confusion Matrix
![CNN](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/2eda205e-1d18-4798-8200-1be6ae3abe8e)

## ResNet50 Transfer Learning:
Transfer learning is a machine learning technique where a model developed for one task is reused as the starting point for a model on a second task. 

![ResNet50](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/880732aa-077e-4126-a025-8a4a54a174f9)

## ResNet50 Transfer Learning + Regularization:
Regularization was added because transfer learning model seems to be overfit. Overfit happens when the model learnt only "training data" by heart.
To fix it we have following options:

1. Reduce network complexity

2. use drop out (more dropout in last layers)

3. Regularise

4. Use batch norms

5. Increase the training dataset size
                              
For our case, I added a dropout layer with the rate 0.5 ( 50% of learning weights will be cut off randomly ! )
![ResNet50Reg](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/a3256223-4460-4d90-823f-972334ba879e)

## ResNet50 Fine Tuning:
Fine-tuning is used when our transfer learning model is still needed to improve.

Fine-tuning is the process of retraining a pre-trained model on a new dataset. 

![ResNetFineTuning](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/946e7eb4-bd8f-4ca1-8d20-6a855b5272df)


### Confusion Matrix
![ResNet50FineTuning_CM](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/49ecc6c7-c80a-4350-839b-10e110b90e4c)

