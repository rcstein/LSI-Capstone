# LSI-Capstone
 UVA Landscape Studies Initiative project code

## Introduction

Neural networks can learn a task quickly and with a relatively small amount of data if they are initialized with weights from another task on a large dataset, such as ImageNet, a technique known as transfer learning. Our capstone project, in collaboration with the Landscape Studies Initiative at UVA, used feature visualization techniques to qualitatively analyze how the dataset which produced the transferred weights affects a neural network's behavior and performace on its task.

This repository contains our project code, initial and final network parameters, and paper, which we submitted to the May 2020 SIEDS conference. Please refer to the paper for more information about the project's motivation, design, and conclusions. 

## Files

`LandscapeNet.ipynb'` contains the training code. We trained two neural networks: one initialized with weights from an ImageNet task, which are available via PyTorch's vision API, and one with weights from the Places365 project, which we obtained from their repository at https://github.com/CSAILVision/places365 . The latter are loaded in from `resnet18_places365.pth.tar`. 

`LandscapeNet_imagenet_pretrained` is the neural network trained for our landscape classification task using the ImageNet weights. `LandscapeNet_places365_pretrained`. These files are loaded into `OptimalClass.ipynb`. 

`OptimalClass.ipynb` contains the code used to generate images which optimize the activation of a given network node. 

**Note: due to image permissions, we have not uploaded our datasets, so the training code cannot actually be run.**

If you want to run the training code on your own dataset and classification task, download the repository and add an `Images` directory with sub-directories `Training` and `Validation`. Within each subdirectory organize your images into labeled folders for each class. Modify the code to expect the correct number of classes. 

You can of course also alter `OptimalClass.ipynb` to load your own weights.

