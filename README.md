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




For ResNet50:



For ResNet50+Regularization:


For ResNet50+Fine_Tuning


