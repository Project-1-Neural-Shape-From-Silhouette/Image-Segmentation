# Image Segmentation Methods

This repository contains Python implementations of various image segmentation techniques. The segmentation methods implemented here include UNet-based segmentation, Otsu's Thresholding, and the GrabCut algorithm. These scripts are useful for extracting regions of interest from images, a common task in computer vision and image analysis applications.

## Contents

1. **segmentation_UNet.py**  
   A script implementing the UNet architecture for image segmentation. UNet is a convolutional neural network designed specifically for biomedical image segmentation. It follows an encoder-decoder structure, making it effective for extracting fine-grained details from images.

2. **segmentation_OtsuThresholding.py**  
   This script demonstrates Otsu's Thresholding method, a popular image segmentation technique that automatically determines the optimal threshold value for an image. It works by minimizing the intra-class variance, which is effective for separating foreground and background in images with bimodal histograms.

3. **segmentation_GrabCut.py**  
   A script using the GrabCut algorithm for image segmentation. GrabCut is an iterative algorithm that combines graph cuts and Gaussian Mixture Models to perform segmentation. It's particularly useful for separating foreground objects from the background in color images.

## Requirements

To run these scripts, you need the following Python packages installed:

- `numpy`
- `opencv-python`
- `tensorflow` (for UNet)
- `matplotlib` (optional, for displaying images)

Install the required packages using pip:

```bash
pip install numpy opencv-python tensorflow matplotlib
```

## Usage

Each script can be executed independently. Make sure you have your images in the correct directories specified within the scripts. Modify the file paths in the scripts as needed to point to your input image directory and desired output directory.

### Running `segmentation_UNet.py`

This script requires a pre-trained UNet model or you need to train it using labeled datasets. Once the model is trained, you can use it to perform segmentation on new images:

```bash
python segmentation_UNet.py
```

### Running `segmentation_OtsuThresholding.py`

This script uses Otsu's method for segmenting images:

```bash
python segmentation_OtsuThresholding.py
```

The output will be binary segmented images saved in the specified output directory.

### Running `segmentation_GrabCut.py`

This script uses the GrabCut algorithm to segment images. It requires an initial bounding box around the object of interest:

```bash
python segmentation_GrabCut.py
```

The results will be saved as segmented images with the background removed.

## Examples

Include example images and their segmented results here to showcase the performance of each method.

## License

Specify the license under which the code is shared, such as MIT License.
