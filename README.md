# Image Processing with OpenCV and Pillow (PIL)

## Overview
This repository provides a basic introduction to image processing using the OpenCV and Pillow (PIL) libraries in Python. OpenCV is a powerful open-source computer vision library, while Pillow (PIL) is a Python Imaging Library that adds image processing capabilities. This README file will guide you through the setup and usage of these libraries for image manipulation and processing tasks.

Table of Contents
Installation
Getting Started
Image Reading and Display
Image Filtering
Image Transformations
Image Drawing
Image Manipulation
Saving Images
Conclusion
Installation

## Make sure you have Python installed on your system. You can install the required libraries using pip:

pip install opencv-python
pip install pillow

## Getting Started
To begin, import the necessary libraries in your Python script:
import cv2
from PIL import Image, ImageFilter


## Image Reading and Display
Learn how to read and display images using OpenCV and Pillow:

# Using OpenCV
image_opencv = cv2.imread('path/to/image.jpg')
cv2.imshow('Image', image_opencv)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Using Pillow
image_pillow = Image.open('path/to/image.jpg')
image_pillow.show()


# Image Filtering
Explore different image filtering techniques with OpenCV and Pillow:

## Using OpenCV
# Example: Applying Gaussian Blur
blurred_image = cv2.GaussianBlur(image_opencv, (5, 5), 0)

## Using Pillow
# Example: Applying Box Blur
blurred_image_pillow = image_pillow.filter(ImageFilter.BoxBlur(5))


# Image Transformations
Learn about image transformations, such as resizing and rotating:
# Using OpenCV
# Example: Resizing
resized_image = cv2.resize(image_opencv, (width, height))

# Using Pillow
## Example: Rotating
rotated_image_pillow = image_pillow.rotate(angle)

# Image Drawing
## Discover how to draw shapes and text on images:
# Using OpenCV
# Example: Drawing a red rectangle
cv2.rectangle(image_opencv, (x1, y1), (x2, y2), (0, 0, 255), thickness)

# Using Pillow
# Example: Drawing a blue ellipse
draw = ImageDraw.Draw(image_pillow)
draw.ellipse([(x1, y1), (x2, y2)], outline=(0, 0, 255), width=thickness)

# Image Manipulation
Combine images or perform other manipulations:

# Using OpenCV
# Example: Merging two images
merged_image = cv2.addWeighted(image1, alpha, image2, beta, gamma)

# Using Pillow
# Example: Pasting one image onto another
image_pillow.paste(paste_image, (x, y), mask=paste_mask)

# Saving Images

Learn how to save processed images:
# Using OpenCV
cv2.imwrite('path/to/output.jpg', processed_image)

# Using Pillow
image_pillow.save('path/to/output.jpg')

This README provides a basic overview of image processing using OpenCV and Pillow. Feel free to explore more features and functionalities of these libraries to enhance your image processing skills.
