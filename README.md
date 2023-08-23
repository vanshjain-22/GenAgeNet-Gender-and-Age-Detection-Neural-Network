

# Project Goal

The aim of this project is to develop a system capable of approximating a person's age and gender based on facial images, either from a static photo or a live webcam feed.


## Project Overview

In this Python-based project, I leveraged Deep Learning techniques to accurately determine a person's gender and age range from a single facial image. The models I employed were originally trained by Tal Hassner and Gil Levi. The system predicts either 'Male' or 'Female' for gender and categorizes age into one of eight predefined ranges. Due to factors like lighting, makeup, and facial expressions, it's challenging to pinpoint an exact age, so I framed this as a classification problem rather than a regression task.
## Data Source

The project utilizes the publicly available Adience dataset, which you can find here. This dataset is a benchmark for facial images and includes a variety of real-world conditions such as different lighting and poses. It comprises 26,580 images of 2,284 individuals across eight age categories and is approximately 1GB in size.
## Required Python Libraries

OpenCV\
pip install opencv-python\
argparse\
pip install argparse\

## Components

opencv_face_detector.pbtxt
opencv_face_detector_uint8.pb
age_deploy.prototxt
age_net.caffemodel
gender_deploy.prototxt
gender_net.caffemodel
Sample images for testing
detect.py

For facial recognition, the project uses TensorFlow's .pb and .pbtxt files to hold the model's architecture and trained parameters. For age and gender classification, the .prototxt files describe the network layout, and the .caffemodel files contain the layer parameters.
## How To Use

Clone this repository.

Navigate to the project directory via Command Prompt or Terminal.

To identify age and gender from an image, run:

python detect.py --image <image_name>

Note: The image should be in the same directory as the project files.

For real-time age and gender detection via webcam, run:

python detect.py

To terminate the program, press Ctrl + C.
## Sample Outputs

Example 1: python detect.py --image girl1.jpg\
Predicted Gender: Female\
Estimated Age: 25-32 years\
[Example 1](Example/Detecting age and gender girl1.png)\

Example 2: python detect.py --image girl2.jpg\
Predicted Gender: Female\
Estimated Age: 8-12 years\
[Example 2](Example/Detecting age and gender girl2.png)