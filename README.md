# Pytorch Introduction and Image Classification

## Environment
### Please install the requirements:
```
pip install -r requirements.txt
```

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

Other datasets can be downloaded with the following links:
- [Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data)
..Download both train and test datasets, and unzip under `.pytorch/Cat_Dog_data`. Make sure the folders are named `train` and `test`, respectively.
..Run the following commands:
```
cd ~/.pytorch/Cat_and_Dog_data/train
mkdir cat dog
mv cat.* cat/
mv dog.* dog/
cd ~/.pytorch/Cat_and_Dog_data/test
mkdir data
mv *.jpg data/
```

Move the unzipped data to `~/.pytorch/` folder

A majority of this code was adopted from the Udacity Deep Learning course. 
Big thanks to Udacity for providing their code on an MIT License.
[Link to Udacity code](https://github.com/udacity/deep-learning-v2-pytorch/)
