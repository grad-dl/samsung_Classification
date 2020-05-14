# Pytorch Introduction and Image Classification

## Environment
### Please install the requirements:
```
pip install -r requirements.txt
```
The above command assumes you are in a clean Python virtualenv, running Python3.7.x

If you're running Conda on a windows machine, the above installation may not work. 
* First, install PyTorch version 1.2.0 by following the instructions from this [link](https://pytorch.org/get-started/previous-versions/#v120).
* Then, remove the lines `torch==1.2.0`, `torchvision==0.4.0` and run the command above. 
* For some unknown reason, conda on windows won't let you install Pytorch with the `requirements.txt`.

## Datasets

The following datasets should be downloaded. Open up python and download the datasets:

```
from torchvision import datasets
# MNIST
trainset = datasets.MNIST('~/.pytorch/MNIST_data/', download=True, train=True)
testset = datasets.MNIST('~/.pytorch/MNIST_DATA/', download=True, train=False)
# FashionMNIST
trainset = datasets.FashionMNIST('~/.pytorch/F_MNIST_data/', download=True, train=True)
trainset = datasets.FashionMNIST('~/.pytorch/F_MNIST_data/', download=True, train=False)
```

The Cats vs Dogs dataset can be downloaded as follows:
```
cd ~/.pytorch
wget https://s3.amazonaws.com/content.udacity-data.com/nd089/Cat_Dog_data.zip
unzip Cat_Dog_data.zip
```

## Pretrained Models

Lastly, we have some pre-trained models we need to download. Open up a python console and run the following commands:
```
from torchvision import models
model = models.resnet18(pretrained=True)
model = models.resnet50(pretrained=True)
model = models.desnet121(pretrained=True)
```
This will download the torch models to the default folder. (Usually this is `~/.cache/torch/checkpoints/`)

## Acknowledgements
A majority of this code was adopted from the Udacity Deep Learning course. 
Big thanks to Udacity for providing their code on an MIT License.
[Link to Udacity code](https://github.com/udacity/deep-learning-v2-pytorch/)
