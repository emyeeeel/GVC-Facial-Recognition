# CS Elec 2 - Graphics and Visual Computing

## Overview

This repository contains the **Facial Recognition Activity** completed as part of the **CS Elec 2** (Graphics and Visual Computing) course at the **University of San Jose - Recoletos (USJR)** during the **2nd Semester** of the **2024 - 2025** academic year.

The project explores core concepts and technologies in **computer graphics** and **visual computing**, with a specific focus on facial recognition techniques using **computer vision**. The goal is to build a functional facial recognition system using popular libraries and algorithms.

## Table of Contents

- [Project Description](#project-description)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
  - [Prerequisites](#prerequisites)
  - [Installation Steps](#installation)
- [Usage](#usage)
- [License](#license)

## Project Description

The primary objective of this project was to develop a facial recognition system that utilizes **computer vision** techniques to detect and recognize human faces. The project enabled us to understand key components of visual computing, such as:

- Image processing techniques
- Feature extraction methods
- Machine learning models for facial recognition

The implementation leverages **OpenCV**, **NumPy**, and **Pillow (PIL)** for image processing and manipulation. We also utilized a pre-trained **Haar Cascade classifier** for effective face detection.

## Technologies Used

This project is built using the following technologies:

- **Python**: The primary programming language for implementing the system.
- **OpenCV** (`cv2`): A library used for image processing, face detection, and feature extraction.
- **NumPy**: A numerical computing library for handling arrays and mathematical operations.
- **Pillow (PIL)**: A Python Imaging Library for image manipulation tasks.
- **JSON**: Used for storing and handling facial recognition data, such as user labels and image encodings.
- **Haar Cascade Classifier**: A pre-trained classifier (`haarcascade_frontalface_default.xml`) used for detecting faces within images.

## Setup and Installation

### Prerequisites

Before you begin, ensure that the following software and libraries are installed on your local machine:

- **Python 3.x**: The programming language used for this project.
- **OpenCV** (`cv2`): Required for image processing and face detection.
- **NumPy**: Used for handling arrays and mathematical operations.
- **Pillow (PIL)**: Required for image manipulation.
- **JSON**: Used for storing facial recognition data.

You can install the necessary libraries by running the following command:

```bash
pip install opencv-python numpy pillow
```

### Installation

Follow the steps below to set up the project on your local machine:

### 1. Clone the Repository

Start by cloning this repository to your local machine. This will copy the entire project to your local environment.

```bash
git clone https://github.com/emyeeeel/GVC-Facial-Recognition.git
```

### 2. Navigate to the Project Directory

Change your working directory to the project folder after cloning the repository. This will allow you to run all scripts from the correct location.

To navigate to the project directory, run the following command:

```bash
cd GVC-Facial-Recognition-main
```

### 3. Prepare the Dataset

Before you begin collecting data, it's important to prepare the `datasets` folder.

- You can remove the contents of the `datasets` folder to make room for your own photos that will be used for training the model.
- The folder will store images for each user, and each user’s images should be placed in their own subfolder.

This step ensures that the dataset is ready to receive new images for training.

### 4. Collect Your Data

To collect photos for your dataset, run the `datacollection.py` script. This script allows you to add a new user's photos to the system.

- When you run the script, you will be prompted to enter a **user ID** and **name** to associate with the collected photos.
- The script will capture images of the user’s face and store them in the `datasets` folder under the user’s specified ID and name.

To collect your data, run:

```bash
python datacollection.py
```

### 5. Train the Model

Once you have collected enough data, you can proceed to train the facial recognition model.

- Run the `trainingdemo.py` script to train the model using the photos stored in the `datasets` folder.
- The script will process the images, extract facial features, and create a trained model that can recognize the faces associated with the dataset.

To train the model, run:

```bash
python trainingdemo.py
```

#### 6. **Test the Model**

Once the model is trained, you can test the facial recognition functionality by running the `testmodel.py` script. This script will evaluate the model's ability to recognize faces and return the confidence level for each recognized face.

To test the model, run the following command:

```bash
python testmodel.py
```

## Usage

Once you have set up and trained your facial recognition model, you can start using it to detect and recognize faces. Follow these steps to run the system and perform face recognition.

### Workflow Overview

The workflow consists of three main steps:
1. **Data Collection**: Collect images of users to build your training dataset.
2. **Model Training**: Train the model on the collected dataset to recognize faces.
3. **Model Testing**: Test the trained model by running the recognition system and evaluating its accuracy.