# Automated Detection of COVID-19 Using X-Ray Imaging (IN RASPBERRYPI)
An automated system for detecting COVID-19 from chest X-ray images using computer vision and deep transfer learning models like ResNet and DenseNet. This repository includes a trained model, dataset, and implementation for accurate and efficient COVID-19 diagnostics.

>USING RPI 4B (OS: UBUNTU V22)
>>PYTHON 3.10

## RPI UPDATE 

 ```bash sudo apt update && sudo apt upgrade -y^C ```

```bash
sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```
## CREATE VENV
Install Dependencies
- First, ensure your system has the necessary dependencies for building Python versions.


```bash
sudo apt update
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```
## Install pyenv:

```bash
curl https://pyenv.run | bash
```
Add pyenv to your shell:
- Add the following lines to your ~/.bashrc (or ~/.zshrc if you are using Zsh):

```bash
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
``` 
## Apply the changes:

```bash
source ~/.bashrc
```

- Install Python 3.10 with pyenv
- Use pyenv to install Python 3.10.

```bash
- pyenv install 3.10.0
```
## Create the environment:
- pyenv virtualenv 3.10.0 myenv310

- Activate the environment:

```bash
- pyenv activate myenv310
```
- Verify that your virtual environment is using Python 3.10.

```bash
python --version
```


