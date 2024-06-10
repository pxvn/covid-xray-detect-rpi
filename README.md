# Automated-Detection-of-COVID-19-Using-X-Ray-Imaging
An automated system for detecting COVID-19 from chest X-ray images using computer vision and deep transfer learning models like ResNet and DenseNet. This repository includes a trained model, dataset, and implementation for accurate and efficient COVID-19 diagnostics.

>USING RPI 4B (OS: 12 BOOKWORM)
>
## RPI UPDATE 
rpi@rpi:~ $ sudo apt update && sudo apt upgrade -y^C

sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

## CREATE VENV
Step 1: Install Dependencies
First, ensure your system has the necessary dependencies for building Python versions.


sudo apt update
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

Install pyenv:


curl https://pyenv.run | bash
Add pyenv to your shell:
Add the following lines to your ~/.bashrc (or ~/.zshrc if you are using Zsh):


export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"

Apply the changes:


source ~/.bashrc
Step 3: Install Python 3.10 with pyenv
Use pyenv to install Python 3.10.

pyenv install 3.10.0

> Create the environment:

pyenv virtualenv 3.10.0 myenv310
Activate the environment:

pyenv activate myenv310

Verify that your virtual environment is using Python 3.10.


python --version



