# COVID-19 Detection from X-rays with Raspberry Pi 4

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pxvn/covid-xray-detect-rpi)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue?logo=python)](#)
[![TensorFlow Lite on RPi 4B](https://img.shields.io/badge/TensorFlow%20Lite%20Runtime-RPi%204B-green?logo=tensorflow)](#)
[![Raspberry Pi 4B](https://img.shields.io/badge/Device-Raspberry%20Pi%204B-lightgrey?logo=Raspberry%20Pi)](#)

This project uses TensorFlow Lite model to analyze chest X-rays for potential signs of COVID-19 on a RaspberryPi 4.

> ⚠️ **Disclaimer:** This is NOT a medical diagnostic tool. Consult a healthcare professional for any health concerns.

## How It Works

1. **Load X-ray image**
2. **Preprocess image** (resize, normalize)
3. **Run TensorFlow Lite model** (trained on 5,000 X-ray images)
4. **Interpret results** (predicted label & confidence score)
5. **Display results**

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

## Model Training

The TensorFlow Lite model was trained on a dataset of 5,000 chest X-ray images sourced from Kaggle, enabling it to distinguish between healthy and COVID-19-positive lungs.

## Getting Started

### Prerequisites

- Raspberry Pi 4B running Ubuntu 22.04 LTS
- Python 3.10+
- TensorFlow Lite Runtime
- Pillow (PIL Fork)
- Matplotlib

### Setup
- Open a terminal on your Raspberry Pi:

 `sudo apt update
   sudo apt install python3-venv`

- Install pip:

`sudo apt install python3-pip`

1. Create a virtual environment: `python3 -m venv venv_name`
2. Inastall py 3.10:
`
sudo apt update
sudo apt install python3.10
`

3. Activate it: `source venv_name/bin/activate`
4. Install dependencies: `pip install numpy Pillow matplotlib tflite-runtime jupyter`

## Usage

1. **Open the Jupyter Notebook:** `jupyter notebook`
2. **Follow instructions in the notebook.** 
   - Optionally, specify a custom model/labels file path: `--model <path>` or `--labels <path>`

## Project Goals

This project aims to:

- **Educate and inspire:**  Demonstrate AI's potential in medical image analysis.
- **Foster collaboration:**  Encourage contributions and further development.

## Contributing

I welcome contributions! Please open an issue or submit a pull request.

## Additional Resources

- [TensorFlow Lite](https://www.tensorflow.org/lite)
- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
