Drowsiness Detection

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

For CNN:

![CNN_Image](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/f348c8e4-a033-4977-b984-b04ff4b169be)

###Confusion Matrix

![CNN_CM](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/8f075d85-32f4-47c3-acf9-16019c449cc2)

For ResNet50:

![ResNet50](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/ffeb8b4c-0ed3-4973-9fc5-bd2a4b9d7207)

For ResNet50+Regularization:

![ResNet50Reg](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/2b6cf04d-d7ff-42fb-ac73-79e7769c5df4)

For ResNet50+Fine_Tuning:

![ResNetFineTuning](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/a7fb5ea3-f81c-4e43-904a-6f3543c32397)

###Confusion Matrix

![ResNet50FineTuning_CM](https://github.com/saikarthiknaladala/Drowsiness_Detection_Project/assets/144606889/c79067c3-7913-4b4c-8280-e85a58778bd5)
