# DenoisingCT
Deep Learning method for denoising CT images


### Image Augmentation Methodology

The `augment_image` function enhances the diversity of your dataset by applying a series of random transformations to the input CT images, represented as numpy arrays. These augmentations are intended to simulate variations that might occur in real-world scenarios, helping to improve the robustness of models trained on this data. The specific transformations applied are as follows:

- **Random Rotation**: Each image is rotated by a random angle between -20 and +20 degrees along a randomly chosen plane within the image volume. This simulates the variability in patient positioning.

- **Random Flipping**: With a 50% probability, the image is flipped along a randomly chosen axis. This augmentation reflects the unpredictable orientation of scans.

- **Random Translation**: The image is translated along each axis by a random value within the range of -10 to +10 pixels, mimicking slight shifts in the imaging field.

- **Intensity Adjustment**: The intensity of the entire image is adjusted by a random factor between 0.9 and 1.1, and then clipped to maintain the original intensity range of the image. This step accounts for variations in imaging equipment and settings.

Each of these steps introduces variability into the dataset in a controlled manner, enhancing the dataset's utility for training machine learning models without the need for additional data collection.
