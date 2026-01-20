# Image Recognition: MLP vs. CNN (CIFAR-10)
##Sagar Bhandari
###Machine Learning


**I have written a jupyter notebook in a very self-explanatory manner.** **Please read the notebook for the full details.** 
 
Testing out deep learning on the CIFAR-10 dataset. I wanted to see how two different neural network architectures compared when it comes to identifying small scale color images. This project covers the build, the training process, and the final head-to-head results. 

###Project Overview
This project explores the application of deep learning architectures for image recognition. Using the benchmark CIFAR-10 dataset, I designed, implemented, and compared two distinct neural network models:

Multilayer Perceptron (MLP): A baseline fully connected neural network.

Convolutional Neural Network (CNN): A specialized architecture for spatial data.

The primary objective was to evaluate the performance trade-offs between these architectures in terms of classification accuracy and computational efficiency.

###Dataset
The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class.

Training Set: 50,000 images

Test Set: 10,000 images

Classes: Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck.

###Key Features
Local Execution: Developed and tested locally to ensure full control over the execution environment and hardware utilization.

Hardware Acceleration: Leverages Apple Silicon (MPS device) for optimized training speeds, with fallbacks for CUDA or CPU.

Custom Training Loops: Built comprehensive training pipelines including forward passes, backpropagation, and mixed-precision optimization.

Comparison Analysis: Detailed evaluation of how model depth and architecture (e.g., flattening vs. convolutional layers) affect final accuracy.

###Installation & Setup
Prerequisites
Python 3.x
PyTorch
Torchvision
Matplotlib
NumPy

Local Configuration
To run this notebook locally, ensure your environment is configured for HTTPS dataset downloads



Project Structure
Data Preprocessing: Standardizing 32x32x3 images using ToTensor() transformations.

Part 1: MLP Implementation: Experimenting with fully connected layers and observing the impact of hidden layers on accuracy.

Part 2: CNN Implementation: Utilizing convolutional layers to capture spatial hierarchies in image data.

Part 3: Fast.ai Integration (Optional): Leveraging high-level APIs for rapid prototyping and performance comparison.

Conclusions
The project highlights the inherent advantages of Convolutional Neural Networks for image tasks. Key takeaways include:

Increasing hidden layers in an MLP does not always correlate with improved accuracy, likely due to the loss of spatial features during the flattening process.

CNNs significantly outperform MLPs by preserving the structural integrity of image data through convolutional filters.

Using optimized training techniques (like mixed precision) allows for high-performing models with minimal, efficient code.

*** Note: This project was developed as part of a Fall 2025 academic curriculum.
