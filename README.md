
# COVID19 DETECTION FROM XRAY USING RASPBERRYPI-4

<p align="center">
<a href="https://colab.research.google.com/github/yourusername/chestscanai"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
<img src="https://img.shields.io/badge/python-3.10%2B-blue?logo=python" alt="Python 🐍">
<img src="https://img.shields.io/badge/TensorFlow%20Lite%20Runtime-RPi%204B-green?logo=tensorflow" alt="TensorFlow Lite 🧠">
<img src="https://img.shields.io/badge/Pillow-Latest-yellow?logo=pypi" alt="Pillow 🖼️">
<img src="https://img.shields.io/badge/Matplotlib-Latest-orange?logo=matplotlib" alt="Matplotlib 📈">
<img src="https://img.shields.io/badge/Jupyter%20Notebook-Latest-red?logo=jupyter" alt="Jupyter 📓">
<img src="https://img.shields.io/badge/Device-Raspberry%20Pi%204B-lightgrey?logo=Raspberry%20Pi" alt="Raspberry Pi 🍓">
</p>

This powerful tool leverages artificial intelligence to analyze chest X-ray images and identify potential signs of COVID-19. The core of the project is a pre-trained TensorFlow Lite model, meticulously trained on a dataset of 5,000 X-ray images sourced from Kaggle. This extensive training enables the model to distinguish between healthy lungs and those exhibiting patterns consistent with COVID-19.

Utilizes the TensorFlow Lite framework for optimized performance on devices like the Raspberry Pi.

>*⚠️ Please note: This project is NOT a medical diagnostic tool and should not be used as a substitute for professional medical advice.*
>>  We encourage researchers, developers, and medical professionals to explore, contribute to, and build upon this open-source project. Together, we can harness the 
     power of AI to make a real difference.


## Table of Contents

* [Technical Overview](#how-it-works-technical-overview)
 * [Installation and Setup](#installation-and-setup)
    - [Prerequisites](#prerequisites)
    - [Setup Instructions](#setup-instructions)
* [Usage](#usage)
    - [Run Jupyter Notebook](#run-jupyter-notebook)
    - [Command-line Arguments](#command-line-arguments)
* [Disclaimers](#disclaimers)
* [Additional Resources](#additional-resources)


## Technical Overview

It follows these steps to analyze chest X-ray images:

1. **Image Loading**: Uses [Pillow](https://pillow.readthedocs.io/en/stable/) (PIL Fork) to read the X-ray image.
2. **Preprocessing**: Involves resizing, normalization, and formatting the image to meet the model's input requirements.
3. **Model Inference**: Utilizes [TensorFlow Lite](https://www.tensorflow.org/lite) Runtime to run the pre-trained model on the processed image.
4. **Output Interpretation**: Extracts the predicted label and confidence score from the model's output.
5. **Visualization**: Uses [Matplotlib](https://matplotlib.org/stable/contents.html) to display the original image alongside the prediction.

### Flow Chart

```mermaid
graph LR
    A[Start] --> B[Load Image]
    B --> C[Preprocess]
    C --> D[Run Model]
    D --> E[Get Prediction]
    E --> F[Display Results]
    F --> G[End]
```

## Installation and Setup

> 🧩Prerequisites

| Component               | Version               |
|-------------------------|-----------------------|
| Python                  | 3.10                  |
| TensorFlow Lite Runtime | Compatible with RPi 4B |
| Pillow (PIL Fork)       | Latest                |
| Matplotlib              | Latest                |
| [Jupyter Notebook](#run-jupyter-notebook)       | Latest                |
| Device                  | Raspberry Pi 4B       |
| OS                      | [Ubuntu](https://ubuntu.com/download/raspberry-pi) 22.04 LTS      |


## Setup Instructions

### Create and Activate a Virtual Environment

> Open a terminal on your Raspberry Pi:

```bash
sudo apt update
sudo apt install python3-venv
```

### Create a new virtual environment (replace 'venv_name' with your preferred name)
```bash
python3 -m venv venv_name
```

### Activate the virtual environment
```bash
source venv_name/bin/activate
```
### Install Python 3.10:

 ```bash
sudo apt update
sudo apt install python3.10
```

### Install pip:

```bash
sudo apt install python3-pip
```

### Install Git:

```bash
sudo apt install git
```
### Install Required Packages

> Now, within the activated virtual environment, install the necessary Python packages:

```bash
pip install numpy Pillow matplotlib tflite-runtime
```

### Install Jupyter Notebook:

```bash
pip install jupyter
```

### Prepare Model and Label Files
- Model File (model_unquant.tflite): Ensure this TFLite model file is present and accessible from your Python script.

- Labels File (labels.txt): This file should contain labels corresponding to the output classes of your TFLite model. 


## Usage

### Run Jupyter Notebook

```bash
jupyter notebook
```

> Open .ipynb in Jupyter and follow the instructions within the notebook.

### Command-line Arguments (Within the Notebook)

>Use --model to specify a different model file path.
>Use --labels to specify a different labels file path.


## Disclaimers
    This model is NOT a substitute for professional medical advice.
    Always consult a healthcare professional for any health-related concerns.
    The tool is designed for educational and research purposes only.


## Potential Improvements
  Integrating more advanced CNN models for improved accuracy.
  Developing a web-based interface for easier accessibility.
  Adding support for other types of medical imaging.

## Additional Resources
- [TensorFlow Lite](https://www.tensorflow.org/lite)
- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

