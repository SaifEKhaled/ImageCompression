### **Image Compression using Linear Algebra** 



# Overview
This repository contains Python code for a comprehensive image compression project that harnesses Linear Algebra concepts, particularly Singular Value Decomposition (SVD), to efficiently reduce the storage footprint of digital images while maintaining their visual quality. Image compression plays a crucial role in optimizing storage, bandwidth, and data transfer in various applications such as web development, image archiving, and more. This project focuses on the compression of color images, breaking down the process step by step.

I've participated with this project in 4th Egyptian Junior Researcher Competition - 16th UGRF (Special Edition) at Nile University

## Table of Contents
- [Dependencies](#dependencies)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Methods and Techniques](#methods-and-techniques)
- [Examples](#examples)
- [Contributing](#contributing)
  
## Dependencies
This project relies on the following libraries:

matplotlib: Matplotlib is a versatile Python library used for creating data visualizations, including the display of images. In this project, it is utilized for loading and visualizing both the original and compressed images.

numpy: NumPy, a fundamental library for numerical computing in Python, is essential for multi-dimensional array operations and matrix manipulations. It plays a pivotal role in performing SVD and various matrix operations within this project.

## Usage
Clone this repository to your local machine using git clone.

Ensure you have the required dependencies installed using pip install -r requirements.txt.

Run the image_compression.py script, providing the path to your target image as an argument. For example:

shell
Copy code
python image_compression.py dog.jpg
Experiment with different compression ranks to observe the trade-off between image quality and storage size.

## How It Works
The project follows these fundamental steps:

Image Loading: We start by using Matplotlib to load the target color image. This process converts the image into a numerical representation, which we can manipulate as a pixel array.

Color Channel Separation: The image is then separated into its constituent color channels: red, green, and blue. This separation enables us to independently apply SVD to each color channel.

Singular Value Decomposition (SVD): SVD is a key Linear Algebra technique employed separately for each color channel. It decomposes the color channel into three matrices: U, S, and VT. U and VT contain structural information, while S contains singular values that indicate the significance of each component.

Compression Function: The compress function is provided a rank as input, and it uses this rank to reconstruct each color channel. By selecting a lower rank, we retain only the most vital components of the image, effectively compressing it.

Image Reconstruction: The compressed red, green, and blue channels are recombined to create a single compressed image. This compressed image can be displayed using Matplotlib.

## Methods and Techniques
This project showcases several important methods and techniques:

Image Compression: Using SVD, this project efficiently compresses images by retaining only the most significant components, reducing storage requirements.

Singular Value Decomposition (SVD): A fundamental technique from Linear Algebra, SVD helps decompose the image into three matrices and enables precise control over image compression.

## Examples
You can experiment with image compression and see the results for yourself. Adjust the rank parameter in the compress function to control the level of compression, allowing you to understand the trade-offs between image quality and storage size.

## Contributing
We welcome contributions! If you have ideas for improvements or new features, feel free to open an issue or submit a pull request.
