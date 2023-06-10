# EcoVision
An AI based Trash can
# EcoVision: Trash Can Object Detection with YOLO

EcoVision is a computer vision project that focuses on promoting environmental sustainability by automating the process of trash classification. Using the YOLO (You Only Look Once) object detection algorithm, EcoVision enables a smart trash can to classify different types of waste accurately.

# Project Overview

The goal of EcoVision is to provide an intelligent solution for waste management by automatically identifying and segregating various types of trash. The system utilizes a YOLO-based object detection model trained on a dataset consisting of six distinct classes: paper, plastic, metal, glass, cardboard, and a general class for all other types of waste.

# Key Features
1. Object Detection: EcoVision employs the YOLO algorithm to detect and locate objects in real-time video streams captured by a camera placed above the trash can.
2. Trash Classification: Once an object is detected, EcoVision uses its trained model to classify the object into one of the predefined classes, including paper, plastic, metal, glass, cardboard, or a general trash category.
3. Segregation and Sorting: Based on the classification results, the trash can automatically separates and sorts the waste into different compartments dedicated to each specific trash type.
4. Real-time Feedback: EcoVision provides immediate visual feedback, such as a graphical display or LED indicators, to indicate the category assigned to the detected trash object.

# Technologies Used

* Python: The project is implemented using Python programming language due to its extensive libraries and frameworks for computer vision tasks.
* YOLO (You Only Look Once): The YOLO object detection algorithm is utilized for accurate and efficient real-time object detection.
* OpenCV: OpenCV library is employed for image and video processing, including capturing, pre-processing, and post-processing of video frames.
* Deep Learning Framework: A popular deep learning framework such as TensorFlow or PyTorch is utilized for training the object detection model.
* Hardware Setup: The system requires a camera for capturing video footage and a microcontroller or single-board computer for running the code and controlling the trash can.


# Requirements

*  Python >= 3.8
*  Requirements that are specified in the yolov5 Model

# Usage Instructions
To use EcoVision, follow these steps:

1. Set up the hardware by placing a camera above the trash can and connecting it to the microcontroller or single-board computer.
2. Install the required dependencies and libraries specified in the project's documentation.
3. Download or train the YOLO-based object detection model using the provided dataset or your own dataset.
4. Configure the system to run in real-time video mode, capturing frames from the camera feed.
5. Apply the object detection model to the captured frames to detect and classify the trash objects.
6. Implement the segregation and sorting mechanism in the trash can to direct the classified trash objects into separate compartments.
7. Provide appropriate visual feedback to the user to indicate the category assigned to the detected trash object.


# Train your model
Use Google colab cloud based training.
1. First your google drive using this command `from google.colab import drive
drive.mount('/content/drive')`
2. Download our dataset given from the following drive link and upload it in your google drive.
3. Extract the dataset using the command `import zipfile
with zipfile.ZipFile(zip_file_path, 'r') as zip_ref:
    zip_ref.extractall(extract_path)`
5. Run this `%cd yolov5
%pip install -qr requirements.txt`
4. Then start training using this command `!python train.py --img 416 --batch 16 --epochs 150 --data {dataset.location}/data.yaml --weights yolov5s.pt --cache` specify the path of the data correctly. You can change the batch and epoch as of your need and accuracy.
5. Download the trained weights 'best.pt' from `runs/train/exp` to your device. You can use use our already pre trained weights that provided here.


# Deploy on your system

1. Install python - >=v3.8
2. Create one virtual environment named "whatsapp" by run the command `python -m venv yolo`
3. Run `cd yolo/scripts`
4. Run `activate.bat`
5. Run `cd ../..`
6. Run `pip install -r requirements.txt`
7. Run the following command `python detct.py --weights best.pt --source 0` to deploy using your system like rasperry pi, Jetson Nano or anything else.
8. Note: Specify the correct source of the camera.

# Contribution Guidelines
If you wish to contribute to EcoVision, please follow these guidelines:

1. Fork the repository and create a new branch for your contributions.
2. Ensure that your code adheres to the project's coding style and follows best practices.
3. Clearly document any new features, changes, or bug fixes in the code.
4. Test your changes thoroughly and provide relevant test cases when applicable.
5. Create a pull request and describe the changes you've made in detail.

# Acknowledgments
We would like to express our gratitude to the open-source community and the developers behind YOLO, OpenCV, and the deep learning
