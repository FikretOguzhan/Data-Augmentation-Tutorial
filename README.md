# Data-Augmentation-Tutorial
Pytorch Data Augmentation by using RandomResizedCrop, RandomRotation, ColorJitter, RandomHorizontalFlip, CenterCrop, RandomPerspective, ElasticTransform

## What is Data Augmentation
Data augmentation is a technique used to artificially expand the size and diversity of a dataset by applying various transformations to the original data. The goal is to increase the variability of the data so that the model can learn to be more robust and generalize better to unseen data.

  Data augmentation is widely used in computer vision applications, where the input data is often images or videos. Some of the most common transformations used in image data augmentation include:

- Rotation: rotating the image by a certain angle
- Scaling: increasing or decreasing the size of the image
- Shifting: moving the image horizontally or vertically
- Flipping: flipping the image horizontally or vertically
- Cropping: extracting a smaller region of the image
- Color shifting: changing the brightness, contrast, or hue of the image

Data augmentation is particularly useful when working with limited datasets. By artificially generating more data, it helps to prevent the model from overfitting to the training data and improves its ability to generalize to new, unseen data. Moreover, data augmentation can help to improve the performance of the model by training it on different variations of the data, which can make it more robust to different types of input.

In this study, RandomResizedCrop, RandomRotation, ColorJitter, RandomHorizontalFlip, CenterCrop, RandomPerspective and ElasticTransform are discussed, explained in detail and results are shown with examples.

### Random Resized Crop
transforms.RandomResizedCrop is a data augmentation technique in the PyTorch library used for image transformation. It randomly resizes and crops images in the dataset to different sizes and aspect ratios.

This technique is particularly useful for deep learning models like Convolutional Neural Networks (CNNs) that require input images to have fixed dimensions. RandomResizedCrop allows the use of images with different sizes during training while ensuring that the model receives consistent input size.

The transforms.RandomResizedCrop function randomly resizes the images by a certain scale factor. The scale parameter determines the image scale. For example, the code transforms.RandomResizedCrop(size=(224, 224), scale=(0.08, 1.0)) takes a random crop of any size and aspect ratio from the image and resizes it to a 224x224 size.

This data augmentation technique is commonly used in visual tasks like object detection and classification. Data augmentation helps the model to generalize better and can lead to better results.

### Random Rotation
transforms.RandomRotation is an image transformation technique in the PyTorch library used for data augmentation. This process increases the variation in the dataset by randomly rotating images.

This technique is particularly useful in visual tasks such as image classification or object detection. For example, showing an object from different angles is useful for the model to better recognize and classify it.

The transforms.RandomRotation function rotates the image at a random angle within a specified degree range. For instance, the code transforms.RandomRotation(degrees=30) rotates the image at a random angle between -30 to +30 degrees.

Additionally, the transforms.RandomRotation function can be used to perform rotations in different ways. The resample parameter determines the resampling method used during rotation, and the expand parameter determines whether or not to expand the image after rotation.

This transformation technique helps the model to generalize better, allowing the model to perform better with new examples.

### Color Jitter
transforms.ColorJitter() is an image transformation technique in PyTorch library used for data augmentation. This technique increases variation in the dataset by randomly changing the color of the image.

Brightness: The transforms.ColorJitter() function randomly increases or decreases the brightness of the input image by a random factor. For example, the code transforms.ColorJitter(brightness=0.2) randomly changes the brightness of the image up to 20%.

Contrast: The transforms.ColorJitter() function randomly increases or decreases the contrast of the input image by a random factor. For example, the code transforms.ColorJitter(contrast=0.2) randomly changes the contrast of the image up to 20%.

Saturation: The transforms.ColorJitter() function randomly increases or decreases the saturation of the input image by a random factor. For example, the code transforms.ColorJitter(saturation=0.2) randomly changes the saturation of the image up to 20%.

Hue: The transforms.ColorJitter() function randomly increases or decreases the hue of the input image by a random factor. For example, the code transforms.ColorJitter(hue=0.2) randomly changes the hue of the image up to a factor of 0.2.

This transformation technique helps the model to generalize better and achieve better results. By adding random variations to the dataset during training, the model can better adapt to the variability in real-world data.

### Random Horizontal Flip
transforms.RandomHorizontalFlip() is a image transformation technique in PyTorch library used for data augmentation. This technique randomly flips the input image horizontally (left-right) along the vertical axis.

This transformation technique is particularly useful for tasks such as object recognition. In cases where objects have horizontal symmetry, different images can be generated when the same object is facing different directions. Therefore, by flipping every image horizontally in the dataset, the model is trained with different views of the objects and learns to recognize them better. Additionally, training the model with various image orientations helps it adapt better to real-world scenarios.

### Center Crop
transforms.CenterCrop() is an image transformation technique in PyTorch library used for cropping images. This technique crops the center part of the input image to the desired size.

The main purpose of this transformation technique is to resize images to a specific size while preserving the central part of the image, which usually contains the most important information. For example, in object detection or classification tasks, the object of interest may be located in the center of the image, and this transformation technique can be used to extract the central part of the image for further processing.

transforms.CenterCrop() takes a single argument, the desired output size of the cropped image, and returns an image of the specified size with the central part of the input image.

### Random Perspective
transforms.RandomPerspective() is an image transformation technique in the PyTorch library used for data augmentation. This technique increases the variation in the dataset by randomly warping the image with a perspective transform.

This function can create perspective distortion in images by applying random perspective transformations. This helps the model perform better in real-world scenarios.

transforms.RandomPerspective() preserves the output image size but changes the positions and angles of objects in the image. This function is especially useful for tasks such as object detection.

### Elastic Transform
transforms.ElasticTransform() is an image transformation technique in the PyTorch library used for data augmentation. This technique increases the variation in the dataset by randomly distorting the image using elastic transformations.

Elastic transformations mimic the elastic properties of real-world objects by distorting the image locally. This helps the model learn to recognize objects in various shapes and sizes.

transforms.ElasticTransform() applies random elastic transformations to the input image with a given alpha and sigma value. Alpha controls the magnitude of distortion, while sigma controls the degree of smoothing applied to the displacement field.

By adding elastic transformations to the dataset during training, the model can better handle images that are stretched, compressed, or distorted in other ways, leading to better generalization and improved performance.
